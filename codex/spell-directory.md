# THE AETHER CODEX — The Spell Directory
### §4.4 The Spell Directory · Eq. 4.0d

*Part of the Aether Codex reference set — see `codex/overview.md` for the file map. All § and Eq. numbers are global across the Codex. The base equations these entries draw on are housed across the technique files: Eq. 4.0a–4.0c, 4.0e in `codex/techniques-novice.md`; Eq. 4.13 in `codex/techniques-journeyman.md`; Eq. 4.14–4.15 in `codex/techniques-adept.md`; Eq. 4.16–4.17 in `codex/techniques-artisan.md`; Eq. 4.18–4.19 in `codex/techniques-master.md`; Eq. 4.20–4.21 in `codex/techniques-warden.md`; Eq. 4.22–4.23 in `codex/techniques-legend.md`; Eq. 4.24–4.27 in `codex/techniques-ascension.md`.*

---

### 4.4 The Spell Directory

§4.0's worked examples (EM, gravity, strong, plus the passive EM read of Eq. 4.0e) were chosen to teach the pattern, not to be exhaustive. This section catalogs named techniques across the Power Hierarchy (§3.3), Novice through the Ascent Beyond Legend — every rank except Sovereign, whose two canonical workings are written up in full in `codex/techniques-sovereign.md` (§4.1–§4.3) rather than catalogued here — as a reference a novel can pull named techniques from without re-deriving mechanics each time. Entries use directory codes (`N-`, `J-`, `AD-`, `AR-`, `M-`, `W-`, `LG-`, `AS-`) rather than Equation Index numbers; they draw on the equations already indexed in §6 and don't need separate global numbering to stay traceable. Adding more later only requires following the pattern already set for that tier.

Read through §1.3, this directory is a map of which channel, or channel-pair, each entry routes through, and nothing more exotic than that. Every Novice and Journeyman entry is a single `delta(F_f)` distortion, or two used in sequence — the sole exception being N-EM-05, a passive read on the `k_EM` channel that sources no distortion at all (Eq. 4.0e); every Adept entry is a single ripple coupling into two gauge channels at once through the joint function `Chi(f1, f2)`, formally defined in Eq. 4.14, which is why Adept techniques are the first in this directory whose fidelity requirement is squared rather than linear — a single sourced ripple has to stay coherent enough to satisfy two coupling channels simultaneously, not one after the other, and a wobble a Journeyman's sequential switching would simply absorb as one weak casting instead degrades both halves of an Adept's blend at once. Every Artisan entry is a `delta(M_op)` distortion restricted to whatever eigenvector that Artisan's signature material actually falls under (Eq. 3.1e, Eq. 4.16) — narrow by construction, for exactly the reason §3.3 already gives. Master entries route through the same `delta(M_op)` channel with a complete `S` behind them (Eq. 4.18–4.19). Warden and Legend entries route through `delta(g)`, narrow and perturbative for the former (Eq. 4.20), the same closed-form Overlay/Singularity mathematics held across a vastly larger domain for the latter (Eq. 4.22–4.23). Ascension entries are historical fragments toward the four paths of §3.3, quantified by Eq. 4.24–4.27.

**Eq. 4.0d — Decay Nudge ("Coaxing a Glow")** *(completing the four-force set begun in §4.0)*
```
Gamma_eff = Gamma_0 * (1 + k_weak * Fid)
P_out = Gamma_eff * E_per_decay * N_unstable
```
The caster nudges the decay rate of trace unstable material already present in most ordinary matter, very slightly upward, for the duration of the casting. `P_out` is the resulting radiant power: each decay of the `N_unstable` unstable nuclei present releases an energy `E_per_decay`, so the nudged rate `Gamma_eff` sets the output directly. `k_weak` is, true to its real-world namesake, the smallest of the four couplings by a wide margin — so even a flawless Novice casting of this equation produces only a faint warmth or the barest visible glow. This is the standard explanation given for why weak-force casters are rare and easy to underestimate at Novice tier: the force is not weak in principle, only in this one narrow, unblended expression of it. It reads very differently once an Adept learns to couple it to something else (Adept tier, below).

