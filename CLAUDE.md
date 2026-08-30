# Aether

A hard-magic system for fiction: the Aether Codex, plus a static site that presents it.

## Layout

- `codex/` — the source of truth. Sixteen markdown files, one per area.
- `index.html` — the site. Self-contained, no build step, no dependencies;
  deployable from the repo root via GitHub Pages or Cloudflare Workers.
- `README.md` — project front matter.
- `wrangler.jsonc` / `.assetsignore` — Cloudflare Workers static-asset
  deploy config. The repo's Workers Builds Git integration (project
  `aether`) picks this up on every push with no dashboard-side build
  command needed: `assets.directory` is the repo root, and
  `.assetsignore` keeps `codex/`, `CLAUDE.md`, and `README.md` off the
  deployed site since `index.html` is the only page. There's no server
  script — the router is entirely hash-based (`#/foundations`, …), so
  the Worker only ever has to answer `/` with `index.html`.

## The Codex

Start at `codex/overview.md`: it carries the version, the notation rules, and a
file map naming which sections and equations live in which file. Its reading
order is foundations → grand-equation → power-hierarchy → the technique files in
tier order, with `spell-directory.md` and `glossary.md` as references to consult
rather than read through.

Three conventions matter when editing:

- **Section and equation numbers are global.** "§3.5" and "Eq. 4.7" mean the same
  thing in every file. Never renumber to suit one file's local order — §3.3 sits
  in `power-hierarchy.md` even though §3.2 and §3.4 are in `grand-equation.md`.
- **Equations are plain ASCII.** No Greek letters, hats, daggers or symbols, so
  they can be typed straight into a manuscript. Write `Xi(Ae, g)`, `dAe`,
  `lam_i`, `M_op` — not their typeset equivalents.
- **Extend by appending.** New techniques and derivations go at the end of the
  relevant file, with a version bump and a one-line entry in
  `codex/changelog.md`. New equations continue the running global numbering
  tracked in `codex/glossary.md` (§6).

Cross-references between files are written as `codex/<name>.md` and all resolve
as-is; keep that form if you add more.

## The site

`index.html` presents the Codex as a multi-page reference — sixteen pages
(Foundations, the Grand Equation, the Hierarchy, one page per technique tier,
the Directory, Glossary & Index, Changelog) in one self-contained file. Each
page is a `<template id="t-…">` block; a hash router (`ROUTES` array at the
bottom of the script) clones it into `#app`, so `#/techniques/adept` is a
stable, linkable address. Content is transcribed from `codex/`, not generated
from it, so a substantive Codex change may need the matching page updated.

Structure notes:

- To add a page: add a `<template>`, a sidebar link (`data-r` must equal the
  route path), and a `ROUTES` entry — order in `ROUTES` drives the prev/next
  pager at the foot of every page.
- Interactive figures live in per-page `init*` functions. They draw on canvas
  via the small `frame`/`lineSeries`/`tag` helpers; animation loops must check
  `token !== routeToken` so they stop on navigation, and anything
  size-dependent registers with `onResize`.
- The Spell Directory renders from the `SPELLS` array; the Glossary and
  Equation Index render from `GLOSSARY` and `EQINDEX`. Extend those arrays
  rather than writing markup by hand.

Design notes, so edits stay coherent:

- Committed to a single dark visual world: onyx ground, gold accent. Every
  colour is painted explicitly; there is no light theme to keep in sync.
- Flat throughout, by rule — no glow, no blur, no gradient fill or fade,
  in CSS or on canvas. Emphasis is drawn with a solid fill, a 1–2px stroke, or
  a brighter/lighter step of the same token, never a `box-shadow`,
  `text-shadow`, or `*-gradient()`. If a new element seems to need one to
  read clearly, that is a signal to widen the shape or lighten the token
  instead.
- Colour carries information. The channel palette is a metals set and should
  stay tied to meaning: amber gold `--gauge` for the gauge sector (F_f), copper
  `--quark` for the quark sector (M_op), platinum `--metric` for the metric
  sector (g), iron `--ceiling` for the Unsolved Ceiling, pale gold `--aether`
  for aether itself and every interactive accent. `--danger` marks backlash
  and failure states. The four muted tokens (`--ink-faint`, `--ceiling`,
  `--danger`, `--quark`) were each tuned to sit at ≥5:1 contrast against both
  `--void` and `--plate` — check new tokens the same way (WCAG relative
  luminance) rather than eyeballing them against the editor's colour picker.
- The cursor is themed, not the system arrow: three small inline-SVG data
  URIs in the `--cur-default`/`--cur-pointer`/`--cur-text` custom properties
  (a hollow ring for ambient, a filled point in a brighter ring for anything
  clickable — the same idle/coupled distinction the coupling-bench figure
  draws — and a small I-beam for selectable text). Reference them with
  `cursor:var(--cur-pointer)` / `cursor:var(--cur-text)` on new elements
  rather than the bare `pointer`/`text` keyword, or the browser default will
  show through. `default` stays native on purpose on disabled controls
  and inert cells.
- Type is Cormorant Garamond (display), Spectral (body), IBM Plex Mono (every
  equation, directory code and § marker), loaded from Google Fonts.
- Prefer a short autoplaying (or click-triggered) animation over an
  interactive control that only swaps text — a slider or picker earns its
  keep when moving it changes what you *see*, not just what you read. The
  bar-gauge on the Master page, the eigenvector map on the Artisan page, and
  the Sim[…] boundary diagram on the Grand Equation page are the pattern:
  canvas or CSS-transition state that reacts to an existing control, kept
  legible without a legend. Loops must check `token !== routeToken` each
  frame so they stop on navigation, and `prefers-reduced-motion` must land on
  the same end state a full play-through would reach, not a blank canvas.
- Keep it dependency-free, respect `prefers-reduced-motion` (interactive
  figures fall back to a meaningful static or single-step state), and check
  there is no horizontal overflow at 390px — grid children that hold `<pre>`
  equations need `min-width:0`.
