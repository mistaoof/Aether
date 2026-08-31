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

---

### Directory Expansion I (v2.5) — 200 Further Named Techniques

*Added in v2.5. Entry codes continue the numbering above: Novice from N-EM-06 / N-GR-04 / N-ST-03 / N-WK-03, Journeyman from J-08, Adept from AD-07, Artisan from AR-08, Master from M-03, Warden from W-02, Legend from LG-03, Ascension from AS-03. No new global equation numbers — per this section's own convention, entries use directory codes and draw on equations already indexed in §6. Sovereign remains uncatalogued by design (§4.1–§4.3). Distribution is prevalence-weighted to match the §3.3 rarity table: Novice 60, Journeyman 40, Adept 34, Artisan 26, Master 16, Warden 12, Legend 8, Beyond Legend 4. The directory-local notation these entries use (`t_hold`; *reverse-sign casting*) is defined in §5 (`codex/glossary.md`).*

#### How to read this expansion

Everything below follows the rules the original directory already set. Every Novice entry is a single `delta(F_f)` distortion through one solved `k_f` channel (Eq. 1.3), or a passive read that sources nothing. Every Journeyman entry is two closed-form castings held without blending, under Eq. 4.13's disjoint activation windows. Every Adept entry is built on one of the six solved `Chi(f1,f2)` pairs — there is no seventh pair, so every new Adept technique is a deeper working of a pair AD-01 through AD-06 already named, and each entry states its pair. Every Artisan entry names a signature material — one solved eigenvector family in `S` (Eq. 3.1e, 4.16) — and every one of them is exactly as narrow as §3.3 demands. Master entries assume a complete `S` (Eq. 4.18–4.19). Warden entries are Eq. 4.20 confined to one named, proven geometry each. Legend entries are Sovereign mathematics under Eq. 3.1g's scaling, with the maintenance interval (Eq. 4.22–4.23) called out as the operative constraint. Ascension entries are historical fragments, quantified by Eq. 4.24–4.27, and are not teachable in the ordinary sense.