#### Novice (Common)

*Electromagnetic (`k_EM`)* — extends Eq. 4.0a.

**[N-EM-01] Spark Draw**
```
V_out = k_EM * Fid * Ae_local
```
A small, controlled static discharge (`V_out`, the discharge potential produced) between the caster's fingers and a target — enough to light kindling, startle, or send a visible signal at range. The first technique most students cast that isn't Eq. 4.0a itself.

**[N-EM-02] Cold Ember**
```
P_in = -k_EM * Fid * Ae_local^2
```
Eq. 4.0a run in reverse: heat is drawn out rather than pushed in. Used for chilling drinks, slowing spoilage over a single evening, or cooling a wagon axle that's started to seize — nothing that would count as preservation at any real timescale.

**[N-EM-03] Lumen Thread**
```
L_out = k_EM * Fid * Ae_local(t)   -- held steady rather than discharged
```
A sustained, low, flameless glow (`L_out`, the luminous output) along a treated wick or thread rather than a single discharge. The caster's main skill here is holding `Ae_local` constant over time instead of releasing it all at once — an early, gentle introduction to sustained casting.

**[N-EM-04] Static Ward**
A faint, continuous repulsive charge held at the skin or on clothing — deflects dust, light debris, and insects. Popular with travelers, archivists, and anyone else who spends their day around things they'd rather not carry home.

**[N-EM-05] Ripple Sense** — Eq. 4.0e.
```
S_detect(x, t) = k_EM * dAe_nearby(x, t)
```
A passive, continuous read on the same `k_EM` channel every other EM technique here actively sources into — the caster notices a nearby working before an ordinary bystander would feel its heat, light, or static. Costs nothing and carries no fizzle or backlash risk (Eq. 4.0e), since nothing is ever sourced; the limitation is purely informational, not mechanical.

*Gravity (`k_grav`)* — extends Eq. 4.0b.

**[N-GR-01] Feather Fall**
```
F_net = m_obj * g_local * (1 - k_grav * Fid),  Fid < 1 by design
```
The same equation as Eq. 4.0b, deliberately undershot — a controlled slow descent rather than full cancellation. Taught before full levitation precisely because undershooting on purpose is safer to practice than aiming for zero and occasionally overshooting into a shove.

**[N-GR-02] Anchor Step**
```
F_net = m_obj * g_local * (1 + k_grav * Fid)
```
The inverse of Eq. 4.0b: a temporary increase in effective weight at the caster's own feet, for better footing on ice, a listing deck, or a narrow ledge in wind.

**[N-GR-03] Light Load**
Eq. 4.0b applied to a carried object rather than the caster — a porter's or packer's trick, and one of the first Novice techniques to see routine commercial use rather than staying purely in a training hall.

*Strong (`k_strong`)* — extends Eq. 4.0c.

**[N-ST-01] Seal Bind**
```
E_bind_eff(x) = E_bind(x) * (1 + k_strong * Fid),  applied only at contact point x
```
Eq. 4.0c narrowed to a single point of contact between two surfaces — rope ends, a cracked seam, torn fibers held together — rather than a whole object's bulk cohesion. Fails safely: a dropped `Fid` just loosens the join rather than fusing it wrong.

**[N-ST-02] Brittle Ease**
```
E_bind_eff(x) = E_bind(x) * (1 - k_strong * Fid)
```
The deliberate inverse of Eq. 4.0c — a small, precise weakening at one point, for a clean split rather than a ragged one. Common among fletchers, coopers, and quarry hands.

*Weak (`k_weak`)* — extends Eq. 4.0d.

**[N-WK-01] Quick Ripen**
Eq. 4.0d's decay nudge applied to already-ripening produce, nudging a process already underway forward by a day or two rather than starting one from nothing. An orchard-keeper's convenience, not a transformation.

