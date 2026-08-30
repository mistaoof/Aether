# THE AETHER CODEX — Applied Techniques: Sovereign Tier
### §4.1 The Overlay Fold · §4.2 The Collapse Condition · §4.3 The Bound Singularity

*Part of the Aether Codex reference set — see `codex/overview.md` for the file map. All § and Eq. numbers are global across the Codex. The Part 4 preamble and Novice worked examples (§4.0) are housed in `codex/techniques-novice.md`. Eq. 3.1g is explicit that Sovereign and Legend "are the same mathematics at different scales... not different equations" — this file defines that mathematics once, at Sovereign's bounded scale; `codex/techniques-legend.md` (§4.10) extends the same constructions to Legend's effectively-permanent scale without re-deriving them.*

---

### 4.1 The Overlay Fold

The Overlay Fold relocates a caster from point A to point B without displacing mass. Rather than accelerating a body through space, it asserts a conformal identification between the two coordinates — establishing that, for the duration of the effect, A and B are the same point in the aether field — after which the caster's position resolves to the far side. At Sovereign scope, "for the duration of the effect" means a bounded hold: minutes to hours, per Eq. 3.1g's `R_dom`/`t_dom`, released once the caster arrives. A fold held open across years rather than hours is the same mathematics pushed to Legend scale (§4.10) — a different discipline of upkeep, not a different derivation.

**Eq. 4.1 — Overlay Identification**
```
Xi_overlay(A, B) = Ae*(A) * U_op(A, B) * Ae(B) - Delta( g(A) - Om2(x) * g(B) )
```

**Eq. 4.2 — Null-Displacement Constraint** (guarantees mass-neutrality)
```
Loop_traj[ (T_ae - T_mat) ] d(traj) = 0
```

| Symbol | Meaning |
|---|---|
| `U_op(A, B)` | Unitary phase-lock operator identifying point A with point B |
| `Delta(g(A) - Om2(x)*g(B))` | Forces the two local metrics to match, up to a conformal scale factor |
| `Om2(x)` | Conformal factor absorbing scale differences between A and B |
| `T_ae`, `T_mat` | Stress-energy tensors of the aether field and of the caster's body |

Three practical constraints follow directly from this mathematics rather than being imposed as separate rules. The destination's local metric must already be known to the caster, since `Om2(x)` in Eq. 4.1 cannot be computed for an unmeasured location. No momentum can be carried through the fold, since the null-displacement constraint in Eq. 4.2 requires the aether and matter stress-energy tensors to cancel exactly along the transition path. And the difficulty of a given fold scales with the magnitude of the conformal mismatch between A and B, so a jump between similar environments is markedly easier than one between, for instance, sea level and a mountain summit.

Per §3.5–§3.6, `U_op` itself is subject to both the Fidelity Principle and Unassisted Invocation: a sloppily inscribed fold uses the same equation but a weaker effective operator, and a sufficiently practiced caster can hold the fold open with a visualized `U_op` alone, with no visible casting tell.

In §1.3's terms, the Overlay Fold routes entirely through the metric channel: Eq. 4.1's `Delta(g(A) - Om2(x)*g(B))` term is a `delta(g)` distortion by another name, which is exactly why holding a fold open engages the self-referential propagator behavior described in §1.4 rather than the simpler, static channel behavior a Novice's `k_f` techniques enjoy. This is the mechanical reason a fold cannot simply be "aimed and released" the way Eq. 4.0a can: the moment `U_op(A, B)` begins identifying the two coordinates, the caster's own ripple is propagating through a geometry it is simultaneously reshaping, and everything that follows in §4.2 — the superposed state, the possibility of a fizzle, bleed, or backlash collapse — is what that self-referential propagation looks like while it is still in flight.

### 4.2 The Collapse Condition

While the identification operator `U_op` is active, the caster does not occupy A or B individually. They exist in a superposed state between the two.

**Eq. 4.3 — Superposed State Vector**
```
|Phi(t)> = a(t)|A> + b(t)|B>
|a|^2 + |b|^2 = 1
a(0) = 1,  b(0) = 0
```

**Eq. 4.4 — Fold Evolution** (how holding the fold shifts probability from A toward B)
```
i*hbar * d/dt [a; b] = [ [0, U_op(A,B)], [U_op(A,B)*, 0] ] * [a; b]
```

A lower-fidelity `U_op` (§3.5) produces slower, weaker oscillation here — a sloppily inscribed fold is not just riskier but literally slower to resolve, independent of the caster's theoretical grasp of the technique.

**Eq. 4.5 — Resolution Functional** (probability of clean arrival at the moment of release)
```
P_arrive(t_rel) = | <B | Phi(t_rel)> |^2 * exp( -G_dec * t_rel )
```

**Eq. 4.6 — Decoherence Rate**
```
G_dec = eta * ( mismatch(Om2) )^2 / K(B) + s_int
```

