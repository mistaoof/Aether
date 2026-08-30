# THE AETHER CODEX — Applied Techniques: Artisan Tier
### §4.7 Artisan Techniques

*Part of the Aether Codex reference set — see `codex/overview.md` for the file map. All § and Eq. numbers are global across the Codex. The seven named Artisan specialties (AR-01–AR-07) already catalogued in the Spell Directory (§4.4) are formalized by this section's two equations, which extend Eq. 3.1e (`codex/power-hierarchy.md`).*

---

### 4.7 Artisan Techniques

Every Artisan entry in §4.4 has, until now, been described narratively — a named material and a narrow use, with the formal weight carried entirely by Eq. 3.1e's partial diagonalization. That equation establishes *which* eigenvectors an Artisan has solved; it does not by itself say what casting one actually produces, or what happens when a caster reaches past it. The two equations below close that gap, giving AR-01 through AR-07 the same kind of shared backbone that Eq. 4.0a already gives every Novice entry.

**Eq. 4.16 — Eigenvector Draw ("Signature Working")**
```
Effect_i = lam_i * Fid * dAe_local,      e_i in S   (S per Eq. 3.1e)
```
This is the quark-sector channel's version of Eq. 4.0a. Where a Novice's `k_EM` is a single fixed coupling shared by every caster who touches the electromagnetic channel, `lam_i` is not fixed at all — it is the specific eigenvalue an individual Artisan has personally solved for a specific eigenvector `e_i`, and it exists in their working equations only because `e_i` already sits inside their proven `S`. A caster with salt in `S` has a `lam_i` for salt's lattice and nothing else; a caster with iron in `S` has an entirely different `lam_i`, tied to an entirely different `e_i`. The equation's shape is otherwise identical to Eq. 4.0a in every way that matters: `Fid` still scales the outcome linearly, `dAe_local` is still the sourced ripple doing the actual work, and a flawless casting against a low `Fid` still produces a correct but weak effect rather than an incorrect one. AR-01 through AR-07 are seven independent instances of this one equation, each keyed to its own `lam_i` and `e_i`. Nothing about Eq. 4.16 changes when an eighth material joins the catalog — it is the eigenvector entering `S` that does the work of unlocking a technique, not any new mathematics.

**Eq. 4.17 — Off-Basis Extrapolation**
```
E_back_mat = Int_V[ | lam_guess - lam_true |^2 ] dV,      e_guess not in S
```
This is the failure mode Eq. 4.16 cannot produce by construction, because Eq. 4.16 only ever fires for `e_i in S`. Eq. 4.17 fires the moment a caster targets a material whose eigenvector was never solved and proceeds anyway on the strength of a resemblance — bronze reasoned from iron, porcelain reasoned from glass, tallow reasoned from rot. `lam_guess` is the eigenvalue the caster assumes by that analogy; `lam_true` is whatever the real eigenvalue would be, which was never measured because `e_guess` was never in `S` to begin with, and which the caster has no way to know in advance. The ripple goes out shaped for `lam_guess`; the material answers according to `lam_true`; the mismatch between them does not dissipate quietly. It integrates over the working volume as absorbed stress, exactly as Eq. 4.7 describes for an unresolved metric mismatch at Sovereign tier — this is the same backlash mechanism, not an analogous one, expressed through the quark-sector channel instead of the metric-sector channel. That equivalence is the point: §1.3's claim that this reflection-not-dissipation behavior is a universal property of unresolved channel mismatch, rather than something peculiar to the Overlay Fold, is proven precisely by the fact that Eq. 4.7 and Eq. 4.17 are the identical integral applied to two different channels. An Artisan who has never so much as glimpsed `Xi(Ae, g)` can still absorb backlash shaped exactly like a failed fold — smaller in most cases, since a single mismatched lattice rarely stores as much stress as a mismatched region of spacetime, but never zero, and never survivable to extrapolate from twice.

The practical lesson §3.3 already states in prose — that reaching outside a signature material is Master-tier work attempted without Master-tier comprehension — now has a cost attached to it in the same units used everywhere else in this Codex. A guild that trains Artisans trains Eq. 4.16 by widening `S` one eigenvector at a time, and trains against Eq. 4.17 by drilling the discipline of recognizing, before casting, whether a target material's `e_i` was ever actually solved.