**[N-WK-02] Faint Ward-Light**
Eq. 4.0d held at the lowest sustainable output — a dim, steady, personal glow rather than a burst of warmth. The standard "still breathing" marker-light for anyone working somewhere that a torch would be a liability: mines, powder stores, night watches.

#### Journeyman (Common)

A Journeyman holds two or more of the above in closed form without a cross-term connecting them (§3.3) — every entry below is two Novice techniques held without blending: executed in clean sequence, or held as a live either/or choice between them (as in J-03). That distinction is the entire point of the tier, so it's called out explicitly in each write-up rather than left implied. Eq. 4.13 (`codex/techniques-journeyman.md`) formalizes exactly this pattern: disjoint activation windows separated by a switching cost, `tau_switch`. Note that `X_1` and `X_2` in Eq. 4.13 may also be two closed-form techniques drawn from a single `k_f` term (as in J-02 and J-06) — the tier's comprehension requirement is two or more solved terms on the caster's sheet, but the disjoint-window pattern applies to any pair of un-cross-coupled castings, same-force or not.

**[J-01] Ember Handoff** — Eq. 4.0a, then N-GR-03. Heat a coal, then briefly lighten it to toss it accurately. Two separate, complete castings back to back, not one continuous effect.

**[J-02] Ward and Weld** — N-ST-01, then N-ST-02, on different materials in the same working session. A cooper's or fletcher's routine: bind one seam, split one length, never both at once.

**[J-03] Lantern-Keeper's Round** — N-EM-03 or N-WK-02, chosen by available margin rather than blended between. A night-watch specialty precisely because the choice, not a combination, is the skill being exercised.

**[J-04] Porter's Relief** — N-GR-03 on a companion's litter, N-EM-02 on a wagon axle that's started to seize, applied in turn over the course of a journey rather than together.

**[J-05] Two-Handed Smith** — Eq. 4.0a to heat the workpiece, then Eq. 4.0c to set the join, in strict alternation for as long as the work lasts. A guild-standard pairing precisely because an Adept's Flash-Forge (below) replaces it with one technique instead of two.

**[J-06] Watch-Fire Relay** — Eq. 4.0a to relight a signal fire, N-EM-01 for a brief, bright flash where a full fire would be too slow. A chain of watchers relaying a message this way is switching, station to station, never combining.

**[J-07] Bladeline Feint** — N-GR-01, then N-EM-01, drilled by duelists to the smallest `tau_switch` (Eq. 4.13) a Journeyman can sustain: lighten the step mid-lunge, then snap a startling spark at the guard the instant the lightening window closes. The tightness of the gap is the entire training regimen — and precisely how close it can get to zero without ever reaching it is the standing proof the duelist is still Journeyman, not Adept.

#### Adept (Uncommon)

**Eq. 4.15 — Adept Combined Output** *(defined in §4.6, `codex/techniques-adept.md`, where the full derivation lives; restated here for the pattern below)*
```
X_combo = k_f1 * k_f2 * Fid^2 * Chi(f1, f2)
```
`Chi(f1, f2)` (Eq. 4.14) is the cross-coupling function joining two `k_f` terms — the one piece Journeyman tier explicitly lacks (§3.3). Solving it once for a given pair is what promotes a caster from switching between two effects to blending them into a single technique. Fidelity enters squared rather than linearly because both halves of the blend must be held to standard at once; a combination technique punishes sloppy execution harder than either parent effect would alone. There are exactly six unordered pairs among the four forces, and each of the six below is the signature technique built on one of them.

| Symbol | Meaning |
|---|---|
| `Chi(f1, f2)` | Solved cross-coupling function joining forces `f1` and `f2`; absent at Journeyman tier, present at Adept (Eq. 4.14) |

**[AD-01] Flash-Forge** *(EM + Strong)* — heating and cohesion-boosting blended into one continuous pass rather than Two-Handed Smith's two separate steps (J-05). The signature technique of any smith who's made Adept, and usually the reason they're described that way rather than as "a very fast Journeyman."

**[AD-02] Storm-Step** *(EM + Gravity)* — a static discharge and a lightened stance blended into a single short, controlled leap kicked off by the discharge itself. Popular with couriers and scouts for the same reason Ember Handoff (J-01) isn't: no visible gap between the spark and the motion.

