# Aether — Roblox Studio Implementation Reference

Condensed, game-implementable version of the Aether Codex (`codex/`), for
building the magic system in Roblox Studio (Luau). This file translates the
Codex's math into stats, formulas, and state machines a game needs — it is
**not** a Codex file itself: it doesn't carry § / Eq. numbers, isn't subject
to the Codex's extend-by-appending rules, and isn't canon. When this file and
`codex/` disagree, `codex/` is the source of truth; re-derive from there and
update this file to match. It's deliberately excluded from the deployed site
(see `.assetsignore`) since it's a dev/reference doc, not site content.

Full citations point back at `codex/<file>.md §<section>` / `Eq. <n>` so you
can verify any formula against its source before shipping it.

---

## 1. Core model: three independent axes per player

Every caster is defined by three separate values, tracked independently
(`codex/foundations.md` §2, "The Three Axes, Named"). None of them is a
resource pool — there is no mana/stamina meter in the source material.

| Axis | What it is | Varies | Roblox-side storage |
|---|---|---|---|
| **Comprehension** | Which coupling channels are solved — the *ceiling* | Only on "research" progress, not per-cast | Player data: a set/table of unlocked channels (see §2) |
| **Fidelity (`Fid`)** | How well *this specific cast* reproduces the ideal structure, `0 <= Fid <= 1` (Eq. 3.2) | Per-cast, per-attempt | Computed at cast time, not stored |
| **Practice depth (`prac`)** | Per-technique drill progress toward unassisted (no-glyph) casting (Eq. 3.4) | Per technique, accumulates with reps | Player data: a table keyed by technique id |

Design rule that follows directly from the source: **do not implement a mana
bar.** Power is gated by *what's unlocked* (comprehension) and *how well the
player executes the cast* (fidelity), never by a depleting/regenerating
resource. If your game needs a cast-frequency limiter, use cooldowns tied to
`tau_switch` (§4 below) or per-technique cast timers, not a resource pool.

---

## 2. Comprehension: the tech tree

Comprehension is exactly the union of "coupling channels" a caster has a
proven functional form for (`codex/foundations.md` §1.3, §2). This maps
directly onto a Roblox skill tree / unlock table. Three channel types:

- **Gauge channel `delta(F_f)`** — one entry per fundamental force: EM,
  Gravity, Strong, Weak. Each is unlocked independently (a Novice `k_f`
  term, closed form — `codex/techniques-novice.md` §4.0).
- **Quark channel `delta(M_op)`** — unlocked per-material eigenvector
  (`lam_i`, `e_i`). An Artisan's `S` is a small finite set of materials
  (Eq. 3.1e); a Master's `S` is the complete basis (Eq. 4.18).
- **Metric channel `delta(g)`** — unlocked as an *order* of a perturbation
  series (Warden, Eq. 3.1f) or a bounded closed-form domain (Sovereign/
  Legend, Eq. 3.1g), never as a flat on/off toggle.

**Suggested Luau shape:**

```lua
-- PlayerComprehension (persisted)
{
  gauge = { EM = true, Gravity = true, Strong = false, Weak = false },
  crossCoupling = { ["EM_Strong"] = true, ["EM_Gravity"] = false, ... }, -- Chi(f1,f2), Adept
  quark = { -- Eq. 3.1e: S, the solved eigenvector subset
    Salt = true, Iron = false, Bone = false, ...
  },
  quarkComplete = false, -- Master tier: S = full eigenbasis (Eq. 4.18)
  metric = {
    order = 0,      -- 0 = none, 1 = Xi_0, 2 = Xi_0+Xi_1 (Warden, Eq. 3.1f)
    provenSites = {},   -- R_proven geometries a Warden has validated (Eq. 4.20)
    sovereign = false,  -- closed-form Xi(Ae,g), bounded R_dom/t_dom (Eq. 3.1g)
  },
}
```

Tier (Novice → Legend, `codex/power-hierarchy.md` §3.3) is a **derived
label**, not stored state — compute it from the comprehension table:

