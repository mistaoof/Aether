# THE AETHER CODEX — Applied Techniques: Novice Tier
### Part 4 Preamble · §4.0 Novice Techniques

*Part of the Aether Codex reference set — see `codex/overview.md` for the file map. All § and Eq. numbers are global across the Codex. Sovereign-tier techniques (§4.1–§4.3) are housed in `codex/techniques-sovereign.md`; Legend-tier techniques (§4.10) in `codex/techniques-legend.md`; the Spell Directory (§4.4) in `codex/spell-directory.md`.*

---

## 4. Applied Techniques

Every technique below is an instance of the same three-step chain formalized in §1.2–§1.3: source a ripple (`J_cast`), propagate it (`G`), and couple it into one of the three channels above (`delta(F_f)`, `delta(M_op)`, `delta(g)`). Most entries compress this chain into a single closed-form line, the way ordinary practice always does — no caster consciously reasons through a propagator integral to boil a kettle. §4.0 walks the chain in full once, for Eq. 4.0a, so that the shorthand used everywhere else in this Part can be read with the underlying mechanism in mind rather than as an unexplained set of coincidentally similar formulas.

### 4.0 Novice Techniques

This section marks the start of the applied curriculum proper — the point where a student moves from reading the Grand Equation's structure (§3) to actually casting from it. Every technique here uses exactly one term from Eq. 3.1c, in closed form, with no combination and no metric-level involvement. The same terms reappear, in far more complete form, throughout the rest of Part 4; the throughline is deliberate — lifting a pebble and binding a singularity both trace back to gravity, at opposite ends of the hierarchy (`k_grav` in Eq. 3.1c versus `Xi(Ae, g)`; see Eq. 4.0b's note).

**Eq. 4.0a — Thermal Excitation ("Boiling Water")**
```
P_in = k_EM * Fid * Ae_local^2
dT/dt = P_in / (m * c_p)
```
The caster concentrates aether density at a point of contact, `Ae_local`, and the electromagnetic coupling `k_EM` converts that into injected power, `P_in`. From there it's ordinary thermodynamics: temperature rises at a rate set by the substance's mass and specific heat capacity, exactly as if the energy had come from a stove rather than a caster. This is usually the first equation any aether student is taught, precisely because it has no failure mode worth naming — a low-`Fid` attempt just heats the water more slowly.

**From ripple to result.** It's worth tracing Eq. 4.0a back through §1.1–§1.3 once, in full, since every other technique in this document compresses the same chain of reasoning into a single closed-form line the way this one does. A caster inscribes a glyph or cadence that constitutes `J_cast(x', t')`, localized at the point of contact. Eq. 1.2 propagates this through the essentially flat, unperturbed geometry around an ordinary kettle — no metric distortion is involved, so the propagator `G` reduces here to its simplest, unperturbed form — producing a local perturbation `dAe(x, t) = Ae_local`, concentrated exactly where the caster intended. Eq. 1.3's gauge channel then converts that local perturbation into a distortion of the electromagnetic field-strength tensor, `delta(F_EM) = k_EM * Ae_local`, scaled by the fidelity of the sourcing current per Eq. 3.2. What Eq. 4.0a's `P_in = k_EM * Fid * Ae_local^2` actually represents is the power delivered by that distorted field once it couples to the water's own electromagnetic structure at the molecular level — the squared `Ae_local` reflects that the power delivered by a field is proportional to the square of the field's own strength, exactly as it would be for a coil or a flame. Everything after that line is ordinary thermodynamics, precisely because the ripple's job ends the moment it hands off a real, physical field distortion to physics that already knows what to do with one. This is the pattern every equation in the rest of this Part follows, whether or not it is spelled out again explicitly: source a ripple, propagate it, couple it into a channel, then let the receiving field behave exactly as it always would once genuinely disturbed.

**Eq. 4.0b — Minor Levitation ("Lifting a Feather")**
```
F_net = m_obj * g_local * (1 - k_grav * Fid)
```
`k_grav`, like the other three `k_f` terms in Eq. 3.1c, treats gravity as a simple force-coupling — enough to push, pull, or, as here, partially cancel a local pull. It cannot bend the metric itself; that requires `Xi(Ae, g)` (§3.3, §4.3). This is why lifting a pebble and generating the Bound Singularity's well (§4.3) both trace back to gravity but sit at opposite ends of the Power Hierarchy (§3.3) — one is a single closed-form term, the other is a partial solution to an entirely different piece of the Grand Equation.

**Eq. 4.0c — Minor Cohesion Boost ("Hardening a Surface")**
```
E_bind_eff = E_bind * (1 + k_strong * Fid)
```
A temporary, proportional boost to a material's ordinary binding energy — enough to resist a scratch or a minor impact better than it otherwise would. This is a single-term nudge to an existing property, not a rewrite of the material itself; true transmutation requires a fully diagonalized `M_op` (§3.3, §4.8), which is Master tier, not Novice.

**Eq. 4.0e — Ripple Sense ("Feeling a Working")**
```
S_detect(x, t) = k_EM * dAe_nearby(x, t)          -- read-only; no delta(F_EM) is sourced
```
The proven `k_EM` channel is not a one-way valve. The same coupling that lets a Novice push a distortion into the electromagnetic field also lets them notice one arriving from someone else's nearby casting — often well before it registers to an ordinary bystander as heat, light, or a felt static charge. This is a read, never a source: `S_detect` never itself becomes a `delta(F_EM)` in Eq. 1.3's sense, so neither Eq. 3.3's resolution threshold nor Eq. 1.3's fizzle/backlash distinction has anything to bite on here. A Novice can hold Ripple Sense continuously at zero risk — the cost is entirely informational rather than mechanical: this equation alone tells a caster *that* aether is moving nearby, not *whose* it is, what it's for, or whether it's friendly. Distinguishing those is a discipline built on top of this equation, not a further term inside it.

Adept- and Master-tier applied techniques are written up in `codex/techniques-adept.md` (§4.6) and `codex/techniques-master.md` (§4.8); Journeyman, Artisan, and Warden in their own respective files (§4.5, §4.7, §4.9) — see `codex/overview.md` for the full map. Every equation above is a single closed-form `k_f` term (or, for Eq. 4.0e, a passive read of one); the next stage up is holding more than one such term without a cross-term (Journeyman, §4.5), then combining them (Adept, §4.6); past that, the quark-sector `M_op` machinery from Eq. 3.1d opens partially (Artisan, §4.7) and then completely (Master, §4.8).

*Note: Eq. 4.0d (Decay Nudge), which completes the four-force set of Novice worked examples, is defined in the Spell Directory (`codex/spell-directory.md`, §4.4), where it was introduced.*