**[AD-03] Cinder-Fall** *(EM + Weak)* — heat injection blended with a decay nudge to produce a sustained, low, self-feeding flame from poor fuel — damp wood, old peat. Unglamorous and widely taught to Adept-tier quartermasters precisely because it's useful rather than impressive.

**[AD-04] Sunder Weight** *(Gravity + Strong)* — the inverse of Light Load blended with Brittle Ease: an object made heavier and more fragile in the same casting. A demolition specialist's standard tool.

**[AD-05] Quiet Mend** *(Strong + Weak)* — a cohesion boost blended with Eq. 4.0d run in reverse, slowing rather than hastening decay, to stabilize an already-aging bind — old rope, brittle leather — rather than merely strengthening a fresh one. A preservationist's or archivist's technique, and one of the few Adept combinations built around slowing something down.

**[AD-06] Grave Lantern** *(Gravity + Weak)* — Light Load blended with Faint Ward-Light so a marked object hovers just barely off true rest while glowing faintly. Ceremonial rather than practical; several regional death-rites use a version of this over a grave-marker or a burial buoy.

All six unordered force-pairs are exhausted by AD-01 through AD-06 above — there is no seventh pair among four forces. An Adept's remaining growth from here is depth (`Fid`, practice) on the pairs they hold, solving any of the six they do not yet hold (§4.6 — tier is a per-pair predicate), or reaching for a different channel entirely (Artisan's `delta(M_op)`); what it is never is a brand-new combination beyond the six.

#### Artisan (Uncommon)

Each entry names the specific material an Artisan has solved — the finite subset `S` in Eq. 3.1e — and the narrow, precise work that subset allows. Reaching for a different material with the same confidence is Master-tier work attempted without Master-tier comprehension (§3.3), and fails accordingly. Eq. 4.16 (`codex/techniques-artisan.md`) gives every entry below a shared formal backbone; Eq. 4.17 formalizes the backlash risk of reaching for a material outside `S`.

**[AR-01] Artisan of Salt** — the solved eigenvector governs salt's crystal lattice: precise purification, preservation, or selective dissolution and reformation of salt-based compounds. Does not extend to sugar or quartz, whatever their surface similarity.

**[AR-02] Artisan of Iron** — a solved eigenvector for iron's lattice lets a warped blade be trued or its temper shifted without a forge. Bronze and silver are unmodeled and are not touched.

**[AR-03] Artisan of Bone** — a solved eigenvector for bone's mineral structure, used by menders and, less happily, morticians, to realign or preserve it precisely. One of the more common Artisan specialties in settlements without ready access to a trained surgeon — and, per §3.3, exactly as narrow as every other entry here.

**[AR-04] Artisan of Rot** — not a strengthening eigenvector but a specific, solved decay pathway in organic matter: controlled composting, curing, tanning. A closely guarded trade secret among tanners and vintners rather than a battlefield technique.

**[AR-05] Artisan of Glass** — a solved eigenvector for silica's amorphous structure allows cold reshaping without a furnace. Prized by lens-makers and glaziers, and nearly useless for anything crystalline, since glass's structure is specifically the thing that's been solved.

**[AR-06] Artisan of Ash** — rare, and largely ceremonial: a solved eigenvector for post-combustion residue lets a caster bind ash into a temporary, brittle shape. Associated almost exclusively with funerary sculpture in the few traditions that still practice it.

**[AR-07] Artisan of Clay** — a solved eigenvector for clay's mineral lattice lets a caster drive precise, localized vitrification — true firing without a kiln — via Eq. 4.16, shaping and hardening a vessel wall by wall rather than all at once in a single heat-soak. Porcelain and stoneware bodies are close cousins but unmodeled, and firing them on the strength of clay's `lam_i` risks Eq. 4.17's off-basis backlash rather than a merely uneven glaze.

#### Master (Rare)