| Symbol | Meaning |
|---|---|
| `eta` | Proportionality constant setting how strongly conformal mismatch drives decoherence |
| `mismatch(Om2)` | Mismatch between the caster's assumed and the true conformal factor of B |
| `K(B)` | Caster's knowledge coefficient for B — prior visits, sensory data, measurement quality |
| `s_int` | External disruption injected mid-fold |

Three outcomes are possible depending on when and how the caster releases the fold. A **fizzle** occurs when release comes too early, before `b` has grown appreciably; the state collapses back to A harmlessly — nothing is absorbed and nothing reflects, the quiet failure of §1.3 and Eq. 3.3, reached here by releasing before `b` has grown rather than by low `Fid`; the only cost is the wasted casting. A **bleed**, or echo, occurs when release happens mid-oscillation, with `a` and `b` both significant; neither location fully resolves, and both sites display brief duplicate images of the caster and nearby objects until decoherence forces a resolution on its own. The most severe outcome, a **backlash collapse**, occurs when `G_dec` spikes sharply during the hold — from interference, or from a poorly measured destination — forcing an ungraceful resolution. The unresolved metric mismatch is then absorbed directly into the caster as curvature stress:

**Eq. 4.7 — Backlash Energy**
```
E_back = Int_V[ | g(A) - Om2(x) * g(B) |^2 ] dV
```

The magnitude of this injury scales with how inaccurately the caster understood the destination going in, tying the consequence directly to `K(B)` in Eq. 4.6 rather than to chance. Note that this failure mode is a comprehension failure (an unproven or misjudged `mismatch(Om2)`), distinct from the quiet, non-destructive fizzle that results from a purely low-fidelity casting of an otherwise well-understood fold (§3.5, Eq. 3.3).

This is the general fizzle/backlash distinction of §1.3 in its original, specific form: Eq. 4.6's decoherence rate is what happens to Eq. 1.2's propagating ripple when the destination geometry is mismeasured, and Eq. 4.7's backlash energy is exactly the reflected coupling mismatch §1.3 describes, computed for this one technique before the general mechanism existed to name it. Eq. 4.17 and Eq. 4.21, in the Artisan and Warden technique files respectively, show the same mechanism again in the quark and perturbative-metric channels — this was never a rule unique to the Overlay Fold.

### 4.3 The Bound Singularity

The Bound Singularity generates a genuine, localized region of extreme spacetime curvature — a caster-made gravity well, precise enough at sufficient mastery to cross the threshold into a true event horizon — while actively suppressing its influence on everything outside a chosen boundary. It is built from three separately solved components that must be tuned together: a well source, a counter-curvature containment shell, and a time-dilation boundary that gives the shell a genuine causal edge rather than just a canceled field on paper. This sits at Sovereign tier (§3.3): sourcing real curvature from the aether field, rather than from ordinary mass-energy, requires `Xi(Ae, g)` — the same term that governs every other geometry-level effect in this system. At Sovereign scope the well is held and then released; a well maintained as a standing landmark across generations is the same construction at Legend scale (§4.10, Eq. 4.23).

This technique is the clearest possible illustration of §1.4's propagator self-dependence, because it doesn't merely encounter that self-dependence as an obstacle — it is built by deliberately exploiting it three times over, at three different radii, at once. The well source (Eq. 4.8) sources a `delta(g)` that reshapes the local propagator inside `R_core`; the counter-curvature shell (Eq. 4.9) sources a second `delta(g)`, timed and shaped to exactly cancel the first everywhere outside `R_core`; and the lapse tuning (Eq. 4.10) shapes proper time itself within the shell so that whatever self-reference remains between the two doesn't merely look canceled on paper but is causally sealed against escaping at all. Each of these three castings is, in Eq. 1.4's terms, modifying the very medium the other two are propagating through, in real time — which is exactly why they cannot be solved or inscribed independently and then simply layered together. A caster who has nailed the well and the shell separately, but has never practiced holding both simultaneously, is attempting a live recombination in the sense of §3.6, with everything that implies about the risk of doing so before it has been proven as a unit.

**Eq. 4.8 — Localized Well Source**
```
Curv(g)(r) = Xi(Ae, g) * Bump(r, R_core)
```
`Curv(g)` is the curvature built from the metric `g` (the same role the Einstein tensor plays in ordinary general relativity). `Bump(r, R_core)` is a smooth localization function equal to roughly 1 inside the core radius `R_core` and falling to 0 outside it, which is what keeps the well from sourcing curvature everywhere at once. Because the source is `Xi(Ae, g)` rather than ordinary matter, no real mass is ever required to build the well — consistent with the rest of this system never treating mass as a necessary ingredient of an effect.

**Eq. 4.9 — Counter-Curvature Shell (the anti-gravity field)**
```
Curv(g)(r) = -Xi(Ae, g) * Shell(r, R_core, R_shell)      for R_core <= r <= R_shell
```
`Shell(r, R_core, R_shell)` is nonzero only in the annulus between the core and the outer containment radius `R_shell`, and is engineered to carry curvature-charge equal and opposite to the well's. By an argument analogous to Birkhoff's theorem — a spherically symmetric exterior vacuum depends only on the total enclosed curvature-charge — nulling that total collapses the exterior field to flat space, to leading order. This is the "anti-gravity field": not a force pushing outward, but a matched counter-curvature that leaves nothing for the far field to respond to.