Two notational conveniences recur throughout and are defined once in the Glossary Additions rather than per-entry: `t_hold` (the sustain duration of a held rather than discharged casting) and the term *reverse-sign casting* (a Novice technique that runs its parent equation's distortion in the opposite direction, as N-EM-02 and N-ST-02 already do — a choice of target expression at inscription, never a sign on `Fid` itself, which Eq. 3.2 bounds to `0 <= Fid <= 1`).

---

#### Novice (Common) — 60 entries

*Electromagnetic (`k_EM`)* — extends Eq. 4.0a; passive reads extend Eq. 4.0e.

**[N-EM-06] Kettle's Patience**
```
P_in = k_EM * Fid * Ae_local^2,   Ae_local held deliberately low over t_hold
```
Eq. 4.0a throttled rather than released — a low, even simmer held for as long as the caster maintains the inscription. The cook's counterpart to Lumen Thread (N-EM-03): the skill being trained is a steady `Ae_local`, not a strong one.

**[N-EM-07] Mirror Flash**
A single bright, directional pulse of light — Eq. 4.0a's channel expressed as luminance rather than heat, discharged all at once toward a distant watcher. The standard daytime counterpart to a signal fire, and drilled alongside N-EM-01 in most watch traditions.

**[N-EM-08] Lodestone Touch**
A weak, temporary magnetization impressed on a small iron object — a needle, a nail, a clasp. The effect fades in hours, which is precisely why compass-makers pay for the permanent article and travelers make do with this one.

**[N-EM-09] Chill Locker**
Cold Ember (N-EM-02) held over the interior of a chest or crock for `t_hold` instead of discharged once. Still nothing that counts as preservation at any real timescale — the difference between this and a Master's decay arrest (Eq. 4.19, `s = -1`) is the difference between a cool pantry and a stopped clock.

**[N-EM-10] Glow Mark**
A faint luminous trace left on stone or bark, fading over a night. Trail-markers, mine surveyors, and children playing at being mine surveyors. The mark is a slowly-relaxing field distortion, not a substance — it cannot be scraped off, only outwaited.

**[N-EM-11] Static Comb**
A reverse-sign casting of N-EM-04's held charge: rather than repelling debris from the caster, it strips accumulated static and clinging dust from cloth, parchment, or fleece drawn past the hand. Archivists' guilds teach it in the first month.

**[N-EM-12] Spark Fence**
A treated cord holding a mild N-EM-01 discharge at any point along its length, released on contact. Startles animals and drowsing apprentices equally; hurts neither. The whole cord is one casting — touching it anywhere closes the same inscription.

**[N-EM-13] Ember Coax**
Eq. 4.0a at its gentlest, aimed into a nearly-dead fire's remaining coals. Distinguished from simply casting heat at fresh fuel by economy: coaxing a live ember to spread costs a far lower `Ae_local` than igniting cold wood, which is the entire lesson the technique exists to teach.

**[N-EM-14] Fever Gauge**
A minimal calibrated pulse of Eq. 4.0a into a body or substance, with the caster reading how quickly the injected warmth disperses. Faster dispersal means wetter, denser, or feverish; slower means dry or cold. A physician's and brewer's rule-of-thumb instrument, honest to about the precision of a practiced hand.

**[N-EM-15] Lantern Snuff**
Cold Ember narrowed to a wick — heat pulled from the combustion point until flame can no longer sustain. Cleaner than pinching, safer than blowing, and silent, which is why night-watch curricula pair it with N-EM-03 as a set.

**[N-EM-16] Dew Draw**
A surface chilled below the morning's dew point (N-EM-02 held at low output), collecting drinkable condensate over hours. Yields a cup, not a cistern — but a cup, in the wrong country, has bought this technique its place in every caravan-master's contract.

**[N-EM-17] Dazzle Ward**
Mirror Flash (N-EM-07) turned defensive: a hard, close flash at an aggressor's eyes. Duelists disdain it, because Ripple Sense (N-EM-05) makes it nearly useless against anyone trained — the working announces itself on the `k_EM` channel a beat before the light arrives.

**[N-EM-18] Copper Song**
A small current induced in a closed loop of wire, enough to twitch a needle or sound a tiny bell at the far end of the loop. Estates wealthy enough to run wire between wings use it as a summons; the technique itself is a Novice staple, the wire is the luxury.

**[N-EM-19] Frost Etch**
N-EM-02 focused to a fingertip's breadth, walking a line of frost across glass or polished metal. The frost pattern lasts minutes and marks nothing permanently — glaziers use it to sketch a cut before committing, which is also exactly how casting instructors use it to sketch glyphs.

**[N-EM-20] Hearth Halo**
Eq. 4.0a spread thin across a small room's air rather than concentrated at a point — a few degrees of ambient warmth held for `t_hold`. Inefficient by design; the same `Ae_local` at a kettle would boil it. Taught anyway, because holding a *diffuse* distortion steady is a different skill than holding a concentrated one, and Adept blends will eventually demand both.

**[N-EM-21] Signal Thread**
Lumen Thread (N-EM-03) pulsed rather than held steady — a coded flicker readable at line-of-sight range. Every trade consortium and border garrison maintains its own codebook; the technique is common, the codebooks are what get stolen.

**[N-EM-22] Sun's Patience**
Kettle's Patience (N-EM-06) applied across racks of sliced fruit, fish, or herb over a full day — drying heat, held low and even. One of the highest-`t_hold` Novice castings in common use, and a standard endurance exercise for exactly that reason.

**[N-EM-23] Arc Splice**
Spark Draw (N-EM-01) narrowed to a wire junction, fusing a hair-fine join. The Novice edge of what Flash-Forge (AD-01) does wholesale: no cohesion boost accompanies the heat, so the join holds by melt alone and a jeweler's version of this remains honest work rather than a blend.

**[N-EM-24] Gleam Lure**
A hovering point of soft light held just above water or among stubble — fish rise to it, moths mob it, and both end up in somebody's basket. Fisherfolk's guilds in three river systems independently claim to have invented it, which probably means nobody did.

**[N-EM-25] Quiet Coil**
A reverse-sign damping held around a delicate instrument — lodestones, fine balances, another caster's inscription-in-progress — suppressing ambient static and stray field noise. The rare Novice technique whose customers are mostly other casters.

*Gravity (`k_grav`)* — extends Eq. 4.0b.

**[N-GR-04] Steady Hand**
Light Load (N-GR-03) at the scale of a single held tool — a scalpel, a brush, an engraver's burin made a fraction of its weight so a tremor moves less mass. Surgeons and forgers of documents prize it equally, a pairing moralists have gotten essays out of for generations.

**[N-GR-05] Level Set**
Anchor Step's increase (N-GR-02) applied to a plumb bob or spirit level, settling its swing in a breath instead of a minute. A surveyor's convenience — and, drilled for speed, a common first exercise in casting on a *moving* target.

**[N-GR-06] Soft Landing**
Feather Fall (N-GR-01) cast on falling cargo rather than a falling person. Harder than it sounds: the caster is not riding the object, so range and timing must both be judged from outside. Dockworkers' guilds test it with crockery, publicly.

**[N-GR-07] Counter Sway**
Anchor Step held on a vessel's keel-line in a swell, damping roll. The weight increase is modest; what steadies the boat is that it is *constant* while the water is not. Ferry crews rate a caster by how long they can hold it, not how hard.

**[N-GR-08] Ridge Step**
Light Load on the caster's own body, held across a climb rather than discharged per-stride. The deliberate complement to Feather Fall: one manages a fall, the other prevents it. Mountain couriers run both as a single drilled sequence — which makes those couriers, formally, Journeymen the day the sequence becomes their habit.

**[N-GR-09] Cart's Mercy**
Light Load on a mired wheel at the moment the team heaves. Timing is the entire technique — a lightened wheel and an unready team accomplishes nothing, which makes this the canonical example in casting schools of a flawless `Fid` wasted by bad coordination.

**[N-GR-10] Well Draw**
Light Load held on a filled bucket for the length of its rise. Utterly unremarkable, universally taught, and by head-count likely the most-cast gravity technique in the world — a standing reminder that the median use of aether is chores.

**[N-GR-11] Ballast Word**
Anchor Step on one gunwale, cast and released on a coxswain's call, trimming a hull through a turn. Racing crews treat the caster as a crew position with its own seat and its own verb: to *ballast*.

**[N-GR-12] Firm Table**
Anchor Step's increase applied to a workpiece instead of the caster — the object clamps itself to the bench under its own borrowed weight. Woodworkers use it where a vise would mar the piece; casting instructors use it because a *still* target is the kindest possible fidelity drill.

**[N-GR-13] Gentle Toss**
Light Load on a thrown line, bag, or grapnel for the first half of its arc, released midflight so it lands true. The release timing is the training value: letting go of a casting cleanly, mid-effect, is a skill Novices otherwise reach Journeyman without acquiring.

**[N-GR-14] Restful Weight**
Anchor Step at its mildest, spread across a blanket — the pressure of a heavy quilt from an ordinary one. Sanatoriums and nurseries keep a caster on retainer for it. Among the least dramatic entries in this directory, and among the most requested.

**[N-GR-15] Snow Shed**
Light Load across a roof's snow burden while crews work beneath, cast from the ground in sections. The load is lightened, never lifted — a distinction every winter-country guild drills, because an overshot casting that *lifts* the pack sends it down all at once when the hold ends.

**[N-GR-16] Ford Keeper**
Anchor Step held on the caster's own steps across a current. The river pushes; the crosser simply weighs more than the push. Larger parties cross roped to the one caster holding it, which is why river-guides in fording country are casters by default.

**[N-GR-17] Hawk's Lend**
Light Load on a messenger bird for its first climbing seconds off the glove. The bird gains launch height; the effect must end before the bird leaves range. Falconers argue endlessly about whether it helps enough to justify unsettling the animal, which is to say: it is traditional.

**[N-GR-18] Mason's Third Hand**
Light Load on a stone through the final hand-span of its placement — not the lift, the *setting*, where fingers would otherwise be. Masons' guilds credit it with more saved hands than any physician, and apprentice it accordingly.

*Strong (`k_strong`)* — extends Eq. 4.0c.

**[N-ST-03] Edge Hold**
Seal Bind's boost (N-ST-01) laid along a cutting edge, resisting the rolling and dulling of a day's work. The edge is not sharper — it is merely *still sharp* at dusk. Harvest crews hire it by the field.

**[N-ST-04] Green Split**
Brittle Ease (N-ST-02) run down a billet's grain-line before the maul falls. Firewood splits true; knots surrender ungracefully but surrender. The most commercially common strong-force casting in cold country.

**[N-ST-05] Knot Faith**
Seal Bind at the crossings of a tied knot — the knot holds against loads that would walk it loose, yet unties by hand when the casting lapses. Riggers value the *reversibility* over the strength; a fused knot is just a lump.

**[N-ST-06] Patch Press**
Seal Bind holding a patch to a hull, boot, or bellows seam while proper repair waits for shore, bench, or morning. Explicitly a promise to fix something later — several harbor authorities require patched hulls to carry proof of a standing repair contract for exactly this reason.

**[N-ST-07] Chisel's Consent**
Brittle Ease a finger's width ahead of a chisel line in stone or hardwood. The material parts where asked and nowhere else. Carvers describe the sensation as the workpiece *agreeing* — the directory records the phrasing because every carving tradition independently arrives at it.

**[N-ST-08] Thread Lock**
Seal Bind at a screw's threads, a peg's seat, an axle pin. Holds against vibration that would back the fastener out; releases to a deliberate hand on the tool. Wainwrights cast it as routinely as they grease.

**[N-ST-09] Shatterguard**
Eq. 4.0c across a glass vessel, a fired pot, a lens — held for the duration of a transport. A dropped crate still breaks; a *jostled* one doesn't. Carriers price fragile freight with and without a caster riding along, and the difference is the technique's market value, published quarterly.

**[N-ST-10] Clean Break**
Brittle Ease at an old, badly-healed fracture so a mender can re-break precisely where intended rather than where the bone prefers. Cast only ever alongside a mender's direct instruction; the technique is Novice, the judgment of *where* is not, and every guild charter that mentions this entry says so.

**[N-ST-11] Miller's Mercy**
Brittle Ease across grain hulls at the millstone's mouth — flour from less force, less heat, fewer burnt batches. Millers who employ a caster advertise it; customers taste the difference or claim to.

**[N-ST-12] Supple Hand**
Brittle Ease at its gentlest, worked through stiff leather, dried rope, or a rusted hinge's seized grain. Loosens what disuse has hardened without weakening what should hold. The restorer's counterpart to N-ST-01, and cast with the same touch.

**[N-ST-13] Anchor Bite**
Seal Bind into the soil gripping a stake, piton, or fence post — the ground itself briefly bound around the shaft. Ends, like all of these, when the casting ends; a camp that stands a season is held by dug anchors, not held breath.

**[N-ST-14] Mortar's Reprieve**
Seal Bind across frost-cracked mortar or a split lintel, buying a wall the weeks between discovery and repair. Building wardens keep ledgers of standing reprieves precisely because the technique is good enough to invite forgetting — the directory notes, without comment, that every such ledger has at least one entry older than its warden.

**[N-ST-15] Quarry Line**
Brittle Ease cast point by point along a scribed line across rock — each point a separate, complete casting, the line parting under wedges where it was eased. A patient Novice splits stone a gang of hammers couldn't; an *impatient* one learns why the points are cast separately.

**[N-ST-16] Barrel True**
Seal Bind at a hoop's seat while the cooper drives it home, then released — the bind holds the stave-line true during the set, and the finished barrel holds by craft alone. A signature example of aether as a *tool of* a trade rather than a replacement for it.

**[N-ST-17] Wheelwright's Weld**
Seal Bind clamping a felloe joint or chair joint while glue cures — hours of `t_hold` at trivial intensity. Workshops schedule these castings the way they schedule the glue, and apprentice casters bill by the drying afternoon.

*Weak (`k_weak`)* — extends Eq. 4.0d. The couplings here remain, per that equation's write-up, faint by nature at this tier; every entry below is honest about it.

**[N-WK-03] Slow Larder**
Eq. 4.0d as a reverse-sign casting — the decay nudge run *downward*, slowing spoilage by a margin measured in extra days, not seasons. The pantry-scale ancestor of what Quiet Mend (AD-05) blends and Eq. 4.19 (`s = -1`) perfects; the family resemblance is the standard lecture example for how one channel deepens across four tiers.

**[N-WK-04] Hearthstone**
A smooth stone nudged to a faint, steady warmth (Eq. 4.0d held low), wrapped in flannel at the foot of a bed. Output a candle would mock; comfort a candle can't match, since it cannot gutter, tip, or burn a sleeping child. The signature domestic casting of weak-force households.

**[N-WK-05] Assayer's Glow**
Eq. 4.0d cast across a spread of crushed ore — fractions bearing trace unstable material answer with a faint luminescence, and the assayer reads the sparkle like a map. One of the few Novice techniques that meaningfully *prospects*, and the historical reason weak-force casters cluster in mining towns.

**[N-WK-06] Compost Quicken**
Quick Ripen's logic (N-WK-01) turned on a heap rather than an orchard row — decomposition already underway, nudged. A season's soil in most of one. Estate gardeners consider it beneath discussion and cast it weekly.

**[N-WK-07] Mourner's Candle**
Faint Ward-Light (N-WK-02) formalized for a vigil: one caster, one night, one steady glow that cannot blow out. Several funerary traditions hold that the light must be *held*, not merely lit — the point being the attendance, which a lamp cannot offer.

**[N-WK-08] Deep Mark**
Ward-light worked into mineral-rich cave paint, leaving marks that answer a later caster's nudge with a soft glow. Cavers' guilds blaze routes in it; the marks outlast the guilds, and mapping dead guilds' marks is its own small profession.

**[N-WK-09] Leak Finder**
A trace of nudge-responsive mineral salt fed into a water line or millrace, then followed by its faint glow to wherever the flow escapes. Aqueduct wardens' standard diagnostic, and the technique most often cited when someone argues weak-force casting is underrated.

**[N-WK-10] Long Watch**
Faint Ward-Light rebalanced for duration over brightness — output near the resolution threshold (Eq. 3.3), hold measured in full nights. The endurance benchmark for weak-force Novices, as Sun's Patience (N-EM-22) is for their EM peers.

**[N-WK-11] Salamander's Breath**
Hearthstone's warmth cast directly into a bedroll, boot, or glove for the minutes it takes to stop shivering. Border sentries call the technique by this name in six languages; the directory declines to rule on which came first.

**[N-WK-12] Miller's Clock**
A pinch of nudge-responsive salt in a sealed vial, its glow decaying at a known rate once nudged — a crude, unstealable timer for processes that outlast attention: proofing dough, steeping dye, a rented hour. Accurate to about a tenth; disputed at the margins in every market that uses it.

#### Journeyman (Common) — 40 entries

*Every entry below is two closed-form castings held without blending — executed in clean sequence or as a live either/or — under Eq. 4.13's disjoint activation windows and `tau_switch`. As with the original seven, the switching discipline is the technique; the components are all Novice.*

**[J-08] Harvest Round** — N-ST-03 on the scythe at dawn, N-EM-22 on the racks at noon. A single caster carries a farm's cutting and drying through harvest by never once trying to do both at once.

**[J-09] Ferryman's Habit** — N-GR-07 in the crossing, N-GR-16 at the landing, switched as the deck empties. Same force, two closed forms — the pairing that most often teaches a Journeyman that Eq. 4.13 doesn't care whether the two windows share a `k_f`.

**[J-10] Surgeon's Table** — N-GR-04 on the instrument, then N-ST-10 at the mender's word, never overlapping — the hand must be steady *before* the bone is eased, and the sequence is legally fixed in three guild charters.

**[J-11] Glazier's Morning** — N-EM-19 to sketch the cut, N-ST-02 to make it. Frost line, then brittle line, in strict order; reversing them ruins the pane and is the trade's standard joke about impatient apprentices.

**[J-12] Winter Doorstep** — N-EM-20 held indoors *or* N-WK-04 sent to the beds, chosen nightly by fuel, weather, and who's home. A householder's version of J-03's either/or discipline.

**[J-13] Prospector's Walk** — N-WK-05 across the spread, then N-ST-15 along the seam it reveals. Read, then split; the assay window closes before the quarry window opens.

**[J-14] Dockmaster's Pair** — N-GR-06 over the swinging crate, N-ST-09 on the fragile one — never both on one load, because a load that needs both needs a better crane.

**[J-15] Night Fisher** — N-EM-24 to raise the shoal, N-GR-13 to lay the net's throw long. Lure, then cast; the lure dies the moment the net flies, which the fish appear not to have learned in several centuries.

**[J-16] Courier's Descent** — N-GR-08 up the ridge, N-GR-01 down the scarp. The mountain courier's canonical pair, and the worked example most curricula use for drilling `tau_switch` under fatigue.

**[J-17] Physician's Round** — N-EM-14 to read the fever, N-EM-02 to ease it. Gauge, then chill, in alternation through the night — a discipline built on never trusting the last reading through the current casting.

**[J-18] Archivist's Bench** — N-EM-11 across the folio, then N-ST-12 through its cracked spine. Clean, then soften. The reverse order grinds loosened grit into the leather, a mistake each archivist is permitted exactly once.

**[J-19] Stable Fire Drill** — N-EM-15 on the lamp, N-GR-14 across the spooked animal. Snuff, then settle. Written into stable standing orders in most walled towns, in that order, in large letters.

**[J-20] Wall Warden's Round** — N-ST-14 on the crack at morning, N-WK-09 through the cistern line at noon. The maintenance Journeyman's archetype: two small competences, held honestly apart, worth more than either doubled.

**[J-21] Smith's Apprentice Round** — N-EM-13 to wake the forge, N-GR-12 to pin the work. The pairing traditionally assigned the year before Two-Handed Smith (J-05), and the reason that year exists.

**[J-22] Lens-Grinder's Sequence** — N-ST-09 while the blank travels, N-EM-19 to mark the grind. Guard window closed, mark window opened, no overlap — an heirloom sequence in workshops that cannot afford one dropped blank.

**[J-23] Vintner's Cellar Round** — N-WK-06 at the press-waste heap, N-WK-03 over the must. Hasten one decay, slow another, same force, opposite signs, and a cellar-master's entire reputation living in never confusing the targets.

**[J-24] Siege Porter** — N-GR-18 setting the stone, N-ST-13 binding the stake-line. The field-works pairing; drilled to a called cadence so a wall crew's several Journeymen switch on the same beat.

**[J-25] Beacon Chain** — N-EM-07 by day *or* N-EM-21 by night, chosen by light and weather — J-06's relay discipline with the choice itself formalized as the skill.

**[J-26] Falconer's Launch** — N-GR-17 off the glove, then N-EM-24 held far afield to mark the lure point. Bird lightened, then light raised; the windows must not touch or the bird chases the wrong brightness.

**[J-27] Ropewalk Round** — N-ST-05 proving the knots, N-ST-01 sealing the whipped ends. A rigger's same-force pair, examined annually in every harbor that licenses one.

**[J-28] Icefield Crossing** — N-GR-02 on the crosser's own steps, N-GR-06 held ready over the sledge. The second window opens only if the first fails — a *contingency* pairing, and most curricula's first example of holding a casting in reserve rather than in effect.

**[J-29] Kiln Watch** — N-EM-06 through the long soak, N-EM-14 at the hour-marks. Hold, gauge, hold again; the gauge pulse cannot read truly while the heating window is open, which is the whole lesson.

**[J-30] Orchard Round** — N-WK-01 along the early rows, N-GR-13 lofting sacks to the cart. The picking crew's pairing, unremarkable everywhere fruit is grown, which is the point of cataloguing it.

**[J-31] Tinker's Call** — N-EM-18 to ring ahead, N-GR-10 at the well when the work is watering. An itinerant's pairing chosen for breadth of custom rather than depth of either.

**[J-32] Quarry Foreman's Day** — N-ST-15 along the line, then N-GR-15's sectional lightening as the block walks the ramp. Split window closed before lift window opens; the trade's oldest safety verse says so in rhyme.

**[J-33] Night Nurse's Round** — N-WK-04 to the beds, N-WK-10 at the door. Warmth, then watch-light, resumed in alternation through the dark — the humblest entry in this directory's Journeyman tier and, by any honest count of castings performed, its most practiced.

**[J-34] Carpenter's Close** — N-ST-17 clamping the joint, then N-ST-08 locking the pegs once dry. Same force, sequential by necessity: the glue's schedule, not the caster's, sets `tau_switch`'s floor — a favorite exam question.

**[J-35] Harbor Light Relay** — N-EM-03 in the tower *or* N-WK-02 on the buoy-line, chosen by fog. The keeper's either/or; on the worst nights the choice reverses hourly, and the log of choices is the keeper's real deliverable.

**[J-36] Drover's Ford** — N-GR-16 while wading the herd, N-EM-12 strung at the far bank's pen. Cross, then fence. Held apart because a spark anywhere near a mid-river herd is a lesson no drover needs twice.

**[J-37] Engraver's Sitting** — N-GR-04 on the burin, N-EM-25 around the plate. Steady the hand, quiet the field, in alternation as the work demands — a pairing whose customers, like Quiet Coil's, are mostly other casters.

**[J-38] Storm Prep Round** — N-ST-06 over the seams, N-GR-11 to trim her as the crew works. The pre-gale checklist pairing; every harbor's version differs and every harbor is certain theirs is canonical.

**[J-39] Assay Office Sequence** — N-WK-05 across the sample, N-EM-14 into the suspect fraction. Glow to find it, pulse to weigh its wetness — two *reads* in sequence, the directory's cleanest example that Journeyman discipline governs information-gathering castings as strictly as forceful ones.

**[J-40] Bellringer's Feint** — N-EM-18 to sound the far bell, then N-GR-01 stepping off the tower stair's worn edge. A sexton's pairing in old towers; drilled, like Bladeline Feint (J-07), to the smallest `tau_switch` its holder can survive being wrong about.

**[J-41] Foundling's Kit** — N-EM-01 *or* N-WK-11, chosen by what the night needs lit or warmed. The classic first pairing of self-taught casters, catalogued precisely because it appears independently, everywhere, in exactly this form.

**[J-42] Paper-Maker's Day** — N-EM-22 over the drying felts, N-ST-12 through yesterday's brittle sheets. Dry the new, ease the old; the windows are half a workshop apart and still, formally, disjoint.

**[J-43] Sapper's Discipline** — N-ST-02 at the marked stone, N-EM-05 held *between* castings, listening for another crew's work through the wall. Ease, then listen; the passive read costs nothing (Eq. 4.0e) but attention, and the discipline of actually stopping to spend it is the entry.

**[J-44] Ostler's Evening** — N-GR-14 across the tired animal, N-WK-04 in its water trough against the frost. The pairing that keeps coaching inns' beasts sound through winter, and ostlers' guilds in dispute with casters' guilds over whose members it belongs to.

**[J-45] Toll Keeper's Test** — N-EM-14's pulse into a suspect cask, then N-ST-01 re-sealing the tap-hole. Excise work: read, then reseal, leaving no sign — the directory notes that both windows also open in the *smuggler's* version, in the other order.

**[J-46] Winter Mason's Pair** — N-EM-20 held around the curing mortar, N-ST-14 across yesterday's frost damage. Warm the new work, hold the old; cold-country building seasons are two castings longer than they used to be.

**[J-47] Rescue Line** — N-GR-13 sending the rope long, then N-GR-16 as the hauler sets their feet. Throw light, stand heavy — drilled by every river-rescue watch to a called two-beat, because in the water between the two windows is somebody's neighbor.

#### Adept (Uncommon) — 34 entries

*There is no seventh pair. Every entry below is a deeper working of one of the six solved `Chi(f1,f2)` pairs already named in AD-01 through AD-06, and states its pair; all follow Eq. 4.15's combined-output form, with fidelity entering squared for the reason §4.6 derives. Within each pair, entries are ordered roughly from trade to battlefield.*

*(EM + Strong — the Flash-Forge pair, AD-01)*

**[AD-07] Annealing Breath** *(EM + Strong)* — heat and a *gentle* cohesion ease blended, walking a stressed metal's grain back to softness in one pass. Flash-Forge's mirror image: where AD-01 joins, this relaxes. Toolmakers who hold both describe them as one technique with a sign choice.

**[AD-08] Glasswright's Kiss** *(EM + Strong)* — localized heat and a cohesion boost held at a crack's tip, healing a glass flaw without slumping the pane. The blend exists because sequential casting fails here: heat alone spreads the crack in the gap before a second casting could bind it — `tau_switch` is precisely the technique's enemy, which makes it the standard demonstration that Adept tier is a different *kind* of casting, not a faster Journeyman.

**[AD-09] Coldwright's Temper** *(EM + Strong)* — deep chill (Eq. 4.0a reversed) blended with a cohesion boost, setting a hardened edge without a quench-bath's warp. Smithing traditions that hold AD-01 and AD-09 both speak of *fire-write* and *frost-write* as the pair's two hands.

**[AD-10] Breachwright's Answer** *(EM + Strong)* — heat and brittleness driven together into a lock, hinge, or grate: the metal is hot *and* frangible in the same instant, and one blow does the rest. The pair's siege expression, licensed accordingly almost everywhere.

**[AD-11] Solder Line** *(EM + Strong)* — Arc Splice's heat blended with Seal Bind's grip, running a continuous sealed seam along a boiler course or still-pipe in one inscription. The industrial workhorse of this pair; entire manufactories are laid out around how far one Adept can walk a seam before `Fid^2` sags.

**[AD-12] Cooper's Furnace** *(EM + Strong)* — steam-bending heat and a grain-line cohesion ease blended along a stave or rib, curving seasoned wood in one dry pass with no steam box and no springback. The shipwright's and cooper's shared prize; yards that retain a holder bend frames to curves their rivals' molds cannot draw.

*(EM + Gravity — the Storm-Step pair, AD-02)*

**[AD-13] Crane Whisper** *(EM + Gravity)* — a signal pulse and a lightening blended so the load lightens *on* the signal, in the same casting, across a work yard. What J-14 does with two windows, one Adept does with none; dock guilds bill the difference by the hour.

**[AD-14] Beacon Vault** *(EM + Gravity)* — Storm-Step's leap blended with Mirror Flash's pulse: the courier's arrival *is* the signal. Border relays built around one Adept replace a tower's worth of Journeyman watchers, which is why border lords count Adepts the way they count cannon.

**[AD-15] Lightning Draw** *(EM + Gravity)* — a discharge blended with a lateral pull on the discharge path itself, bending a spark around cover to a target the caster cannot see straight. The duel-legal ceiling of this pair in most codes; the duel-*illegal* extensions are the same casting with worse intentions.

**[AD-16] Feather Barrage** *(EM + Gravity)* — thrown objects lightened in flight and given a static crackle that spooks and scatters — a crowd-control blend built to end brawls without ending brawlers. City watches teach it as their signature Adept technique; city watchmen mostly never make Adept, which keeps its holders employed.

**[AD-17] Lampfall** *(EM + Gravity)* — a hovering glow-point lowered smoothly down a shaft ahead of the descending crew, light and lift as one held blend. Mine rescue's standard-bearer technique, and the entry most often cited when a guild argues an Adept's wage.

**[AD-18] Stormglass Reading** *(EM + Gravity)* — a diffuse static read and a fine sounding-pull blended across the sky's near column: pressure, charge, and the *weight* of coming weather from one held casting. The pair's quiet scholarly face; harbor pilots trust a holder's morning over any instrument they own, and say so in their logs.

*(EM + Weak — the Cinder-Fall pair, AD-03)*

**[AD-19] Forge From Nothing** *(EM + Weak)* — Cinder-Fall pushed to its working limit: a self-feeding heat sustained on fuel so poor it barely deserves the name — wet peat, green wood, bilge scrap. Expedition quartermasters rank it above any weapon this pair offers, and the directory declines to argue.

**[AD-20] Watchman's Dawn** *(EM + Weak)* — ward-light's steadiness blended with lamplight's brightness: a glow that cannot gutter *and* genuinely lights the yard. The night-watch blend that retires J-35's either/or, in the towns that can hire it.

**[AD-21] Assayer's Lens** *(EM + Weak)* — the decay-glow read and a calibrated heat pulse blended into one probing casting: composition *and* wetness from a single touch. Turns N-WK-05 and N-EM-14's two windows (J-39) into one instrument; mints and mine offices treat holders as senior staff on arrival.

**[AD-22] Slow Match** *(EM + Weak)* — a heat point and a decay nudge blended into a self-timing ignition — a fire that starts *later*, by a chosen interval, with no fuse to see or cut. Sappers' guilds keep its deeper calibrations off the open directory, and this entry respects that.

**[AD-23] Kilnless Fire-Gilding** *(EM + Weak)* — a heat gradient and a decay nudge blended through a glaze or gilt layer, curing in minutes what a kiln cures in a day, with no kiln to crack the piece. Restorers' workshops guard their holders jealously; AR-27's porcelain state guards its own more jealously still.

**[AD-24] Hearth Eternal** *(EM + Weak)* — Cinder-Fall's self-feeding logic inverted into pure endurance: a banked civic fire blended to draw so little that one charge of fuel warms a hall through a winter's siege. The blend behind three cities' famous "undying" hearths — undying, the directory notes, in exact proportion to their Adepts' renewal calendars.

*(Gravity + Strong — the Sunder Weight pair, AD-04)*

**[AD-25] Mason's Miracle** *(Gravity + Strong)* — a stone lightened *and* cohesion-boosted through placement: half its weight and twice its patience with handling, in one blend. What N-GR-18 and N-ST-09 do apart, this does whole; cathedral works measure their schedules in how many holders of it they can retain.

**[AD-26] Controlled Fall** *(Gravity + Strong)* — Sunder Weight's demolition blend refined for *direction*: the target made heavier and selectively brittle so it fails along a chosen line and drops where told. The difference between demolition and catastrophe, per every guild examiner's opening lecture.

**[AD-27] Bulwark Set** *(Gravity + Strong)* — a barricade's timbers weighted and bound in one casting — heavier to move, harder to break, for as long as the Adept holds. Siege defense's mirror to AD-10; fortress rosters list holders of both under one heading: *gatewrights*.

**[AD-28] Wrecker's Mercy** *(Gravity + Strong)* — a collapsing structure's fragments lightened and toughened mid-fall, so what lands, lands soft and whole. The rescue blend of a demolition pair — the directory's standing example that a pair's moral character belongs to its caster, not its `Chi`.

**[AD-29] Anchor Absolute** *(Gravity + Strong)* — a ship's anchor weighted and its cable's grip bound as one blend through a blow. Harbormasters in storm latitudes retain one Adept for this the way they retain one pilot, and for the same nights.

**[AD-30] Avalanche Writ** *(Gravity + Strong)* — a loaded slope's snowpack made locally heavier and more frangible on a chosen line, releasing the slide at a chosen hour onto an emptied path. Sunder Weight turned to prevention; high-country districts post the writ's schedule beside the church door, and attendance at both is customary.

*(Strong + Weak — the Quiet Mend pair, AD-05)*

**[AD-31] Reliquary Seal** *(Strong + Weak)* — Quiet Mend deepened to institutional scale: an object's binds boosted and its decay slowed as one standing blend, renewed on a calendar. Archives and reliquaries keep *seal-books* recording each renewal — the humble ancestor, several lecturers note, of the recertification ledgers Legend tier lives by (Eq. 4.23).

**[AD-32] Surgeon's Hold** *(Strong + Weak)* — tissue's cohesion boosted and its decay arrested together at a wound too grave to close — a blend that buys hours at the edge of what Novice and Journeyman menders can buy at all. Not healing: *time*. Every tradition that holds it says those words in its oath.

**[AD-33] Ship-Biscuit Blessing** *(Strong + Weak)* — provisions' binds toughened and spoilage slowed in one hold-wide casting before a long passage. Unglamorous even by this pair's standards, and the blend most often named in shipping contracts by its plain effect: *the cargo arrives*.

**[AD-34] Rot-Fence** *(Strong + Weak)* — the pair run in *opposed* signs: decay hastened in a blighted limb of an orchard row while the healthy wood's binds are boosted against its spread. The blend's judgment burden — where the fence falls — is the entry's real difficulty, and the reason orchard wardens who hold it sit on rural courts.

**[AD-35] Tanner's Secret** *(Strong + Weak)* — a hide's decay pathway nudged while its fiber binds are held — controlled cure in days, supple as months. The trade blend AR-04's eigenvector work resembles from the outside; the two are routinely confused, and both trades profit from the confusion.

**[AD-36] Seed Writ** *(Strong + Weak)* — seed-stock's coats bind-boosted while dormancy's slow decay is arrested, one granary-blessing casting holding a district's next planting viable across a failed year. AD-33's logic pointed at the year after this one; famine-country traditions rank its holders above physicians, and physicians there agree.

*(Gravity + Weak — the Grave Lantern pair, AD-06)*

**[AD-37] Vigil Bier** *(Gravity + Weak)* — Grave Lantern held at procession scale: the bier lightened to its bearers and lit with a steady ward-glow across the whole rite. The ceremonial pair's ceremonial deepening; several traditions hold that the casting must be one Adept's alone, unrelieved, and that the fatigue is part of the observance.

**[AD-38] Deep Sounding** *(Gravity + Weak)* — a glow-traced weight lowered on a blended casting down a shaft, well, or wreck — depth read from the descent, condition from the glow's return. The surveyor's expression of a funerary pair, and proof, cited in every lecture on this pair, that no pair is only what its signature suggests.

**[AD-39] Beacon Buoy** *(Gravity + Weak)* — a marker held just off true rest and lit with unquenchable ward-light, riding a reef or bar through weather that would drown any lamp. Coastal charities fund holders of this blend the way inland towns fund bridges.

**[AD-40] Lightened Watch** *(Gravity + Weak)* — a sentry's own body faintly lightened and faintly lit — steps silent on old floors, presence marked to allies by a glow only Ripple Sense reads at range. The pair's one martial expression, favored by honest garrisons and dishonest guests in exactly equal measure.

#### Artisan (Uncommon) — 26 entries

*Each entry names a signature material — one solved eigenvector family in `S` (Eq. 3.1e), worked through Eq. 4.16 — and is exactly as narrow as §3.3 requires. The neighboring materials each entry pointedly does not cover are listed in the tradition of AR-01 through AR-07; every one of them is an Eq. 4.17 backlash waiting on a caster who reasons by resemblance.*

**[AR-08] Artisan of Copper** — a solved eigenvector for copper's lattice: cold-drawing true wire, healing verdigris pitting, tuning a bell's voice by grain. Bronze — *mostly copper*, as every examiner sighs — is an alloy with its own unsolved eigenvector, and the classic Eq. 4.17 cautionary example in metals guilds.

**[AR-09] Artisan of Silver** — solved for silver's lattice: mirror-finishing without polish, closing hairline cracks in plate, drawing filigree no hand-tool matches. Tarnish removal is the trade's bread; the directory notes it is the *lattice* being trued, not the tarnish addressed — sulfur is somebody else's eigenvector.

**[AR-10] Artisan of Gold** — solved for gold's lattice: beating leaf past any hammer's thinness, seamless joins in regalia, assay-grade surface truth. The rarest metals specialty not for difficulty but economics — patrons who can fund the eigenvector's proving already own the gold, and guard both accordingly.

**[AR-11] Artisan of Tin** — solved for tin's lattice, including its cold-weather gray-rot, which a holder can arrest or *induce*. The induced form once collapsed a ducal treasury's plate stock in a winter, which is why this modest eigenvector appears in three kingdoms' espionage statutes.

**[AR-12] Artisan of Bronze** — solved for one bronze — a specific casting-alloy ratio, proven as its own eigenvector. Bell-founders' orders hold it closely. The directory stresses what §4.7 requires it to: this eigenvector covers *that ratio*, and a neighboring bronze is Eq. 4.17's problem, not a discount.

**[AR-13] Artisan of Oak** — solved for oak's grain structure: seasoning decades into weeks, truing warped beams, reading — and steering — how a trunk will split. Shipwrights' yards bid for holders by name. Elm, ash, and pine are separate trees, separate eigenvectors, separate careers.

**[AR-14] Artisan of Paper** — solved for felted cellulose: mending tears fiber-to-fiber, lifting foxing, splitting a sheet into two whole leaves. Archives employ them; forgers court them; the guild examination, notoriously, includes an ethics paper — on paper the candidate must first mend.

**[AR-15] Artisan of Ink** — solved for one iron-gall formulation's bound structure: fixing fading script, lifting chosen strokes cleanly, aging a fresh line — or *proving* one aged. Courts in four jurisdictions seat one as an examiner of documents; courts in the other jurisdictions wish they could.

**[AR-16] Artisan of Wool** — solved for wool's fiber structure: felting without labor, un-shrinking a ruined garment, weatherproofing a cloak's weave as a lattice property rather than a grease. The homeliest eigenvector in the directory and, by guild membership rolls, the most widely held.

**[AR-17] Artisan of Silk** — solved for silk's protein lattice: reweaving tears invisibly, tuning drape and sheen, proofing thread against rot on the loom. Sericulture states treat the eigenvector's proof as a trade secret of state; at least one war of customs inspection is politely called *the Silk Clarification* in its winners' histories.

**[AR-18] Artisan of Leather** — solved for tanned hide — a *finished* material's eigenvector, distinct from AR-04's rot-pathway work on raw ones, a distinction both trades police with unusual energy. Restores suppleness, seals seams, trues stretched harness. Cavalry quartermasters rank the specialty above farriery, in writing.

**[AR-19] Artisan of Ice** — solved for water ice's crystal lattice: clear structural block from cloudy pond harvest, bridges trued across weak freezes, meltwater channels cut without a pick. Seasonal by nature — the eigenvector governs ice, not cold — and its holders famously winter in high country and summer as AR-05's envious students.

**[AR-20] Artisan of Quartz** — solved for crystalline silica — pointedly *not* glass, whose amorphousness is AR-05's whole solved subject; the two specialties are each other's standing Eq. 4.17 warning. Trues lens blanks, rings time-steady chimes, cleaves crystal along chosen planes. Instrument-makers' orders underwrite the eigenvector's teaching.

**[AR-21] Artisan of Marble** — solved for marble's calcite structure: flaw-reading before the first cut, crack-healing in standing statuary, a polish from within the stone. Temple works keep one on the fabric payroll for generations at a stretch; granite, an igneous stranger, stays strictly somebody else's stone.

**[AR-22] Artisan of Granite** — solved for one granitic family's interlocked structure: foundation truing, fortress patching, splitting along planes the quarry gods never intended to permit. The complementary specialty to AR-21 in every mason's order large enough to afford both — and the two eigenvectors, famously, share not one solved term.

**[AR-23] Artisan of Chalk** — solved for soft calcium carbonate: hardening a chalk face against sea-collapse, drawing survey lines that sink into the stone, quarrying blocks that hold an edge they have no business holding. A coastal specialty, held mainly by two orders who between them prop up a national coastline and never tire of saying so.

**[AR-24] Artisan of Amber** — solved for fossil resin: clarifying clouded pieces, healing crazing, sealing inclusions against air forever. The jeweler's face of the specialty funds it; the naturalist's face — a solved window onto unspoilable specimens — is why scholarly orders keep a holder on correspondence.

**[AR-25] Artisan of Wax** — solved for beeswax's structure: seals that cannot be lifted and re-set without trace, casting-patterns held true through handling, tablets that take a stylus cleanly and blank cleanly. Chanceries hold the specialty in quiet, permanent demand — the directory observes that the *unforgeable seal* has outsold every sword this catalog contains.

**[AR-26] Artisan of Pitch** — solved for wood-tar pitch: caulking driven and cured in one working, waterproofing that flexes with the hull, torch-fuel tuned to burn slow or fierce. Every major yard keeps one; every major yard's rival counts theirs. Bitumen — earth's pitch, not the tree's — is a stranger eigenvector and a recorded backlash in two yards' logs.

**[AR-27] Artisan of Bone-China** — solved for one fired porcelain body — proof, alongside AR-12, that a *made* material can be a solved eigenvector. Heals chips invisibly, trues warped firing, thins a vessel wall past the kiln's tolerance. The specialty exists in exactly one porcelain state's guild, which exports the ware and never the proof.

**[AR-28] Artisan of Obsidian** — solved for volcanic glass — a *natural* amorphous structure, cousin to AR-05's subject and, per the now-familiar warning, no part of it. Draws edges finer than any steel, heals conchoidal fractures, reads a flow's cooling history from its sheen. Surgical traditions and sacrificial ones both claim the specialty's origin; the directory records the dispute and backs neither.

**[AR-29] Artisan of Pearl** — solved for nacre's layered structure: matching lost pearls to a necklace's survivors, healing peeling luster, thickening a seed pearl toward gem grade over patient months. Divers' cooperatives and crown jewelers maintain the specialty's two very different schools, which examine each other's students with theatrical suspicion.

**[AR-30] Artisan of Charcoal** — solved for pyrolyzed wood: fuel pressed to burn at a chosen rate, filter-char tuned to a chosen taint, artist's sticks that neither crumble nor shine. The forge trade takes the tonnage; the water trade, quietly, takes the credit — a charcoal Artisan's filters have ended more epidemics than any entry above this line.

**[AR-31] Artisan of Horn** — solved for keratin in horn and hoof: lantern-panes shaved translucent and true, bows' bellies tuned, a working farriery of cracked hooves. The pastoral specialty, held widely and shallowly — the directory notes it as the eigenvector most often *inherited*, taught parent to child outside any guild at all.

**[AR-32] Artisan of Salt-Glass** — solved for one glazing compound — the fused salt-silica skin of salt-glazed stoneware, and neither the salt (AR-01) nor the glass (AR-05) it grew from. Seals a vessel's glaze against acid and age, heals crazing, trues a kiln-warped finish. Catalogued substantially because its examiners' first question is famous: *which of your three neighboring eigenvectors will kill you, and in what order?*

**[AR-33] Artisan of Blood** — solved for blood's bound structure *outside a living body*: keeping transfusion stock sound, reading old stains truly for the courts, proofing written oaths sworn in it. Living blood answers to the whole `M_op` a body is, and every charter licensing this specialty forbids the attempt in its first clause — the directory's starkest standing example of where `S` ends and Eq. 4.17 begins.

#### Master (Rare) — 16 entries

*Every entry assumes what defines the tier: a closed `S` — the complete eigenbasis (Eq. 4.18) — with Eq. 4.19's universal binding and decay control as the working instrument. The entries run from the civic to the extraordinary; none is spectacle for its own sake, in keeping with M-02's founding observation.*

**[M-03] Purefont** — Eq. 4.19 swept across a fouled well or cistern: contaminant binds eased to settle out (`s = -1` where it counts), the water's own structure left honestly alone. A city Master's most requested working by two orders of magnitude, and the standard answer to *what are Masters for?*

**[M-04] Granary Writ** — decay arrest (`s = -1`) held across a district's stored harvest through a hard season, renewed on a posted schedule. Where AD-33 blesses one hold, a Master's complete `S` covers whatever the granary contains, unlisted and unasked — the tier's generality expressed as bread.

**[M-05] Sound Timber** — Eq. 4.18 turned to a builder's honest purpose: beam-rot re-expressed as sound wood, not patched but *re-answered* across the operator's full basis. Cathedral fabrics and shipyards book Masters years out for it; the directory notes it quietly retires a dozen Artisan patches per casting, and that no Artisan has ever been recorded objecting.

**[M-06] The Long Table** — controlled ripening, curing, and aging (`s = +1`, finely staged) run across a cellar's whole inventory at once — wine, cheese, cured meat, each at its own chosen rate under one inscription. The tier's virtuosity piece: not power but *per-target discrimination*, and the working examination half the world's orders set for the Master's chair.

**[M-07] Rust's Recall** — corrosion re-expressed as parent metal (Eq. 4.18) across an armory, a bridge's fastenings, a seized engine. The transmutation the public never counts as one — lead-to-gold is a story, rust-to-iron is a budget line, and Masters' orders long ago decided which pays.

**[M-08] Mender's Completion** — Full Mend (M-01) carried to its tier-honest limit: binding boost and decay arrest interleaved across an entire grave injury — tissue, vessel, bone, all of it, one casting. What it cannot do is written into its name in every tradition: it completes *mending*; it does not return what has already ended.

**[M-09] Venom's Unwriting** — a poison's active structure re-expressed as inert matter *in situ* (Eq. 4.18, exquisitely targeted). The complete-basis guarantee is the entire point: an Artisan can only unwrite a toxin whose eigenvector they happen to hold, and poisoners, as one order's charter dryly notes, do not consult `S` before choosing.

**[M-10] Field's Restitution** — exhausted or salted cropland's mineral structure re-expressed toward fertility across whole fields. The working that ends famines rather than sieges; the handful of Masters remembered by farmland placenames all earned them with this entry.

**[M-11] Assay Absolute** — a complete-basis *read*: any sample's full composition, adulterants and all, from one casting — the Master-tier ancestor of every partial assay above (N-WK-05, N-EM-14, AD-21). Mints, courts, and poisons boards hold its findings final; the directory records no successful appeal.

**[M-12] Quarantine Line** — decay hastened (`s = +1`) in a blight's active front while everything beyond the drawn line is bind-boosted against it — AD-34's rot-fence with the whole eigenbasis behind it and a surveyor's precision to the boundary. The judgment burden remains the technique's heart; Masters who hold it sit on plague councils, rarely by choice.

**[M-13] Stone Sleep** — living timber, rope, and canvas of a decommissioned works re-expressed as mineral stillness — a fortress or fleet *paused*, decades at a time, against future need. Reversal is the same casting read backward by whichever Master the future can find; three states maintain sleeping fleets and one, famously, has lost the Masters to wake theirs.

**[M-14] Embalmer's Truth** — decay arrested completely (`s = -1`, held) for a lying-in-state, a long repatriation, or a court's unhurried inquest. M-02's grave-turn made ceremonial and forensic; every tradition that practices it maintains, in identical words, that the working serves the living's need to see truly.

**[M-15] The Salted Ground Unsaid** — deliberate reversal of scorched-earth ruin: burned soil, fouled wells, and sown salt re-expressed toward what they were, across a settlement at a time. Catalogued with its history attached — the entry exists because the working that *causes* such ruin needs no catalog, and Masters' orders have preferred it that way for six centuries.

**[M-16] Forge of Last Resort** — arbitrary feedstock re-expressed as the specific alloys a crisis demands (Eq. 4.18 at industrial patience): a snapped caravan axle from river stones, boiler plate from ballast. Slower and costlier in fidelity than any honest foundry — the directory lists it, as every quartermaster's manual does, under *when there is no foundry*.

**[M-17] The Gentled Blade** — every edge, point, and firing mechanism in a surrendered armory eased toward uselessness (`s = -1`, permanent by renewal) without destroying a single artifact. The diplomatic working: treaties specify it by this directory code in at least nine surviving instruments, which is more than any other entry in this catalog can claim.

**[M-18] Master's Audit** — a working cast on another caster's standing workings: reading, by complete-basis touch, what has been bound, arrested, hastened, or re-expressed in a place, and by roughly what hand. The tier's instrument of governance — orders use it to certify Artisans' claims, courts to unmask fraudulent ones, and historians, with permission and a Master to spare, to read what the dead built.

#### Warden (Very Rare) — 12 entries

*Warden catalog entries remain what W-01's preamble says they are: rarities, because each is welded to one practitioner's proven geometry. The twelve below are the catalogable exceptions — techniques whose `R_proven` (Eq. 4.20) is a class of site so standardized, or an institution so old, that the proof genuinely transfers. Each entry names its geometry; each ends, like all Warden work, exactly at `eps_valid(R_proven)`'s edge (Eq. 4.21).*

**[W-02] Stairwell Grace** — a mapped tower stair's effective steepness eased by a whisper of curvature. Proven, historically, for one royal keep's stairs and every stair since built to its published dimensions — the first Warden proof ever deliberately *standardized into architecture*, and the reason a dozen unrelated buildings share one staircase.

**[W-03] Deep Shaft Mercy** — a fall down one mapped mineshaft made survivably slow along the shaft's own line. The proof cost its Warden years and is tied to the shaft's exact bore; the mining order that holds it re-sinks new shafts to the old bore's gauge, on purpose, and calls the gauge *mercy-width*.

**[W-04] The Weighted Cell** — a single prison cell, mapped to the brick, where crossing the threshold outward costs triple weight. Escape-proof is a myth this entry does not claim; *escape-slowed* funds the technique's keep in four citadels. The directory notes the geometry must be re-proven after any renovation, and that one famous escape followed a repointed wall.

**[W-05] Bridgekeeper's Palm** — a proven span's load eased under one crossing cart at a time — the bridge briefly carries what its engineering alone could not. Tied to one bridge per proof; the great river cities each keep their own Warden and their own proof, and the proofs, famously, do not transfer even between twin spans.

**[W-06] Training Circle** — a casting-school duel ring, mapped for generations, within which every fall lands soft. The geometry every heir to the school re-proves as their graduating work — making the circle itself, as the schools put it, the only student never expelled.

**[W-07] Harbor Palm** — one mooring basin's chop stilled by a held whisper of curvature at the water's mapped rest. Proven for that basin, its dredged depth, its tide-range; a silted season invalidates it, which is why the harbor that holds this proof dredges on a Warden's calendar, not a harbormaster's.

**[W-08] The Listing Ward** — a subsiding tower's lean *held* — not corrected, held — by a standing whisper against its mapped failure line. Renewed daily for one hundred and forty years so far by an order founded for the purpose. The directory lists it as the tier's plainest demonstration that Warden work is bookkeeping with consequences.

**[W-09] Sickroom Ease** — one hospice's mapped ward-floor where the bedridden weigh less to their own failing frames — sores slowed, breathing eased, nurses' lifting halved. The proof transfers to hospices built to the founding floor's plan, and eleven have been, which the founding Warden's epitaph counts as her `R_proven`.

**[W-10] Vault Step** — a treasury antechamber where every unauthorized pace inward grows heavier along the mapped approach. The authorized path is a memorized eccentric line — changed quarterly, *within* the standing proof — making this the rare Warden technique with a moving part, and the model for every lesser imitation.

**[W-11] The Proving Corridor** — a casting-order's mapped corridor held at a whisper *more* curvature than flat — the one place a student Warden can feel a true metric gradient at survivable scale before ever attempting one. Wardens' orders consider the corridor's upkeep their first duty; per §1.4, it is also the only classroom whose subject rebuilds the classroom.

**[W-12] Ferry Line Hold** — a cable ferry's mapped crossing eased along its own line — the water's pull on hull and cable lightened between two surveyed banks. Tied to the crossing, not the boat; the ferry has been rebuilt nine times, the proof never, a distinction Warden curricula quote verbatim.

**[W-13] The Quiet Field** — one mapped ceremonial ground where every voice, footfall, and casting lands *slightly* softened — an `eps` chosen for reverence rather than utility. Proven and held by a contemplative order who publish, uniquely and deliberately, their complete `eps_valid` ledger — the directory's only fully open Warden proof, and the tier's standing gift to Warden pedagogy.

#### Legend (A Handful Across Recorded History) — 8 entries

*As with LG-01 and LG-02, every entry below is Sovereign mathematics unchanged (§4.1–§4.3) held under Eq. 3.1g's scaling, and every one has become an institution, because that is what Legend-scale upkeep (Eq. 4.22–4.23) requires. The names below are the names history uses; the directory's contribution is the mathematics under them.*

**[LG-03] The Pilgrim's Stair** — a mountain crossing where the climb weighs half what geology insists — a standing curvature ease along a mapped pass, held for six generations by the hospice-order at its summit. Its `t_drift` bookkeeping is glacial in every sense: the order re-surveys the ice-load's mass redistribution each thaw, and the pass has closed exactly twice, both times because the survey lapsed before the mathematics did.

**[LG-04] The Quiet Vault** — an archive valley under standing minor time-dilation — years outside for months inside — where a founding Legend banked a civilization's most fragile records against time itself. The keepers enter by rotation measured against their families' aging; the vault's `t_drift` cadence is the outside world's *seismic* drift, and its founding charter is one sentence: *what enters late leaves early.*

**[LG-05] The Long Road** — a standing fold-pair (Eq. 4.1, held per Eq. 4.22) joining a capital to its port, a month's caravan in an afternoon's walk, for two hundred years. The maintaining order re-surveys the port-end's conformal factor on a tide-linked `t_drift` cadence; the directory notes, as LG-01's write-up did, that the order's true craft is scheduling — and that the road's toll schedule *is* the maintenance budget, published as law.

**[LG-06] The Gentle Coast** — a standing whisper of curvature along a mapped hundred-mile lee shore, softening what storm surge can pile against it — W-07's harbor palm at a scale only Eq. 3.1g's dials distinguish from it. Maintained by a coastal league whose member cities each fund one segment's re-survey; the one recorded segment default is why the league's charter now begins with the flooding it caused.

**[LG-07] The Deep Anchor** — a Bound Singularity (Eq. 4.12) sunk beneath a strait as a standing tidal engine, its shell recertified (Eq. 4.23) by a hereditary college of tide-wardens. The strait's currents run the mills of three nations; the college answers to all three and, by its founding compact, to none of them alone — the directory's standing example of what a Held Star's politics look like when the star is load-bearing.

**[LG-08] The Orchard Perpetual** — a valley under standing *reversed* dilation — months outside, years inside — where slow-maturing groves, vintages, and timber pass decades in a season. The Quiet Vault's mirror twin, held by a sibling order, and the two institutions' shared re-survey calendar is the closest thing metric-sector practice has to a professional journal.

**[LG-09] The Sky Harbor** — a standing region of eased weight above a plateau city where cargo rises on winch-lines no engine drives — a curvature well *inverted*, held open as public infrastructure for a century and a half. Its recertification interval is set by the plateau's own erosion; the city's stonemasons and its metric-order share one guildhall, which every visiting scholar remarks upon and every resident finds unremarkable.

**[LG-10] The Border That Persuades** — a frontier march under a standing, mild gradient — every step across it heavier than the last for a mapped dozen miles — raised by a Legend whose realm wanted no wall. Armies can cross it; nothing about crossing it is worth it, which was the design brief in full. Its maintaining order is, by treaty, staffed from *both* sides of it — the mathematics is indifferent to direction, and the treaty's drafters were not fools.

#### Beyond Legend (Historical Fragments) — 4 entries

*As with AS-01 and AS-02: nothing below is teachable in the ordinary sense. These are documented historical attempts along the four paths of §3.3, each quantified after the fact by its path's closeness metric (Eq. 4.24–4.27), and each catalogued for what it proves about the distance rather than as a route across it.*

**[AS-03] The Thousandth Alloy** — the life's work of a Demiurge aspirant who proved one extrapolation rule `r` along a single mixing family and drove `N_family` (Eq. 4.25) past a thousand verified, never-before-observed stable alloys — several of which underpin whole trades today. Records treat the work with the exact double edge Eq. 4.25 predicts: complete mastery of one proven rule, and by the aspirant's own surviving marginal note, *"no nearer the rule of rules than the day I began."*

**[AS-04] The Widening Ring** — a Cosmographer aspirant's forty-year campaign to push one closed-form domain outward, ring by re-proven ring, driving `rho_cosmo` (Eq. 4.26) to the highest value ever independently audited. The campaign's own ledgers are the historical proof of §1.4's cruelty: each ring's cost is recorded, each exceeds the last, and the final entry prices the *next* ring at more than all forty years combined. The aspirant stopped. The ledger, historians note, does not say *failed*.

**[AS-05] The Sixfold Silence** — a second Tetrarch fragment, complementary to AS-01: an aspirant who, rather than chaining the six `Chi` pairs at speed, held all six *simultaneously quiescent* — a standing readiness in which any pair could express without preamble, sustained for a legendary afternoon. Witnesses swore the four forces "waited on her like servants in one hall." Eq. 4.24's verdict is unchanged by the elegance: six couplings in perfect agreement are six couplings, and `k_unified` remained, as ever, unwritten.

**[AS-06] The Unfinished Chorus** — the cautionary completion of AS-02's story: a later Communion that attempted to *hold* its merged boundary standing rather than dissolve after one casting. `N_comm` (Eq. 4.27) exceeded every prior record for eleven days. The surviving accounts of the dissolution are sealed by the three orders that keep them, and the directory records only what all three publish jointly: that `dM_total` is a union of provers, not proofs; that the members were recovered as *members*; and that no Communion since has petitioned to try.

---

### Directory Expansion II (v2.6) — 200 Further Named Techniques

*Added in v2.6. Entry codes continue from Expansion I: Novice from N-EM-26 / N-GR-19 / N-ST-18 / N-WK-13, Journeyman from J-48, Adept from AD-41, Artisan from AR-34, Master from M-19, Warden from W-14, Legend from LG-11, Ascension from AS-07. Same conventions and prevalence weighting as Expansion I; no new global equation numbers, no changes to existing entries, and Sovereign remains uncatalogued by design.*

#### How to read this expansion

All of Expansion I's reading rules carry forward unchanged: single-channel `delta(F_f)` distortions (or sourceless passive reads) at Novice; Eq. 4.13's disjoint windows at Journeyman; only the six `Chi(f1,f2)` pairs at Adept, each entry naming its pair; one signature material per Artisan entry (Eq. 3.1e, 4.16), with its Eq. 4.17 neighbors named; complete-`S` workings at Master (Eq. 4.18–4.19); one proven geometry per Warden entry (Eq. 4.20–4.21); Sovereign mathematics under Eq. 3.1g's scaling at Legend, with the maintenance interval called out (Eq. 4.22–4.23); and historical fragments only, quantified by Eq. 4.24–4.27, beyond that. The directory-local notation defined in Expansion I's glossary (`t_hold`; *reverse-sign casting*; *held vs. discharged*) is used freely below without redefinition.

---

#### Novice (Common) — 60 entries

*Electromagnetic (`k_EM`)* — extends Eq. 4.0a; passive reads extend Eq. 4.0e.

**[N-EM-26] Shaded Lamp**
Lumen Thread's glow (N-EM-03) shaped to shine into a narrow arc and nowhere else — light for the page that shows nothing to the window. The directional shaping is the skill: the same `delta(F_EM)`, sculpted rather than merely held. Standard issue, informally, to every clerk who has ever worked past a garrison's curfew.

**[N-EM-27] Clear Pane**
A whisper of warmth held across glass — a window, a lens, a lighthouse light — keeping frost and breath-fog from forming at all. The rare heating technique judged entirely by what the observer *doesn't* see, which is why lighthouse keepers examine candidates on it in winter, at night, without warning.

**[N-EM-28] Bellows' Ghost**
A moving column of warmed air driven across a forge bed or malting floor — Eq. 4.0a applied to air in motion rather than a body at rest. Holding heat *in something that leaves* is the training value; smiths call a caster who can't yet do it "still heating the room."

**[N-EM-29] Bearing Sense**
The formalized discipline built atop Ripple Sense (N-EM-05), exactly as Eq. 4.0e's write-up predicted someone would build it: reading not just *that* aether moves nearby but roughly *whence* — the read taken at both ears' distance apart, so to speak, and the difference judged. Still a pure passive read, still costless (Eq. 4.0e); the directory catalogs it because every tradition teaches it and no two agree who invented it.

**[N-EM-30] Cook's Even Hand**
Eq. 4.0a spread deliberately flat across a pan or griddle's whole face — no hot center, no raw rim. The domestic sibling of N-EM-20's diffuse hold, and the standard second-year exercise for exactly the same reason: *even* is harder than *strong*.

**[N-EM-31] Smokeless Torch**
A staff-head glow bright enough to walk by, held for a full watch — Lumen Thread scaled up and toughened against the holder's own jostling stride. The casting every night-courier actually uses, catalogued separately from N-EM-03 because sustaining a glow *while moving* is a distinct and harder discipline.

**[N-EM-32] Iron Cry**
Lodestone Touch (N-EM-08) cast on a sweeping tool rather than a needle — dropped pins, nails, and blade-shards leap from floorboards and hay to the magnetized head. Seamstresses' shops and stables both keep the technique in the family; the guilds have given up asserting jurisdiction.

**[N-EM-33] Chill Draught**
Cold Ember (N-EM-02) worked through a sickroom's air rather than a body or a drink — a few degrees of relief held through a fever's worst night. Physicians rank it with N-EM-14 and N-WK-04 as the Novice sickroom triad, and casting schools teach the three together under that name.

**[N-EM-34] Storm Bleed**
A slow, deliberate discharge trickled from a mast-top, steeple, or standing crane down to ground as a storm builds — charge spent quietly before the sky can spend it loudly. Harbor and cathedral wardens keep the technique on their storm rosters; the directory notes that it does not make lightning impossible, merely *bored*.

**[N-EM-35] Ember Purse**
A single coal held alive at the bottom of a lined pouch for a day's march — Eq. 4.0a at its absolute minimum output, plus patience. Predates written casting instruction in every tradition that has looked; several curricula still open with it on the grounds that their founders did.

**[N-EM-36] Scholar's Constant**
A reading light held not merely steady but *unvarying* — no flicker, no drift, for hours. Copyists and illuminators pay the premium over candles gladly; oculists prescribe it; casting examiners love it, because any wobble in `Fid` is instantly, publicly visible in the light itself.

**[N-EM-37] Thawline**
Gentle warmth walked along a path, stoop, or gutter-run, clearing ice without the salt that kills the spring garden. Municipal casting rosters in cold cities list it as the season's bulk work; Novices bill it by the paced yard.

**[N-EM-38] Curing Cave**
Chill Locker (N-EM-09) scaled to a cheese shed, hanging room, or root cellar and held through the warm months — the largest-volume cold-hold in the Novice tier, and the standard endurance benchmark on the cold side, as Sun's Patience (N-EM-22) is on the warm.

**[N-EM-39] Current Taste**
A passive read (Eq. 4.0e) taken *before touching* — a wire, a rail, a cloud-watching mast, another caster's apparatus — for the live charge it may carry. Costless, sourceless, and responsible, linemen's guilds attest, for more working careers reaching retirement than any technique in this catalog.

**[N-EM-40] Traveler's Hearthline**
Soaked boots, cloaks, and blankets dried overnight by a low, even warmth threaded through the drying rack. Inns advertise a caster on staff with a boot-shaped sign; the sign is older than three of the languages it appears in.

**[N-EM-41] Star Point**
A single brilliant mote thrown high and held burning for a slow count — position, distress, or *rally here*, visible for miles. The discharged counterpart to Signal Thread's held code (N-EM-21); every military manual pairs them on the same page.

**[N-EM-42] Glassblower's Patience**
A gathered glass mass held at working heat between furnace trips — minutes bought at the bench that the furnace would otherwise reclaim. Catalogued at Novice with a standing note: this holds *heat in glass*; shaping the glass itself is AR-05's eigenvector and no part of this casting, a distinction glass-shops drill because the confusion is an Eq. 4.17 story waiting to happen.

**[N-EM-43] Ice-House Debt**
Deep, sustained chill poured into an icehouse's mass in high summer — spending a day's casting to extend a season's store. The bulk-work counterpart to N-EM-16's cupful; ice merchants contract it by the hundredweight preserved, audited at autumn opening.

**[N-EM-44] Needle Unsworn**
The reverse-sign casting of Lodestone Touch: magnetization *removed* from a tool, blank, or instrument part that has picked it up unwanted. Instrument-makers cast it before every fine assembly; navigators cast it on everything *near* the binnacle and trust nothing anyway.

**[N-EM-45] Dry Keeping**
A sealed cask, chest, or powder store held a few degrees above the damp — tinder that strikes, biscuit that snaps, paper that takes ink. The unglamorous warm-side twin of N-EM-38, and the technique quartermasters actually mean when they requisition "a caster for the stores."

*Gravity (`k_grav`)* — extends Eq. 4.0b.

**[N-GR-19] Even Pour**
A falling stream — grain into a hopper, sand into a mold, shot into a bag — lightened just enough to slow and smooth its pour. Millers and founders use it daily; casting instructors prize it as the tier's best drill for holding an effect on a *continuous* target rather than an object.

**[N-GR-20] Ringer's Ease**
The great bell lightened through the hard first pulls of swing-up, released once momentum owns the work. Bell towers with a caster among the band ring heavier bells than their ropes deserve; the release timing, as with N-GR-13, is the entire examination.

**[N-GR-21] Diver's Stone**
A descent-weight held heavy on the way down and released at depth — one casting, one hold, one letting-go, in the dark, under pressure of both kinds. Pearl and sponge divers rate casters by how *exactly* the release lands; the directory rates the technique as N-GR-13's discipline with higher stakes.

**[N-GR-22] Ladder Faith**
Anchor Step's increase (N-GR-02) cast on a ladder's feet rather than the climber's. The climber climbs unencumbered; the ladder simply declines to walk. Catalogued beside N-GR-12 as the pair every building trade teaches its first-years in their first week.

**[N-GR-23] Assayer's Stillness**
A fine balance's pans made fractionally heavier, damping their swing to a fast, honest rest. Weigh-houses cast it before every disputed measure; the directory notes with approval that both parties customarily watch the casting, which is precisely why it is done.

**[N-GR-24] Warding Fall**
Feather Fall (N-GR-01) held *ready* over a drop that someone frail, small, or reckless is near — a contingency hold in J-28's sense, but within a single casting: the window is open, the effect waits on the fall. Nurses, scaffold foremen, and the parents of climbing-aged children make up its entire clientele, which is to say most of the world.

**[N-GR-25] Picker's Yoke**
Light Load (N-GR-03) on a full basket, pail, or hod across the carry that fills it — the load lightened *while being added to*, which is the catalogued difficulty. Harvest crews and hod-carriers drill it; the technique's test is that the hold must not lapse at the moment more weight arrives.

**[N-GR-26] Mire Step**
Light Load on the caster's own steps across bog, mudflat, or rotten ice — Ford Keeper's (N-GR-16) exact opposite, catalogued as its pair. Fen-country guides hold both and choose per crossing; choosing *wrong* is the region's oldest joke and occasional obituary.

**[N-GR-27] Ridgepole Rise**
Light Load on a roof-tree or truss through the raising, from ground to seat. The mason has N-GR-18; this is the carpenter's, and barn-raising country treats a visiting caster's afternoon as payment for a winter of dinners.

**[N-GR-28] Long Portage**
A boat lightened on its bearers' shoulders between waterways — held, walking, for however long the path insists. The voyageur's one indispensable casting; brigades log portage times with and without, and recruit accordingly.

**[N-GR-29] Deadfall's Word**
Anchor Step's increase on a trap's drop-weight or a pile-driver's ram at the moment of release — the fall made *committed*, faster and truer than gravity alone would insist. The directory catalogs the pile-driver use; the trapper use is older and the technique keeps the trapper's name.

**[N-GR-30] Flywheel's Memory**
A potter's wheel, grindstone, or lathe-wheel rim made temporarily heavier, storing steadier momentum through uneven work. Turners call the effect "borrowed patience"; examiners call it the cleanest demonstration that N-GR-02's equation never cared whether its target was still.

**[N-GR-31] Belayer's Root**
Anchor Step on the *holder* of the rope rather than the climber on it. Mountain schools teach it before any technique aimed at the climber themselves, on the argument — carved over one school's door — that the mountain is climbed by the one who doesn't fall.

**[N-GR-32] Festival Rise**
Paper lanterns, petals, or streamers lightened at release to climb far past their means. Pure ornament, catalogued without apology: by headcount of witnesses, likely the most *seen* gravity casting in the world, and many casters' first public work.

**[N-GR-33] Plow's Bite**
Anchor Step's increase on a plowshare through baked or root-bound ground. The team pulls no harder; the iron argues better. Field casters bill it by the furlong, and the directory notes it has quietly ended more disputes with heavy soil than any tier above it.

*Strong (`k_strong`)* — extends Eq. 4.0c.

**[N-ST-18] Line's Reprieve**
Seal Bind (N-ST-01) along a frayed span of rope or cable, holding the damaged length trustworthy until the splice can be made. Patch Press's (N-ST-06) rigging sibling, carried under the same rule: a reprieve is a promise, and harbor authorities audit standing ones.

**[N-ST-19] Netmender's Faith**
Knot Faith (N-ST-05) cast across a net's whole working panel at the haul — hundreds of small crossings held as one binding. The volume, not the strength, is the catalogued skill; crews rate a caster by how big a panel they can hold honest through a heavy catch.

**[N-ST-20] Icebreaker's Line**
Brittle Ease (N-ST-02) walked along river ice ahead of a channel cut — Quarry Line's (N-ST-15) winter twin, point by patient point. Ferry towns open their season with it; impatient towns open theirs a casting early and a boat short.

**[N-ST-21] Surgeon's Thread**
Seal Bind at sutures, holding a closed wound's stitches against the body's first restless days. Cast, like N-ST-10, only alongside a mender's instruction, and catalogued with the same standing note: the casting is Novice, the judgment is not.

**[N-ST-22] Drawer's Grace**
Brittle Ease at the grip of a rooted thing — a bad tooth, a rusted spike, a fence post set by someone's proud grandfather — for a clean pull instead of a broken one. Toothdrawers gave it its name; every other trade that pulls things borrowed it and kept the name out of respect or amusement.

**[N-ST-23] Cobbler's Week**
Seal Bind through new boots' seams and sole-stitching across the breaking-in — the boot yields to the foot while the work holds. Marching regiments contract it by the company, and cobblers' guilds, after a century of grumbling, now examine for it.

**[N-ST-24] Grindstone True**
Eq. 4.0c through a spinning grindstone's bulk against the burst that speed invites. The wheel-shop safety casting, held for the duration of every hard run; insurance clubs in three cities discount premiums for shops that keep a caster on the stone.

**[N-ST-25] Shake-Rider**
Brittle Ease down a cedar or oak bolt's rays, riving shingles and lath true off the froe. Green Split's (N-ST-04) finer-grained cousin; shake-makers call the difference "asking the tree politely," and the directory can improve neither the phrase nor the technique.

**[N-ST-26] Binder's Press**
Seal Bind across a sewn book-block while glue and cords set — N-ST-17's logic at the bindery bench, holding signatures square through the cure. Scriptoria schedule it as the wheelwrights do, by the drying afternoon; apprentice casters read while they hold, which both trades approve.

**[N-ST-27] Wellstone Guard**
Shatterguard's hold (N-ST-09) cast down a well or cistern lining while someone works below it. The stones were sound this morning; the casting is for the afternoon. Well-diggers' first rule names it: *no descent unwarded*, and the rule is old enough to scan in verse.

**[N-ST-28] Knapper's Consent**
Chisel's Consent (N-ST-07) carried to flint, chert, and obsidian's conchoidal moods — the flake eased off its chosen plane and no other. The oldest stone trade's newest tool; master knappers accept it grudgingly, use it precisely, and still check the edge by eye, thumb, and oath.

**[N-ST-29] Sea-Chest Seal**
Seal Bind around a chest, cask, or magazine lid's seam for a passage's leg — watertight by casting until made watertight by craft. Pursers log standing seals by berth and renewal date; the log's name aboard most hulls is simply *the promises*.

**[N-ST-30] Fished Mast**
Seal Bind through a sprung spar and its lashed splints — the sailor's fishing of a wounded mast, held from the casting until a yard's honest repair. The open-water sibling of N-ST-06 and N-ST-18, and the entry most often cited in wreck inquiries under *casting, absence of*.

**[N-ST-31] Tent Against Gale**
Eq. 4.0c through canvas, guys, and seams as the weather arrives — the whole shelter bound as one cloth for the blow's duration. Expedition casters hold it in shifts; the directory notes that the technique's true test, every tradition agrees, is casting it *calmly*.

**[N-ST-32] Kiln Prop**
Shatterguard's logic carried into the fire: saggars, shelves, and props bind-boosted through a firing's stress hours. Potteries schedule the casting with the fuel; AR-27's porcelain guild famously staffs it with Novices and pays them like Journeymen, which the directory records as both fact and hint.

*Weak (`k_weak`)* — extends Eq. 4.0d. The tier's standing caution — faint by nature, easy to underestimate — carries forward from Expansion I unchanged.

**[N-WK-13] Reckoner's Touch**
A calibrated decay nudge into old bone, ash, or timber, with the response's strength read against a reckoner's table — a crude age-of-remains estimate, honest to the nearest generation or so. Courts admit it as corroboration, never proof; scholars use it to decide which digging is worth a Master's Audit (M-18).

**[N-WK-14] Firefly Ink**
Nudge-responsive mineral ink that answers a later touch with a soft glow — night-legible orders, boundary-stones that name themselves to a caster's hand, marginalia meant for one reader. Deep Mark's (N-WK-08) portable descendant, and the quiet favorite of every courier service with secrets.

**[N-WK-15] Cinder Sentinel**
A nudge swept through a dead-looking ash heap, spoil pile, or burned-over field — live pockets answer with a glow the eye would never find. Fire-watches cast it behind every extinguished blaze; the technique is credited by name in more city fire codes than any other Novice entry.

**[N-WK-16] Retting Nudge**
Quick Ripen's logic (N-WK-01) turned to flax and hemp in the retting pond — the fiber's release hastened by days, the stink's tenure mercifully shortened. Linen country holds it as N-WK-06's equal in the year's round, and both smell like money to those who cast them.

**[N-WK-17] Silage Keep**
Slow Larder (N-WK-03) at fodder scale — the pit or rick's spoilage slowed through the margin weeks between a thin winter and a lost herd. Pastoral districts roster their weak-force Novices for it the way grain districts roster granary work; the two rosters, famously, trade casters at the equinoxes.

**[N-WK-18] Angler's Star**
Faint Ward-Light on a float, night-line, or trap-marker — a glow that rides the water and cannot drown. The Novice ancestor of AD-39's harbor-scale blend, catalogued as such; fisherfolk, asked about the lineage, reliably answer that the Adepts borrowed it from *them*.

**[N-WK-19] Mushroom Bed Quicken**
Compost Quicken's nudge (N-WK-06) tuned to a spawn bed's slower appetite — cultivated mushrooms brought to flush days early, cellar by cellar. A city technique, oddly: catalogued from the capital's cellar-farms, where casters and growers are usually the same person.

**[N-WK-20] Bathhouse Stones**
Hearthstone (N-WK-04) at civic scale — a bath's stone bank nudged to a faint, steady warmth that carries the day between firings. Bathhouses in fuel-poor towns budget the casting against the wood it saves; the arithmetic, posted by law in two provinces, favors the caster embarrassingly.

**[N-WK-21] Vigil Chain**
A row of faint ward-lights kindled in sequence through the night, each new glow marking a watch's turn — the hours made visible down a wall, a ward, a harbor front. Long Watch's (N-WK-10) institutional form; garrisons that keep it say the chain is for the watchers, and widows say otherwise, and both are right.

**[N-WK-22] Quarantine Mark**
A ward-light glow worked into a door-mark that cannot be doused, scrubbed off, or quietly painted over — only outwaited, at the mark's own slow fading. Plague ordinances in every major port specify it; the directory records, without further comment, that its casters are paid double and thanked never.

#### Journeyman (Common) — 40 entries

*As throughout: two closed-form castings held without blending — clean sequence or live either/or — under Eq. 4.13's disjoint windows. The components below draw freely on Expansion I and II Novice entries; the switching discipline remains the technique.*

**[J-48] Lighthouse Round** — N-EM-27 on the lamp-glass, N-EM-34 down the tower as weather builds. Clear the light, bleed the sky, in alternation all night; the keeper's log marks which window was open when, and inspectors read it like scripture.

**[J-49] Icehouse Summer** — N-EM-43 into the mass at dawn, N-ST-29 on the door-seal at close. Chill, then seal — never together, and the merchant's ledger thanks the discipline twice.

**[J-50] Steeplejack's Creed** — N-GR-22 at the ladder's foot, then N-GR-24 held over the drop while aloft. Faith below, warding above; the trade's oath names both windows in order and apprentices recite it at the first rung.

**[J-51] Fenland Post Round** — N-GR-26 across the mire, N-EM-31 through the dark miles after. The fen courier's pairing; the choice of which window opens at dusk's edge is the district's standing interview question for new riders.

**[J-52] Foundry Pour Sequence** — N-GR-19 steadying the metal's fall, then N-ST-24 on the mold-wheel taking it. Pour window closed before spin window opens — a cadence called aloud, because molten metal forgives less than examiners do.

**[J-53] Sickroom Night** — N-EM-33 through the air, N-WK-04 at the feet, in turn as the fever argues. The Novice sickroom triad's third member (N-EM-14) opens between them as a read — three windows, strictly disjoint, and the physician's real skill is the order.

**[J-54] Bell Founder's Proof** — N-EM-14's pulse through the cooling casting, then N-ST-24's hold as the bell is first swung. Read, then guard; the trade's saying — *listen before you let it speak* — is Eq. 4.13 wearing an apron.

**[J-55] Night Harbor Watch** — N-WK-18 on the far buoys *or* N-EM-41 when a hull comes in wrong. The either/or is the discipline: the star is spent the moment it flies, and a watch that flares at every shadow guards nothing by midnight.

**[J-56] Divers' Tender** — N-GR-21 managed on the stone, then N-ST-27's guard down the ladder-line between dives. Weight window, ward window, never both; tenders keep the count aloud, and the count is the technique.

**[J-57] Winter Stores Round** — N-EM-45 through the dry stores, N-WK-17 at the silage, walked in turn each dusk. The quartermaster's pairing across two forces and two kinds of patience; garrison manuals list it under *duties, unglamorous, essential*.

**[J-58] Ropewalk Proof** — N-ST-18 holding the flawed span, then N-ST-22 drawing the condemned strand clean at the splice. Reprieve, then removal — same force, opposite signs, and the walk's master watching that the windows never touch.

**[J-59] Orchard Night Round** — N-WK-01 along the early rows at dusk, N-WK-22's cousin-mark on the blighted trees for morning's axe. Ripen the sound, mark the sick; the pairing behind AD-34's blend, held here the honest Journeyman way — one window at a time.

**[J-60] Raising Day** — N-GR-27 under the ridgepole, then N-ST-08 through the pegs as it seats. Lift window closed, lock window open, on the foreman's single word; barn country holds the word itself to be the technique's true name.

**[J-61] Tower Ringer's Change** — N-GR-20 through swing-up, then N-EM-36's steady light on the ropes through the changes. Ease, then illuminate; ringing masters note that the second window exists so the first is never needed twice.

**[J-62] Assay Bench Sequence** — N-WK-13's dating touch, then N-EM-39's charge-taste before the sample meets the instruments. Two reads in strict order — J-39's discipline extended one window deeper, and catalogued for the same reason: information has a casting order too.

**[J-63] Icebound Ferry Drill** — N-ST-20 along the channel line, then N-GR-16 as crew walk the cut's edge. Ease the ice, weight the walkers; ferry towns drill it as one exercise with two names, which is Eq. 4.13 taught by winter.

**[J-64] Lampwright's Close** — N-EM-42 holding the gather warm, then N-ST-32's guard as the piece enters the annealing kiln. Heat-hold window, bind window, in sequence at the bench — the glasshouse's standing proof that a Journeyman with two Novice castings outworks a Novice with either.

**[J-65] Trapline Round** — N-GR-29 setting the deadfalls at dawn, N-WK-14's ink blazing the line for the return. Set, then sign; the pairing's discipline is that the marks are made *after* the weights are committed, for reasons every trapper explains with the same shortened finger they don't have.

**[J-66] Harbor Chain Test** — N-ST-18 along the boom-chain's worn links, then N-GR-23's stillness on the strain-gauge weighing them. Hold, then measure — and never measure what you are currently holding, which is the entry's entire catalogued lesson and a proverb in two navies.

**[J-67] Granary Door Round** — N-WK-17 within, N-ST-29 at the seals, walked in opposite orders morning and night. The symmetry is deliberate and examined: a Journeyman who can open two windows in either order holds them; one who can only run the drill forward is still drilling.

**[J-68] Storm Shepherd** — N-GR-33's bite on the fold's gate-posts, then N-ST-31 across the fold's canvas as the gale lands. Root, then bind; hill shepherds pair it with a third, unlisted discipline — going out at all — that the directory respectfully declines to formalize.

**[J-69] Mint Sequence** — N-EM-44 unswearing the blanks, then N-GR-23 stilling the scales that judge them. Two quiet castings between the world and bad coin; mint-masters examine the pairing annually and publish neither the order nor the reason.

**[J-70] Chandler's Evening** — N-EM-35's ember kept in the shop, N-WK-21's chain lit down the lane at dusk. Keep one fire, tell the hours with another force entirely; the lamplighter-chandler double trade exists in most towns *because* this pairing does.

**[J-71] Ford Survey** — N-EM-39's taste of the storm-charged air, then N-GR-26 across the doubtful crossing. Read the sky, then walk the water; fen guides hold that the first window's answer decides whether the second ever opens, which is contingency pairing (J-28) taught by weather.

**[J-72] Portage Brigade Round** — N-GR-28 under the hull, N-EM-40's drying warmth at the night camp. Carry, then cure; brigade logs across a century show the pairing's second window is the one that keeps crews whole, and recruiters lead with it.

**[J-73] Wreck Survey Sequence** — N-EM-05 listening for another crew's workings in the hulk, then N-ST-27's guard down the entry. Listen, then ward, in that order absolutely; salvage law in three ports *requires* the first window, and the requirement is written in the casualty lists that preceded it.

**[J-74] Festival Marshal's Round** — N-GR-32 at the release, N-EM-12's fence around the launch ground. Joy, then order — or as the marshals' manual puts it, the crowd may fly nothing the fence hasn't approved. The directory notes the manual is illustrated.

**[J-75] Bathhouse Round** — N-WK-20 through the stone bank, N-EM-33's draught in the cooling room, in turn through the day. Warm one chamber, cool another, one caster, two forces; the posted schedule *is* the `tau_switch` ledger, which makes it examiners' favorite field trip.

**[J-76] Vintage Watch** — N-WK-16's cousin-nudge in the press-house, then N-EM-38's cave-chill below. Hasten above, hold below; cellar-masters call the stair between them "the switch," and the directory certifies the pun as load-bearing.

**[J-77] Beacon Keeper's Choice** — N-EM-41 skyward *or* N-WK-18 on the water-line, chosen by what the night must be told. J-35's either/or discipline with louder stakes; keepers log the choice, and boards of inquiry read the log first.

**[J-78] Surgeon's Sequence** — N-ST-21 at the sutures, then N-EM-14's pulse reading the wound's heat at each dressing. Bind, then read, never both at once — the read lies while the bind is live, which is J-29's kiln lesson written on skin, and taught with exactly that sentence.

**[J-79] Sapper's Second Discipline** — N-ST-28's consent through the counter-mine's flint seam, then N-EM-05 held listening in the dark after. J-43's sibling, one stone harder; the manuals of two armies print the pair on facing pages, and deserters from both agree the pages are honest.

**[J-80] Coach Inn Evening** — N-GR-14 across the spent teams, N-EM-40 over the passengers' sodden coats. The ostler's round (J-44) widened by a force; posting-houses advertise the pairing on the gate, and the gate, in coaching country, is the region's actual currency.

**[J-81] Reef Passage Drill** — N-GR-11's trim on the helm's call, then N-ST-30's fished-spar hold ready as contingency. An open window and a waiting one — J-28's reserve discipline at sea, drilled until the crew forgets which of the two they're more afraid of needing.

**[J-82] Archivist's Deep Round** — N-EM-45 through the stacks, N-WK-14's ink answering the catalog's touch-marks. Keep dry, then read the marks the dryness protects; great libraries roster the round nightly, and the round's ledger is, itself, archived. The directory suspects the archivists know exactly how that sounds.

**[J-83] Quarry Winter Sequence** — N-EM-37's thawline to the working face, then N-ST-15's points along the mark. Clear, then split; winter quarries run the pairing at first light, and the pairing is why winter quarries run at all.

**[J-84] Plague Door Round** — N-WK-22's mark set, then N-EM-12's fence strung at the lane's mouth. Mark, then bar — two forces between a sick house and a frightened street, and the marshals who walk the round paid, per J-59's grim arithmetic, double and thanked never.

**[J-85] Foundling's Second Kit** — N-EM-35's ember *or* N-GR-24's warding hold, chosen by whether the night threatens cold or falls. J-41's self-taught pairing one hard winter older; catalogued, like its parent, because it appears everywhere unprompted, in exactly this form, which the directory takes as the tier explaining itself.

**[J-86] Wheelhouse Round** — N-GR-30's memory in the flywheel, then N-ST-08's lock through the works at shutdown. Spin, then still; millwrights' guilds close every working day with the pairing and open every apprenticeship with the reason.

**[J-87] Last Lamp Discipline** — N-EM-15 down the hall's lamps in order, N-WK-10's low watch-glow raised at the final door. Extinguish, then keep one honest light — the night-porter's pairing, catalogued last in this tier deliberately: two Novice castings, held apart cleanly, and somewhere behind them a building sleeps because the windows never touched. That, in one round, is Journeyman.

#### Adept (Uncommon) — 34 entries

*Still no seventh pair, and never will be: every entry below deepens one of the six solved `Chi(f1,f2)` pairs of AD-01 through AD-06, named per entry, under Eq. 4.15's `Fid^2` accounting. Expansion I's ordering convention — trade toward battlefield within each pair — carries forward.*

*(EM + Strong — the Flash-Forge pair, AD-01)*

**[AD-41] Riveter's Rain**
*(EM + Strong)* — rivets heated and set in one blended stroke apiece, a crew's day of hammer-and-dolly work falling in a steady patter from one Adept's scaffold. Shipyards and bridge works bid for holders by the thousand-rivet lot; the entry's name is what a finished span sounds like going up.

**[AD-42] Cold Shear**
*(EM + Strong)* — deep chill and a brittle line blended through hot or heavy stock, cutting foundry sprues and forged flash clean without a second heat. The pair's subtractive face, as AD-08's kiss is its healing one; finishing shops rank a holder above any three saws they own.

**[AD-43] Glassblower's Third Lung**
*(EM + Strong)* — a gather's heat and its cohesion held in one blend while the piece is worked — the bubble's wall kept even past what breath and gravity would allow. Named by the trade, catalogued by the directory, and coveted by every glasshouse that has watched a masterpiece slump at the last turn.

**[AD-44] Farrier's Minute**
*(EM + Strong)* — a shoe brought to fitting heat and its nail-seats bind-eased in one pass at the anvil, the whole fitting done inside the animal's patience. The pair's homeliest deepening, and among its most hired; cavalry quartermasters, who ranked AR-18 above farriery, rank this beside both.

**[AD-45] The Patient Anvil**
*(EM + Strong)* — a workpiece held soft *only where the hammer falls*, hard everywhere else, the blend walking with the smith's rhythm. Master-smiths who hold it describe forging "with the metal's consent"; examiners describe it as the pair's finest `Fid^2` test, since the softened zone must move without ever widening.

**[AD-46] Chainwright's Song**
*(EM + Strong)* — link after link heated, closed, and bound in an unbroken worked rhythm — anchor chain proofed as it forms rather than after. The trade sings the pace, hence the name; navies buy the chain, and the directory notes that the song's tempo is, precisely, the caster's sustainable `Fid^2`.

*(EM + Gravity — the Storm-Step pair, AD-02)*

**[AD-47] Kingfisher's Grace**
*(EM + Gravity)* — a controlled plunge and a stunning discharge blended at the entry — fisher-folk's deep strike, rescue crews' fast descent to a drowning grip. The pair's original courier blend (AD-02) turned vertical; coastal traditions dispute which came first and the directory declines the honor of ruling.

**[AD-48] Cage Whisper**
*(EM + Gravity)* — a mine cage's whole descent eased and lit as one held blend, Lampfall's (AD-17) logic carried from the glow ahead of the crew to the crew, the cage, and the light together. Deep mines' standard-bearer technique now, as AD-17 was its herald; the two entries share a guild toast.

**[AD-49] Dust Pillar**
*(EM + Gravity)* — charged dust or spray lifted into a standing, visible column — a signal that needs no fuel, a survey mark that needs no tower, a warning legible for miles. The pair's answer to N-EM-41 at institutional scale; caravan roads in dry country are strung with the memory of where pillars stood.

**[AD-50] The Gentle Volley**
*(EM + Gravity)* — thrown rescue lines, grapnels, or supply casks lightened in flight and sparked visible against dark water or night air. AD-15's crowd logic turned seaward and civic; lifeboat stations examine for it, and the examination is conducted, by unbroken tradition, in weather no one would choose.

**[AD-51] Chandelier Descent**
*(EM + Gravity)* — a great lit fixture lowered burning through its own hall, flames steady, weight feathered, one blend from vault to floor. Opera houses and cathedrals hire it seasonally; the directory catalogs it as the pair's purest showpiece — and notes that showpieces, cast before a thousand witnesses, have recruited more Adepts than any treatise.

**[AD-52] Skater's Edge**
*(EM + Gravity)* — the caster's own weight eased and a thin melt-line warmed beneath the stride — long, impossible glides over rough or doubtful ice. Winter couriers' deepening of AD-02's leap into a sustained gait; fen and lake countries license it like a horse, which is to say jealously.

*(EM + Weak — the Cinder-Fall pair, AD-03)*

**[AD-53] Physician's Lantern**
*(EM + Weak)* — AD-21's assay logic turned to the living: a diagnostic glow-read and a fine heat-read blended into one passing touch — fever's depth, a wound's hidden heat, a lung's wet weight, judged together. The blend behind every story of a healer who "sees" illness; the stories are exaggerated, the waiting lists are not.

**[AD-54] Foundry's Dawn**
*(EM + Weak)* — Forge From Nothing (AD-19) at industrial patience: a smelting fire raised and self-fed on waste coke, culm, and scrap-heat until the pour. Iron districts in poor-coal country run on holders of it; their guild's arms are, exactly, a sunrise over a slag heap, and the directory finds the heraldry honest.

**[AD-55] Beacon of the Interior**
*(EM + Weak)* — Watchman's Dawn (AD-20) scaled to a landlocked light: a tower glow steady for a season on a lamp-room's worth of fuel, marking passes, fords, and desert wells. The lighthouse's inland cousin; the orders that keep them call themselves keepers without qualification, and coastal keepers, notably, do not argue.

**[AD-56] The Slow Star**
*(EM + Weak)* — Slow Match's (AD-22) civic twin: a signal light kindled now to *brighten* at a chosen hour — a rendezvous that announces itself, a curfew that needs no crier. Garrisons and festival marshals share the technique with equal enthusiasm and profoundly different paperwork.

**[AD-57] Curing House Writ**
*(EM + Weak)* — smoke-house heat and the cure's slow chemistry blended and tuned together, whole racks brought through in days without a false note of spoilage. The pair's quartermaster tradition (AD-19, AD-33) at the smokehouse door; ham country hangs a holder's mark on the lintel and means it as armorial.

*(Gravity + Strong — the Sunder Weight pair, AD-04)*

**[AD-58] Bridge of a Day**
*(Gravity + Strong)* — felled timber lightened for the throw and bind-proofed at the lashings, a gorge crossed by noon and the span *held* until the last cart is over. Field engineers' signature blend; the release at day's end is ceremonial in most companies, and the ceremony is attended.

**[AD-59] The Held Roof**
*(Gravity + Strong)* — a mine gallery's burden eased into its props while prop and rock are bind-boosted as one standing blend. Rescue's first casting after any fall, and working mines' quiet daily one; Cage Whisper (AD-48) carries the crew, this carries what's above them, and deep-country guilds examine the two as a single subject.

**[AD-60] Cargo Writ**
*(Gravity + Strong)* — a hold's whole lading lightened to the hull's ease and lashed by binding in one casting — Anchor Absolute's (AD-29) cargo-side twin. Storm latitudes price the writ into freight; the directory notes that "written cargo," in port slang, now simply means *safe*.

**[AD-61] Well-Digger's Faith**
*(Gravity + Strong)* — the unfinished shaft's walls bind-held while the spoil bucket rises featherweight past the digger — one blend, two mercies, all day. N-ST-27 and N-GR-10's work fused and deepened; the trade's first rule (*no descent unwarded*) now has a second verse, and both scan.

**[AD-62] Icefall Warden**
*(Gravity + Strong)* — a glacier route's worst séracs eased of their weight-argument and bind-steadied through the crossing hours — AD-30's avalanche judgment carried onto ice that falls by the tower rather than the slope. High-route hospices roster one holder per season, and name the season for them.

**[AD-63] The Long Lever**
*(Gravity + Strong)* — bar, fulcrum, and load blended as one problem: the pry-bar bind-proofed, the load's weight eased at the bite, seized machinery and fallen lintels arguing with arithmetic and losing. Wreckers, millwrights, and rescue crews hold it in common; the directory catalogs it as the pair's plainest statement of purpose.

*(Strong + Weak — the Quiet Mend pair, AD-05)*

**[AD-64] Field Hospital Writ**
*(Strong + Weak)* — Surgeon's Hold (AD-32) held not at one grave wound but across a tent-row's worth in triage — binds boosted, decay arrested, patient by patient under one sustained inscription walked down the line. The tier's heaviest documented `Fid^2` burden in sustained use; traditions that hold it rotate casters by the hour and chapter their histories by the nights it was needed.

**[AD-65] Brewer's Covenant**
*(Strong + Weak)* — a fermentation's vessel binds held while every spoilage pathway around the working culture is slowed — the culture's own change untouched, its rivals' forbidden. The blend's finest discrimination exercise; brewing dynasties guard their holders like their yeasts, and the directory suspects the priorities are correctly ordered.

**[AD-66] The Standing Orchard**
*(Strong + Weak)* — AD-34's rot-fence held not for a judgment's hour but as a season's standing writ across a whole planting — blight met at a maintained line while the sound wood is kept bound against it. The Adept-tier ancestor of M-12's quarantine precision, catalogued as such; orchard wardens who hold it stop attending rural courts and start convening them.

**[AD-67] Relic Road**
*(Strong + Weak)* — Reliquary Seal (AD-31) made portable: the seal-blend sustained on a fragile burden *through* a journey — a relic, an archive, a body going home — renewed at every halt by the same hand. Pilgrim ways and diplomatic pouches both run on it; the seal-books of moving seals are, librarians attest, the tier's most traveled documents.

**[AD-68] Sap Still**
*(Strong + Weak)* — a tapped stand's vessels bind-held while the sap's souring is slowed through the run — syrup and resin country's answer to AD-33, drawn from living wood rather than a ship's hold. The pair's gentlest industrial face; sugarbush families hold it in the same hereditary way as AR-31's horn-craft, outside any guild at all.

*(Gravity + Weak — the Grave Lantern pair, AD-06)*

**[AD-69] Canary Light**
*(Gravity + Weak)* — a glowing mote held at neutral buoyancy in a mine gallery's air: where the air thins or fouls, the blend's balance shifts and the light *sinks*. The pair's life-saving masterpiece — a lamp that faints before the miner does — and the entry most cited when this ceremonial-seeming pair is called the directory's most underestimated.

**[AD-70] Harbor Constellation**
*(Gravity + Weak)* — Beacon Buoy (AD-39) held not singly but as a fielded pattern — a channel's whole night-shape drawn in unquenchable, station-keeping lights under one renewing casting. Port cities charter holders the way they charter pilots; the pattern's name in every log is simply *the stars*, and making them is the job's title.

**[AD-71] The Weightless Ward**
*(Gravity + Weak)* — Sickroom logic at the pair's full depth: patients eased in their own weight while ward-lights hold at every bed — W-09's mercy rendered portable, one hall at a time, wherever no Warden's proven floor exists. Hospice orders rank the blend above any single mercy in this catalog; the directory, reviewing the tier, does not correct them.

**[AD-72] Night Sowing**
*(Gravity + Weak)* — broadcast seed lightened into a long, even hang while a faint glow marks the sown swaths — planting that outruns the daylight in a short spring. Northern valleys hold the blend communally, one Adept to a district; the sowing nights are festivals, and the directory notes the festivals are older than the district maps.

**[AD-73] Ferryman's Lantern**
*(Gravity + Weak)* — a skiff eased in the water's grip while a stern-light burns unquenchable through fog and rain — the crossing trade's whole burden in one blend. Every river with a name has a story about this casting; most of the stories are true, which the directory records as the pair's quiet distinction.

**[AD-74] Deep Grave Honors**
*(Gravity + Weak)* — Grave Lantern's rite carried to sea burial: the shrouded weight lowered slow and even, a glow riding it down past sight. The pair's founding ceremony (AD-06) completed in its last element; naval traditions hold that the light must be *held to the end of sensing*, and Bearing Sense (N-EM-29), the directory notes, is why the phrase has a measurable meaning.

#### Artisan (Uncommon) — 26 entries

*One signature material per entry — one solved eigenvector family in `S` (Eq. 3.1e, 4.16) — with its unmodeled neighbors named, per the tradition of the tier's every prior entry, as the Eq. 4.17 warnings they are.*

**[AR-34] Artisan of Slate** — solved for slate's cleaving structure: roofing split to whisper-thin true, writing-slates surfaced smooth, a quarry's beds read like a book's spine. Shale — slate's unfinished cousin — is unmodeled, and roofing country's guilds keep a list of those who reasoned otherwise.

**[AR-35] Artisan of Flint** — solved for flint and chert's conchoidal structure: strike-steels' partners shaped true, gun-flints? — no, *fire-flints* — knapped by the gross, N-ST-28's consent deepened into command. Obsidian, that other glassy stone, belongs to AR-28, and the two specialties' mutual warning is carved, jointly, over one shared guildhall door.

**[AR-36] Artisan of Plaster** — solved for gypsum plaster's setting structure: walls cured without crack, casts taken finer than the face they copy, ceilings' ornament run in place. Lime mortar sets by a stranger chemistry and a stranger eigenvector; the two trades share scaffolds and, pointedly, nothing else.

**[AR-37] Artisan of Brick** — solved for one fired clay body at brick scale — AR-07's kiln-craft carried past the vessel to the wall: bricks trued after bad firing, bonds healed in standing work, whole courses proofed against frost-spall. Terracotta and tile are near neighbors and separate proofs; builders' orders fund all three and audit which is which.

**[AR-38] Artisan of Linen** — solved for flax fiber's structure: cloth proofed against mildew on the loom, heirloom lace un-yellowed, sailcloth's weave tightened to hold a stiffer wind. Cotton and hemp answer to other eigenvectors; the linen guilds' examination opens, traditionally, with a blindfolded touch-test the eigenvector itself makes trivial.

**[AR-39] Artisan of Cordage** — solved for laid hempen rope *as a structure* — the lay, not the fiber: splices set true, worked rigging's stretch retired, a cable's hidden wring found and eased. Wire rope, when it comes, will be someone else's proof; the ropewalks say so with a serenity the directory finds premature and records anyway.

**[AR-40] Artisan of Sinew** — solved for sinew and gut's bound structure: bowstrings that keep their voice through weather, sutures' material proofed, instrument strings trued to a maker's exact intent. Living tissue remains, per AR-33's stark clause, absolutely elsewhere; every charter in this specialty cites that entry's first clause verbatim.

**[AR-41] Artisan of Ivory** — solved for dentine's layered structure: carvings healed of age-checks, piano-scale? — keyboard veneers laid seamless, a broken heirloom made whole to the grain. Bone is AR-03's solved country and horn AR-31's; the three specialties' joint examination on *telling them apart at touch* is the trade's oldest and most failed.

**[AR-42] Artisan of Coral** — solved for one reef-coral's stony skeleton: jewelry healed, carved amulets proofed against wear, and — the specialty's quiet judicial use — worked coral dated and sourced by its growth structure. Pearl's nacre is AR-29's; the two maritime eigenvectors share divers, markets, and a firm mutual boundary.

**[AR-43] Artisan of Jet** — solved for jet's fossil-wood structure: mourning-pieces polished from within, carvings proofed against the cracking that dry rooms inflict, false jet unmasked at a touch. Amber, that *other* fossil gem, is AR-24's solved subject — and the two trades' shared customers in grief have made their two guilds, unusually, genuine friends.

**[AR-44] Artisan of Crucible Steel** — solved for one named crucible steel — proof, after AR-12 and AR-27, that the *made-material* precedent now anchors the tier: blades trued and tempers tuned past any forge's reach, but only in that steel. Iron entire remains AR-02's country; every other steel remains Eq. 4.17's. The smelting town that holds the proof stamps its billets with the eigenvector's proving date, and the stamp is the price.

**[AR-45] Artisan of Pewter** — solved for one tin-lead table alloy: dents healed at a touch, tankards re-trued, the sad gray bloom of age reversed. AR-11's tin-rot command does not transfer — the alloy is its own eigenvector, as the tier's every alloy entry retells — and pewterers' marks now record *which* proof a piece was worked under, which assayers quietly love.

**[AR-46] Artisan of Brass** — solved for one founding-brass ratio: instrument valves fitted past machining's patience, bells and horns tuned in the metal, corrosion turned back at the surface. Bronze is AR-12's ratio and copper AR-08's element; the three coppery eigenvectors are the guild examiners' favorite Eq. 4.17 question, and the answer's first word is *no*.

**[AR-47] Artisan of Quicksilver** — solved for mercury's liquid structure: instrument columns purged of flaw, amalgams worked and un-worked cleanly, spills gathered to a bead at a gesture. The specialty's charters mandate more safety clauses than any three others combined; the directory reproduces none and endorses all.

**[AR-48] Artisan of Sulfur** — solved for native sulfur's crystal structure: purification past any refiner's art, fumigants shaped and dosed, vulcanizing? — the trades to come are the trades to come; the proof waits ready. Match-work and powder-work touch this eigenvector's markets at their edges, and the specialty's guilds, notably, decline both by charter.

**[AR-49] Artisan of Alum** — solved for alum's crystal structure: mordants proofed pure so dye-lots never betray a cloth-hall, papermakers' sizing trued, tanners' white leather made honestly white. The homeliest chemical eigenvector and among the most lucrative; dye-country banks, the directory notes, have twice been founded on one practitioner's proof.

**[AR-50] Artisan of Parchment** — solved for prepared skin *as a writing ground* — distinct from AR-18's worked leather and AR-14's felted paper, a boundary all three guilds patrol: cockled leaves relaxed flat, hair-side and flesh-side balanced, a palimpsest's ghost text raised or laid to rest. Chanceries and archives divide the world's old documents among these three specialties, and the dividing itself is a licensed profession.

**[AR-51] Artisan of Cork** — solved for cork's cellular structure: seals sized to a wine's exact breathing, floats proofed against waterlogging, whole harvest-planks trued. The oak *tree* is AR-13's solved timber; its bark is this separate proof — the directory's tidiest demonstration that an eigenvector follows structure, not species, and examiners use it exactly so.

**[AR-52] Artisan of Resin** — solved for fresh conifer resin's structure: varnishes tuned to a luthier's ear, incense graded past any nose's dispute, wound-dressings' old recipes made reliable. Fossil amber is AR-24's, wood-tar pitch AR-26's — the resin line's three ages, three proofs, and the tier's standing lecture on time itself as an Eq. 4.17 boundary.

**[AR-53] Artisan of Tallow** — solved for rendered fat's structure: candles that burn even and smokeless, soap-stock split clean, lamp-tallow proofed against rancid seasons. AR-04's rot-craft prepares what this specialty then commands — the two share a rendering-yard and a boundary line down its middle, drawn, by old custom, in tallow.

**[AR-54] Artisan of Honey** — solved for honey's dense sugar structure: crystallization commanded either direction, adulteration unmasked at a touch, medicinal grades proofed and kept. Beeswax is AR-25's solved country; the hive thus supports two entire specialties, and beekeeping regions, reasonably, believe the arrangement is the bees' own opinion of Artisans.

**[AR-55] Artisan of Soap** — solved for one saponified structure: laundry-stock that rinses true in hard water, surgeon's soap proofed pure, a luxury trade's marbling worked from within. The specialty's proof is younger than most of its customers' guilds; the directory catalogs it as the tier's newest widely-held eigenvector, and its examiners as the tier's most cheerful.

**[AR-56] Artisan of Indigo** — solved for indigo's dye structure through the vat's whole cycle: reduction judged truly, blues struck even across a bolt-run, a vat revived that any dyer would have mourned. Woad's kindred blue is a kindred, *separate* proof; the two dye countries' rivalry predates both eigenvectors and has merely, as one master put it, acquired mathematics.

**[AR-57] Artisan of Peat** — solved for cut peat's compacted structure: fuel-turves dried and graded to burn long, bog-finds stabilized the hour they meet air, a working face read for its best cutting. Coal is a deeper time and a different proof; bog country holds this eigenvector communally, half fuel-craft, half archaeology, and its holders answer to both callings by turf-law.

**[AR-58] Artisan of Sea-Coal** — solved for one seam's bituminous structure: firing graded to the forge's need, sulfurous fractions sorted at a touch, colliers' cargoes certified honest. A neighboring seam is, by now predictably, a neighboring proof — and the coal-ports' assay houses keep both proofs on staff and the difference on a posted placard, which the directory reproduces in spirit here.

**[AR-59] Artisan of Mother-of-Vinegar** — solved for the vinegar culture's bound structure — the tier's second *living-adjacent* proof after AR-04's pathways, and bounded by the same hard clause: the culture as worked material, never as creature. Vinegar-lofts proofed against failure, sour trades' stocks revived, and a boundary with AR-04 so fine that the two specialties examine each other's candidates, by treaty, to keep it.

#### Master (Rare) — 16 entries

*Complete-`S` workings all (Eq. 4.18–4.19), in the tier's established registers: civic first, extraordinary later, spectacle never for its own sake.*

**[M-19] The Sweet Well** — brackish or sea-spoiled water re-expressed sweet across a cistern or a fleet's casks (Eq. 4.18 at the dissolved fraction) — M-03's purification carried past settling into true unwriting of the salt itself. Island garrisons and drought courts rank it first among the tier's workings, and the directory, reviewing the tier's petitions ledger, concurs.

**[M-20] The Breathing Mine** — fire-damp and choke-damp re-expressed inert through a gallery's air before the shift descends. AD-69's canary light warns; this working removes the thing warned of. Deep-country mining law in two nations requires a Master's writ for the gassiest seams, and prices the writ against the alternative in a preamble nobody has ever called excessive.

**[M-21] Wright's Century** — green timber seasoned through decades of settling in a day's casting (Eq. 4.19's controlled hastening, staged as The Long Table stages a cellar). Shipyards and instrument-makers alike book it years out; AR-13's oak-craft trues what this working matures, and the two callings' joint waiting-list is the timber trade's true calendar.

**[M-22] The Honest Coin** — a debased coinage audited and re-expressed true at mint scale — assay (M-11) and correction (Eq. 4.18) as one working under crown witness. Three currency crises in the historical record end with this entry's date in the margin; the directory notes that the working's *announcement* has twice sufficed, which is its own kind of complete eigenbasis.

**[M-23] Wound-Glass** — shrapnel, shot, and splinter re-expressed as harmless bulk *in situ*, drawn or dissolved without the knife's long search. M-09's targeting discipline turned from venom to debris; battlefield chapters of the mending orders count it beside Mender's Completion (M-08), and their casualty rolls, before and after its proving, read like different wars.

**[M-24] The Patient Reef** — harbor stone grown course by course from sea-floor rubble, bound and re-expressed toward a breakwater's need across patient years. A Master's answer to what Wardens ease (W-07) and Legends still (LG-06): not calming the water but giving it something honest to argue with. Port charters call the working by its schedule — *the courses* — and fund it by the storm.

**[M-25] The Kind Harvest** — famine stores' bitter, binding, or poisonous fractions unwritten at the granary door — acorn, vetch, and worse rendered food in a hungry season (Eq. 4.18, discriminated as finely as M-06 stages a cellar). The tier's famine-country twin to Field's Restitution (M-10): that working mends next year, this one mends tonight.

**[M-26] Bell Metal Voice** — a cracked great bell re-expressed whole *in the tower*, its founding alloy and its voice restored without descent or recasting. AR-12 and AR-46's bell-crafts end where their ratios do; a Master's complete basis does not, and campanology's histories keep a separate, reverent list of towers so mended and the dates they spoke again.

**[M-27] The Unrusting Charge** — Rust's Recall (M-07) held as a standing, renewed writ across a whole arsenal, fleet, or bridge inventory — corrosion not repaired but *forbidden*, on a recertification calendar the directory notes is drawn, explicitly and by precedent, from AD-31's seal-books. The tier's plainest institutional working, and among its most quietly expensive to lapse.

**[M-28] Chirurgeon's Match** — donor tissue's rejecting fractions eased toward a patient's own expression at the graft (Eq. 4.18 at its most exactingly discriminated) — the mending orders' deepest ordinary working, chartered everywhere under M-08's same honest clause: it completes mending; it does not return what has ended. The clause is read aloud, by rule, before every casting, and the reading is part of the working.

**[M-29] The Cleansing Reach** — a poisoned or tannery-fouled river re-expressed clean along a settlement's whole reach, the taint unwritten faster than the current re-supplies it, until the source is found and stopped. M-03 at landscape patience; river courts convene *around* the casting, upstream of it, which the directory records as the working's true design.

**[M-30] Founder's Silence** — a working forge, mill, or magazine's ambient hazards — sparks' tinder, dust's temper, fume's edge — kept re-expressed inert through the working day, a Master's standing presence worn like the building's own held breath. Industrial towns that can retain one for this call the retainer *the quiet*, and account it, correctly, as infrastructure.

**[M-31] The Ledger of Stone** — boundary stones, treaty steles, and founding inscriptions proofed against a thousand years — their matter re-expressed toward permanence (Eq. 4.19, `s = -1`, held deep) under seals the law can trust. M-14's forensic honesty turned monumental; surveyors, archivists, and rival heirs all sleep better, which the directory offers as the tier's working definition of civic magic.

**[M-32] The Gleaner's Writ** — spent fields' straw, chaff, and orchard-fall re-expressed toward fodder, thatch-stock, and bedding as the season needs — waste unwritten into use at estate scale. The humblest complete-basis working in the catalog, and the one its holders most often cite when asked, at examination, why they solved the last eigenvector: *because the whole point was everything*.

**[M-33] Glazier's Sand** — optical glass raised flawless from raw shore sand (Eq. 4.18 through the melt's every fraction) — lens blanks past any furnace's honesty, mirror-stock without a seed of ruin in it. AR-05 shapes what exists and AR-20 trues crystal's cousins; this working makes the existence. Observatory patrons fund it by the casting, and astronomy's history, the directory notes, keeps its own list of the dates.

**[M-34] The Sleeping Ground** — plague-pits, battle-grounds, and poisoned works rendered permanently inert and clean — remains honored, taints unwritten, soil restored to the living's use (M-14's dignity, M-15's restitution, one working). Every tradition that holds it holds it last in training and first in honor; the directory follows suit, and closes the tier with it.

#### Warden (Very Rare) — 12 entries

*Catalogable, as ever, only where the proof genuinely transfers — a standardized geometry or an institution old enough to hold one (Expansion I's proof-standard principle). One named geometry per entry; every entry ends at `eps_valid(R_proven)` (Eq. 4.21), and none pretends otherwise.*

**[W-14] Weir Keeper's Palm** — one mill-weir's mapped race eased at the sluice, the water's argument with the gate gentled through flood hours. Proven for that weir's exact fall; the milling order that holds it builds new weirs to the proven fall's gauge — mercy-width's (W-03) river cousin, and the second Warden proof ever standardized on purpose.

**[W-15] The Gentle Portcullis** — a fortress gate's drop eased along its mapped channel for drill and maintenance, and *only* its proven channel — released to honest gravity in anger. The proof transfers to gates built to the founding castle's published gauge, which is why four unrelated fortresses share a portcullis and a Warden's calendar.

**[W-16] Fly-Loft Grace** — a playhouse's rigging loft and stage-drop eased within one mapped house — falls slowed, flown scenery gentled, the deadliest room in theater made survivable. The touring proof transfers only between houses built to the proof-standard stage, which is why that standard exists, and why actors, uniquely among artists, bless a building's *dimensions*.

**[W-17] The Kindly Scaffold** — falls slowed within one standardized scaffold frame's mapped envelope — the building trades' answer to W-06's training circle, bought not with a school's generations but with a published frame gauge and a guild's discipline in never deviating from it. Erected, certified, eased; the certificate is nailed to the frame, and the nail, by trade humor, is load-bearing.

**[W-18] Ringer's Tower** — one bell-tower's mapped swing-path eased at the great bell's hardest arc — N-GR-20's mercy made standing, for every band the tower will ever host. Proven per tower; the change-ringing societies' proof-standard tower gauge has spread it to nine, and the societies count the nine the way navies count ships.

**[W-19] The Steady Cradle** — a dry-dock's mapped cradle eased as the hull settles — the shoring's worst hour gentled along one proven geometry. Tied to the dock, not the ship, per the tier's iron rule about what a geometry is; the yards' apprentices learn that distinction here first, and the directory approves of where they learn it.

**[W-20] Granary Breath** — a tower silo's mapped wall-line eased of the grain-mass's press at filling — burst risk retired along one proven vertical. The proof transfers to silos raised on the founding tower's gauge; grain districts now build to it as reflexively as they roof, which is the proof-standard principle grown quietly universal.

**[W-21] The Long Ladder** — one deep mine's mapped ladderway eased through its worst pitches — the climb-out gentled for spent crews along the shaft the proof knows. W-03 slows the fall; this spares the climb. The mining order holds both proofs as one duty, and sinks, per mercy-width's precedent, every new ladderway to the proven gauge.

**[W-22] Pilgrim's Rest** — one shrine's mapped stair eased for the infirm on festival days — the climb's cost gentled along the proven flights, and only there. The shrine's order publishes the casting's calendar beside the liturgical one; W-13's open-ledger example is cited in their charter, and the directory notes the citation with something like pride.

**[W-23] The Proving Floor** — an assay office's mapped floor where dropped samples, weights, and vessels fall slow — a room that forgives the one profession least able to afford accidents. Proven per office, spread by the proof-standard plan; weigh-house architects now letter the plan's edition in the doorstone, which assayers read the way sailors read a hull's lines.

**[W-24] The Gated Current** — a canal lock's mapped chamber eased at fill and draw — the water's rush gentled, the moored hull's surge tamed, along one proven basin. Tied per chamber; the canal companies' shared lock-gauge has carried the proof down three watersheds, and lock-keepers' manuals open with the casting and close with the `eps` ledger.

**[W-25] The Last Door** — one hospice's mapped threshold eased for the bearing-out — the final carry gentled across a doorway the order has held proven for two hundred years. W-13's contemplative register, one door wide; the order publishes nothing, explains nothing, and re-proves the threshold each spring, which the directory records as a complete account of Warden tier in three clauses.

#### Legend (A Handful Across Recorded History) — 8 entries

*Sovereign mathematics unchanged, held at Eq. 3.1g's furthest dials; institutions all, because Eq. 4.22–4.23's upkeep permits nothing less. History's names, the Codex's mathematics.*

**[LG-11] The Twin Markets** — a standing fold-pair joining two cities' market squares, held *open on market days only* — the tier's one great scheduled fold, its identification re-validated in the closed days between (Eq. 4.22's `t_drift` cadence built into the week itself). The two cities share a calendar, a currency, and a drift-order seated in both; economists date the region's history from the first market crossed.

**[LG-12] The Slow Avalanche** — a mountainside's catastrophic slide arrested mid-fall and held — a cliff of falling snow and stone standing at a lean no geology permits, generation after generation. Raised in one afternoon to spare a valley; maintained since by an order whose re-survey cadence is the mountain's own settling. Pilgrims come to see gravity told *not yet*; the order's records call the working, simply, *the postponement*.

**[LG-13] The Sanctuary of Hours** — a walled close under standing slow-time — days inside to the outside's weeks — where the hunted, the grieving, and the spent step out of the world's pace by right of an old charter. LG-04 banks records against time; this banks *people*, briefly, mercifully. Its drift-order audits the dilation against the charter's exact grant, for the tier's usual reason: at these dials, an error is a history.

**[LG-14] The Cradled City** — one city under a standing whisper of eased falls — roof-slips, scaffold-drops, and stumbles gentled everywhere within the walls, W-06's circle grown to a skyline. The founding Legend's civic gift; the maintaining order re-surveys ward by ward on a rota older than the city's parishes, and the city's masons, famously, still rope and scaffold as if the mercy were not there — which the order's charter, in its first clause, requires them to be taught.

**[LG-15] The Drowned Star** — a Bound Singularity (Eq. 4.12) held beneath a strait's approaches, its worked currents a standing defense no fleet has ever forced — LG-07's tidal engine turned to a realm's lock and key. Its tide-wardens recertify the shell (Eq. 4.23) on a cadence set by treaty among the powers it deters, which the directory records as the tier's driest joke and soundest peace.

**[LG-16] The Raised River** — a river carried along a ridgeline in a standing channel of eased and guided weight — an aqueduct of curvature, watering three duchies from a valley none of them owns. Its drift-order's re-survey cadence follows the river's own silt; the water-law that grew around the working fills nine volumes, and the working itself, one line of Eq. 3.1g's dials, which the jurists cite with visible resentment.

**[LG-17] The Hanging Terraces** — a mountain city's fields stacked in standing eased-weight tiers — soil, water, and harvest carried on curvature where no slope would hold them. The granary of a cold kingdom and the tier's most *inhabited* working: ten thousand people farm inside it daily. Its maintaining order examines Wardens into its service by the hundred-year ledger, and promotes, by charter, only the bored — vigilance, their maxim runs, is a habit, not a mood.

**[LG-18] The Far-Seeing Ridge** — a border ridge under a standing lens of curvature — light's own paths bent so the watchtowers see over the horizon's argument, a march's whole approach laid open to plain sight. The subtlest working in the tier's catalog: nothing moves, nothing weighs less, and nothing crosses unseen. Its drift-order are surveyors to a soul; their re-validation cadence is the starfield itself, read nightly against the lens, which the directory notes is Eq. 4.22 practiced as astronomy.

#### Beyond Legend (Historical Fragments) — 4 entries

*Fragments, not curriculum, as ever: documented attempts along §3.3's four paths, audited by Eq. 4.24–4.27, catalogued for what each proves about the distance.*

**[AS-07] The Unnamed Orchard** — a Demiurge aspirant's proven extrapolation rule along one living family: cultivar after cultivar derived from solved stock, each verified, none ever before grown — `N_family` (Eq. 4.25) driven high through *orchards* rather than alloys. The estate still bears fruit no wild lineage explains. The aspirant's final notebook closes the fragment as AS-03's did, in different ink: the rule's family fed a province; the rule of rules fed nothing but the wanting of it.

**[AS-08] The Ceded Ring** — a Cosmographer aspirant who, confronting AS-04's ledger, tried the other ledger line: *releasing* proven domain at one edge to afford extension at another — `rho_cosmo` (Eq. 4.26) held constant while its shape was walked across a continent over a lifetime. The campaign proved a bitter theorem the equations had merely implied: the propagator's self-dependence (Eq. 1.4) taxes the release too. Ground given back does not un-complicate what its solving complicated. The ring moved; the price compounded; the fragment stands as the path's second ledger, and its lesson is the first ledger's, twice.

**[AS-09] The Weather of One Hand** — a Tetrarch fragment complementary to AS-01's speed and AS-05's stillness: an aspirant who expressed one modest effect — a held warmth over a winter camp — through each of the four forces *in rotation*, nightly, for a season, indistinguishably to everyone warmed. Witnesses could not say which force served on which night; Eq. 4.24's audit could, which is the fragment's whole content. Four servants in perfect livery are not one master, however long the season — and the camp, the records note, was warm all the same.

**[AS-10] The Two-Mind Bridge** — the smallest Communion in the historical record: two lifelong collaborators who pooled their proven domains (Eq. 4.27) for a bounded working season each year, dissolving cleanly each autumn, for forty-one years. `N_comm` barely exceeded one middling Sovereign's measure; nothing about it was vast. The fragment is catalogued for what the sealed accounts of AS-06 are not: a Communion entered, held, and *ended*, repeatedly, by two minds that remained two. The traditions that keep the record disagree on whether it marks the path's one safe door or its subtlest warning, and the directory — as with every question this tier asks — records the disagreement and closes the catalog.