A Master's `S` is the complete eigenbasis of `M_op` (Eq. 4.18), so entries below are not tied to one signature material the way Artisan's are. Eq. 4.19 generalizes Eq. 4.0c's cohesion boost and Eq. 4.0d's decay nudge to any target once `c_M` is no longer restricted to a partial `S`.

**[M-01] Full Mend** — Eq. 4.19's binding-energy term applied broadly across living tissue rather than to one bound seam: `E_bind_eff(x)` raised (Eq. 4.19 with `s = +1`) over an entire injury site at once. Where an Artisan of Bone can only realign what their one solved eigenvector covers, a Master's complete `S` lets the same boost reach muscle, vessel, and bone together in a single casting.

**[M-02] Grave Turn** — Eq. 4.19 turned toward reinforcement (`s = -1` on `Gamma_eff` to arrest decay) or hastened aging (`s = +1`) of ordinary matter, rather than the dramatic identity swaps of Eq. 4.18 that Masters are best known for. A quarry-hand's or embalmer's use of the same complete eigenbasis that, wielded through `U_transmute` instead, changes lead to gold — proof the tier's machinery is general-purpose, not spectacle-only.

#### Warden (Very Rare)

Warden techniques are rarely catalogued at all — most Wardens' proofs are tied so tightly to one practitioner's own tested geometry (`R_proven`, Eq. 4.20) that they stay closely-guarded personal results rather than shared or generalized. One representative entry follows.

**[W-01] Threshold Ease** — Applies Eq. 4.20 to a single, specific, previously-mapped threshold (a doorway or gate), briefly reducing the effective weight of crossing it; `R_proven` is that one threshold and no other, and the effect ends abruptly at its bounds. Pushing `eps` past `eps_valid(R_proven)` risks Eq. 4.21's backlash rather than a merely weaker effect.

#### Legend (A Handful Across Recorded History)

Legend entries reuse Sovereign's own mathematics (§4.1–§4.3) unchanged, held across a domain large enough in `R_dom`/`t_dom` to function as a standing, generational feature. See Eq. 4.22–4.23 (`codex/techniques-legend.md`).

**[LG-01] The Standing Fold** — An inhabited, permanent Overlay linking two settlements, built on the unmodified Eq. 4.1 identification and held open across `t_dom_legend`. A hereditary order resurveys B's true conformal factor on a `t_drift` cadence (Eq. 4.22) so `mismatch(Om2)` never creeps `G_dec` toward collapse; the order's real craft is scheduling, not spellwork.

**[LG-02] The Held Star** — A Bound Singularity (Eq. 4.12) maintained for generations as a regional landmark and power source rather than released. Its shell is periodically re-inscribed on a `t_recert` interval (Eq. 4.23) so the residual field `Curv_ext(r)` never rises above background and betrays an uncontained mass at range.

#### Beyond Legend (Historical Fragments)

No character in recorded history has completed a Tetrarch, Demiurge, Cosmographer, or Communion working (§3.3, §3.4) — but partial, documented attempts exist, and Eq. 4.24–4.27 (`codex/techniques-ascension.md`) give each one a checkable closeness metric. The two entries below are historical rather than teachable in the ordinary sense.

**[AS-01] The Four-Fold Feint** — A historical Tetrarch aspirant's signature working, chaining all six solved `Chi(f1,f2)` pairs in tight, unbroken sequence so that EM, weak, strong, and gravitational expression seemed to flow as one force rather than four. Records treat it as proof `Coh_tetrarch` (Eq. 4.24) sat near 1 in the caster's hands — and, in the same breath, as proof that `k_unified` was never actually reached, since the technique still required four couplings performed seamlessly rather than one coupling performed at all.

**[AS-02] The Bound Chorus** — A historical Communion working in which several practitioners pooled their individually-proven `dM_total` into a single acting boundary for one collective casting, reaching an effect no single member's comprehension could have supported alone. Surviving accounts treat it as both the clearest proof `N_comm` (Eq. 4.27) can exceed 1 and a cautionary tale, since what was merged was the provers themselves, not merely their proofs.
