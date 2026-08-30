# Aether

A hard-magic system for fiction: the Aether Codex, plus a static site that presents it.

## Layout

- `codex/` — the source of truth. Sixteen markdown files, one per area.
- `index.html` — the site. Self-contained, no build step, no dependencies;
  deployable from the repo root via GitHub Pages.
- `README.md` — project front matter.

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

`index.html` presents a selection of the Codex — the layered-field premise, the
three axes, the Grand Equation, the Power Hierarchy, the Spell Directory and the
four Ascension paths. Its content is transcribed from `codex/`, not generated
from it, so a substantive Codex change may need the page updated to match.

Design notes, so edits stay coherent:

- Committed to a single dark visual world: onyx ground, gold accent. Every
  colour is painted explicitly; there is no light theme to keep in sync.
- Colour carries information. The channel palette is a metals set and should
  stay tied to meaning: amber gold `--gauge` for the gauge sector (F_f), copper
  `--quark` for the quark sector (M_op), platinum `--metric` for the metric
  sector (g), iron `--ceiling` for the Unsolved Ceiling, pale gold `--aether`
  for aether itself and every interactive accent.
- Type is Cormorant Garamond (display), Spectral (body), IBM Plex Mono (every
  equation, directory code and § marker), loaded from Google Fonts.
- The Spell Directory renders from the `SPELLS` array near the end of the file;
  add entries there rather than writing card markup by hand.
- Keep it dependency-free, respect `prefers-reduced-motion`, and check there is
  no horizontal overflow at 390px.