| Tier | Derived from |
|---|---|
| Novice | exactly one `gauge[f] == true` |
| Journeyman | 2+ `gauge[f] == true`, no `crossCoupling` entries true |
| Adept | any `crossCoupling[pair] == true` |
| Artisan | `quark` has 1+ entries true, `quarkComplete == false` |
| Master | `quarkComplete == true` |
| Warden | `metric.order >= 1` |
| Sovereign | `metric.sovereign == true`, bounded domain |
| Legend | Sovereign math at `R_dom`/`t_dom` pushed to "effectively permanent" — a scale/duration threshold on the same fields, not a new unlock |

Tier is a ceiling summary for UI, not a gameplay gate by itself — gate
individual spells by their specific channel requirement (e.g. Flash-Forge
needs `crossCoupling.EM_Strong`, not "tier >= Adept").

---

## 3. Fidelity: the per-cast skill check

Fidelity (`Fid`, Eq. 3.2, `0 <= Fid <= 1`) is the overlap between the ideal
cast structure and what the player actually executed *this time*. This is
where player input/skill expression lives — the equivalent of an aim-timing
or QTE-style mechanic, not a stat roll.

**Recommended implementation:** drive `Fid` from a skill-based input rather
than RNG — e.g. a timing bar, a glyph-tracing minigame, or gesture accuracy
— since the source material explicitly ties fidelity to precision of
execution, steadiness, and time invested (§3.5), not chance.

```lua
-- Fid in [0, 1], produced by your input minigame
local function computeFidelity(inputAccuracy: number, wasRushed: boolean, isDistracted: boolean): number
    local fid = inputAccuracy
    if wasRushed then fid *= 0.5 end
    if isDistracted then fid *= 0.6 end
    return math.clamp(fid, 0, 1)
end
```

**Resolution threshold (Eq. 3.3):** below `Fid_min`, the cast fails
*quietly* — no effect, no damage, no backlash. This is a distinct, safe
failure mode; do not attach a penalty to it.

```lua
local FID_MIN = 0.15 -- tune per game feel

if fid < FID_MIN then
    return { result = "fizzle" } -- silent, no VFX beyond a soft puff, no cost
end
```