**Eq. 4.10 — Containment Lapse & Horizon Tuning**
```
lapse(r) = sqrt( 1 - 2*k_newton*M_ae(r) / r )      for R_core <= r <= R_shell
lapse(R_shell) -> 0   when   2*k_newton*M_ae(R_shell) = R_shell
```
`M_ae(r)` is the enclosed aether-mass-equivalent within radius `r` (the same role the mass function plays inside a Schwarzschild interior solution). `k_newton` is a fixed background constant — how strongly mass-energy curves spacetime at all, playing the role Newton's constant plays in ordinary gravity — distinct both from `Xi(Ae, g)`, the active technique the caster wields to source that curvature from aether in the first place, and from `k_grav`, the solvable gauge coupling of Eq. 3.1c that Novice techniques like Eq. 4.0b draw on. No caster solves or scales `k_newton`; it is a property of spacetime, not a channel. Tuning `R_shell` and `M_ae(r)` so the horizon condition is satisfied exactly at the shell boundary does more than cancel a number: it makes proper time within the shell approach a full stop as `r -> R_shell` from inside, so nothing inside crosses out in any finite amount of external time. This is what makes the containment causal, not merely a canceled field on paper.

**Eq. 4.11 — Residual Outreach**
```
Curv_ext(r) = (1 - Fid_shell) * Xi(Ae, g)|_{R_core} / r^3      for r > R_shell
```
`Fid_shell` is the fidelity coefficient (§3.5) specifically for the shell term, Eq. 4.9 — tracked separately from the fidelity of the well source or the lapse tuning, since each is inscribed and practiced on its own. With perfect shell fidelity, external curvature is exactly zero: full containment. Imperfect fidelity leaks a residual field, but only as a higher multipole — falling off as `r^-3` rather than the ordinary `r^-2` monopole a real, uncontained mass would produce. A sloppy containment doesn't reveal the well's true strength; it reveals a faint tidal echo of it.

**Eq. 4.12 — Unified Bound Singularity Form**
```
Curv(g)(r) = Xi(Ae,g) * [ Bump(r,R_core) - Shell(r,R_core,R_shell) ]
             + (1 - Fid_shell) * Xi(Ae,g)|_{R_core} * r^-3 * Step(r - R_shell)

subject to:  lapse(r) = sqrt(1 - 2*k_newton*M_ae(r)/r)
             lapse(R_shell) -> 0   when   2*k_newton*M_ae(R_shell) = R_shell
```
This is Eq. 4.8, Eq. 4.9, and Eq. 4.11 folded into a single piecewise definition, using `Bump`, `Shell`, and `Step` as switches that select the active term by radius: near `R_core` it reduces to the raw well; in the annulus out to `R_shell` it reduces to the counter-curvature shell; beyond `R_shell` it reduces to the residual leak. Eq. 4.10 is kept as an explicit constraint rather than merged into the main line, since the lapse function governs the rate of proper time — a different mathematical object from curvature — and folding it in would misrepresent time dilation as just another curvature term rather than the condition that makes the shell causally real.

**Failure modes.** Two distinct disasters are possible, and they are not the same disaster. A **shell rupture** occurs when `Fid_shell` drops below `Fid_min` mid-technique (§3.5): the counter-curvature cancellation fails outright, and the well's full field snaps outward with no warning beyond whatever residual leak (Eq. 4.11) was already showing. **Horizon migration** is subtler: Eq. 4.9's cancellation can hold perfectly — zero measurable external curvature — while Eq. 4.10's horizon condition is still off, meaning the interior was never actually causally sealed. A containment that looks flawless by every instrument available may not be flawless over long enough timescales; a caster who has only mastered the shell and not the lapse tuning has built something that looks safe and isn't. This is a direct consequence of Eq. 1.4: the lapse function depends on the same reshaped geometry the well and shell are simultaneously producing, so a caster who has only validated Eq. 4.9's cancellation in isolation — rather than the full, mutually-reshaping system of all three castings together — has solved a version of the containment that assumed a propagator the actual, combined casting never provides.

Because `R_core`, `R_shell`, and `M_ae` are independent dials within the same technique, a caster who has crossed `prac_min` (§3.6) on all three can adjust them live — shrinking the shell to swallow an incoming threat, then re-expanding and resealing it, without ever fully dropping containment in between. Attempting the same adjustment through pen-and-glyph inscription is far slower, since each change requires re-inscribing the relevant term from scratch.

At Sovereign scope, "horizon migration" and the residual-leak monitoring above are checked once, at casting time, and again at release. Maintaining that same check across a standing well held for a generation — rather than an afternoon — is Legend tier's specific addition; see Eq. 4.23 in `codex/techniques-legend.md`.