**Unassisted casting (Eq. 3.4):** a caster can drop the "glyph/gesture"
requirement per-technique once `prac(x) >= prac_min` for that specific
technique. In Roblox terms: a technique cast with no anchor (no glyph
UI, no gesture minigame) is only allowed once `PlayerPractice[techniqueId]
>= PRAC_MIN[techniqueId]`; before that threshold, an anchor-less attempt
should be forced through the same fizzle path as a sub-`Fid_min` cast,
never through a weaker partial effect (the source models this as a **step
function**, not a gradient — Eq. 3.4's `Step(...)`).

---

## 4. Tier-by-tier formulas (safe to port near-verbatim)

Below: source equation, the plain-language effect, and a direct Luau
formula. All `k_*` and `lam_i` values are tunable design constants — the
Codex intentionally leaves their magnitude to setting/game balance; only the
*shape* of each formula is canon.

### Novice — single gauge-sector effect (`codex/techniques-novice.md` §4.0)

```lua
-- Eq. 4.0a — Thermal Excitation
local function thermalPower(kEM: number, fid: number, aeLocal: number): number
    return kEM * fid * aeLocal ^ 2
end

-- Eq. 4.0b — Minor Levitation (net force multiplier on gravity)
local function levitationFactor(kGrav: number, fid: number): number
    return 1 - kGrav * fid  -- multiply against mass * g_local
end

-- Eq. 4.0c — Minor Cohesion Boost
local function cohesionBoost(bindEnergy: number, kStrong: number, fid: number): number
    return bindEnergy * (1 + kStrong * fid)
end

-- Eq. 4.0d — Decay Nudge (Spell Directory §4.4)
local function decayOutput(gamma0: number, kWeak: number, fid: number, ePerDecay: number, nUnstable: number): number
    local gammaEff = gamma0 * (1 + kWeak * fid)
    return gammaEff * ePerDecay * nUnstable
end
```

No failure mode worth naming below `Fid_min` beyond the standard fizzle —
these are the safest tier to prototype first.

### Journeyman — sequential, non-blended (`codex/techniques-journeyman.md` §4.5)

Two+ unlocked gauge channels, no simultaneous blend. Model as a state
machine with disjoint activation windows and a hard switch cooldown:

```lua
-- Eq. 4.13 — Sequential Invocation Overhead
-- Win_1(t) . Win_2(t) = 0 for all t  =>  only one technique's window active at once
local TAU_SWITCH = 0.6 -- seconds; tune down with player's drilled proficiency, never to 0

local ActiveWindow = nil -- "technique1" | "technique2" | nil

local function trySwitchTechnique(newTechnique: string, lastWindowEndTime: number, now: number): boolean
    if now - lastWindowEndTime < TAU_SWITCH then
        return false -- still in dead time; cannot begin newTechnique's window yet
    end
    ActiveWindow = newTechnique
    return true
end
```

Do not let `tau_switch` reach zero — the source is explicit that a true
zero-gap alternation is definitionally the Adept transition, not a faster
Journeyman.

### Adept — true simultaneous blend (`codex/techniques-adept.md` §4.6)

```lua
-- Eq. 4.14 — Cross-Coupling (0 <= Chi <= 1, unlocked per force-pair)
-- Eq. 4.15 — Adept Combined Output. Note Fid is SQUARED, not linear.
local function adeptComboOutput(kF1: number, kF2: number, fid: number, chi: number): number
    return kF1 * kF2 * (fid ^ 2) * chi
end
```

There are exactly six unordered force pairs (EM/Gravity/Strong/Weak choose
2) — the full Adept combo list is closed, matching `codex/spell-directory.md`
AD-01 through AD-06. Don't design a "seventh pair"; extend Adept depth via
`Fid`/`Chi` refinement or by branching into Artisan instead.

### Artisan — narrow, material-locked (`codex/techniques-artisan.md` §4.7)

```lua
-- Eq. 4.16 — Eigenvector Draw: only valid if material's eigenvector is in the player's solved set S
local function artisanEffect(lamI: number, fid: number, dAeLocal: number): number
    return lamI * fid * dAeLocal
end

-- Eq. 4.17 — Off-basis extrapolation backlash: reaching for an UNSOLVED material
-- This is a comprehension failure, not an execution one — it can fire even at Fid = 1.
local function offBasisBacklash(lamGuess: number, lamTrue: number, volumeIntegral: number): number
    return (lamGuess - lamTrue) ^ 2 * volumeIntegral
end
```

Gameplay rule: if `material not in player.quark`, never silently downgrade
to a weaker Artisan effect — route to the backlash path (self-damage /
debuff), same as reaching past comprehension anywhere else in this system.

### Master — full eigenbasis (`codex/techniques-master.md` §4.8)

```lua
-- Eq. 4.18 — Full Transmutation: gated on quarkComplete == true, any material
-- Eq. 4.19 — Universal Binding & Decay Control (s = +1 boost/hasten, -1 weaken/arrest)
local function masterBindOrDecay(baseValue: number, s: number, cM: number, fid: number): number
    return baseValue * (1 + s * cM * fid)
end
```

### Warden — perturbative, site-locked (`codex/techniques-warden.md` §4.9)

```lua
-- Eq. 4.20 — only valid within a specific, pre-validated geometry (R_proven)
local function wardenCurvature(eps: number, xi1: number, distanceFromProvenSite: number, rProven: number): number
    if distanceFromProvenSite > rProven then
        return 0 -- outside the validated bump; do not extrapolate
    end
    return eps * xi1 -- * Bump(r, R_proven) shaping, per your VFX/falloff curve
end

-- Eq. 4.21 — pushing eps past eps_valid(R_proven) triggers backlash, not a bigger effect
local function wardenBacklash(epsAttempted: number, epsValid: number, volumeIntegral: number): number
    if epsAttempted <= epsValid then return 0 end
    return (epsAttempted - epsValid) ^ 2 * volumeIntegral
end
```

Design implication: Warden techniques should be implemented as **per-site
unlocks** (a specific door, a specific room, a specific fold-point the
player has "proven" via some in-game validation step), not a general-purpose
spell usable anywhere.

### Sovereign — Overlay Fold / Bound Singularity (`codex/techniques-sovereign.md`)

These are the most state-heavy techniques and the best candidates for a
dedicated module each rather than a single formula:

- **Overlay Fold** (teleport, §4.1–§4.2): implement as a 3-outcome state
  machine keyed on release timing — `fizzle` (released early, harmless),
  `bleed` (released mid-transition, duplicate-image visual at both sites),
  `backlash collapse` (destination badly misjudged / interrupted — apply
  `E_back` damage, Eq. 4.7). Requires the destination's "conformal
  factor" to be known in advance — in game terms, the player must have
  previously visited/scanned the destination, or the fold should be
  disallowed/heavily penalized.
- **Bound Singularity** (gravity well, §4.3): three independently-tuned
  dials — core well (Eq. 4.8), counter-curvature shell (Eq. 4.9), horizon
  lapse tuning (Eq. 4.10). Two distinct failure states: **shell rupture**
  (shell fidelity collapses mid-cast → well "snaps outward", AoE damage
  spike) vs. **horizon migration** (shell reads clean but lapse tuning was
  never validated — a "looks safe, isn't" delayed failure; good candidate
  for a timed/ticking hidden-state hazard rather than an instant one).

### Legend — Sovereign math, held at generational scale (`codex/techniques-legend.md`)

Same formulas as Sovereign; the only game-relevant difference is duration/
domain scale and that upkeep (re-surveying drift, re-inscribing shells) is
the actual gameplay loop, not casting power. Good fit for guild/faction-
owned persistent structures rather than a single-player ability.

### Beyond Legend (`codex/techniques-ascension.md`)

Four paths (Tetrarch/gauge-unification, Demiurge/matter-generation,
Cosmographer/unbounded-geometry, Communion/pooled-comprehension), each with
a "closeness" metric (Eq. 4.24–4.27) that **asymptotically approaches but
never reaches 1**. Treat as unattainable end-game flavor/prestige tracks —
a closeness stat that keeps climbing with no cap-out state — not as a real
unlockable tier. Communion (AS-02) is the one path implementable as
multiplayer co-cast: pool multiple players' `dM` (comprehension sets) for
one combined effect neither could solo (Eq. 4.27).

---

## 5. Failure-mode summary (implement these as three distinct systems)

The Codex is emphatic that fizzle and backlash are *mechanically different*
(`codex/foundations.md` §1.3) — don't collapse them into one "spell fail"
event.

| Failure | Cause | Roblox effect | Source |
|---|---|---|---|
| **Fizzle** | `Fid < Fid_min` (execution too sloppy) | Silent, no cost, no damage — soft VFX at most | Eq. 3.3 |
| **Backlash** | Reaching past comprehension (unsolved channel, wrong eigenvector, `eps` past validated range, misjudged fold destination) | Real damage/debuff to the caster, scaled by the mismatch (`E_back`-style integral) | Eq. 4.7, 4.17, 4.21 |
| **Bleed** | Overlay Fold released mid-transition specifically | Both locations show a duplicate/echo state until it resolves on its own | Eq. 4.6, §4.2 |

Rule of thumb for new spells you design beyond the directory: sloppy but
correct → fizzle; confident but wrong → backlash. Never let a UI or damage
formula blur the two.

---

## 6. Suggested module layout

```
ServerScriptService/
  Aether/
    Comprehension.lua   -- tier derivation, channel unlock checks (§2 above)
    Fidelity.lua         -- Fid computation + Fid_min gate (§3)
    Practice.lua         -- prac(x) tracking, prac_min unassisted gate (§3.4)
    Techniques/
      Novice.lua          -- Eq. 4.0a-4.0e
      Journeyman.lua      -- Eq. 4.13 state machine
      Adept.lua           -- Eq. 4.14-4.15
      Artisan.lua         -- Eq. 4.16-4.17
      Master.lua          -- Eq. 4.18-4.19
      Warden.lua          -- Eq. 4.20-4.21, R_proven site registry
      Sovereign/
        OverlayFold.lua   -- Eq. 4.1-4.7 state machine
        BoundSingularity.lua -- Eq. 4.8-4.12, shell rupture / horizon migration
    Failures.lua          -- Fizzle / Backlash / Bleed as distinct, shared handlers
```

Keep this file (`roblox-reference.md`) as the index back to `codex/` — when
a formula's constants or shape need tuning for gameplay, tune them here or
in code comments, and only touch `codex/` itself if the underlying fictional
mechanic is genuinely changing (per `CLAUDE.md`'s "Extend by appending"
rule, with a changelog entry).
