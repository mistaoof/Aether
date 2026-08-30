# THE AETHER CODEX — The Power Hierarchy
### §3.3 The Power Hierarchy · Subclasses · The Ascent Beyond Legend

*Part of the Aether Codex reference set — see `codex/overview.md` for the file map. All § and Eq. numbers are global across the Codex. This file houses §3.3, which sits between §3.2 and §3.4 in `codex/grand-equation.md`.*

---

### 3.3 The Power Hierarchy

Five of the tiers below mark qualitative jumps in comprehension — a new term of the Grand Equation opened up entirely, or, for Legend, an already-opened term pushed to a categorically different scale. Between each of the first three of those pairs sits a named subclass: a rung defined not by a new term but by an *incomplete* version of the next one. The Sovereign→Legend step is the sole exception — per Eq. 3.1g it is the same term at a larger `R_dom`/`t_dom` rather than a new one, so it admits no partial-solution rung between them. These are where most named characters in a story actually live, since full tier transitions are rare, momentous events, while partial progress toward the next one is the ordinary, unglamorous work of the vast majority of a practitioner's career.

| Tier | What's solved | Capabilities | Prevalence |
|---|---|---|---|
| Novice | One `k_f` term, closed form | Single-force effects: fire/lightning (EM), localized strong/weak-force bursts — worked examples in §4.0 | Common |
| Journeyman | Two or more `k_f` terms, each closed form, not yet cross-coupled | Can produce more than one single-force effect, but must switch between them rather than blend | Common |
| Adept | Multiple `k_f` terms, combined | Cross-force effects, combination techniques | Uncommon |
| Artisan | Partial diagonalization of `M_op` (Eq. 3.1e) | Narrow, proven matter-tricks on specific known materials; general transmutation is not yet safe | Uncommon |
| Master | Full eigenbasis of `M_op` | Transmutation, accelerated decay/healing, binding-energy control | Rare; often order leadership |
| Warden | First-order perturbative `Xi(Ae, g)` (Eq. 3.1f) | Narrow, tightly-scoped metric effects, valid only in already-proven special cases | Very rare |
| Sovereign | Closed-form `Xi(Ae, g)` over a bounded domain (Eq. 3.1g, finite `R_dom`) | Localized spacetime warps, minor time dilation, small causality bends, the Overlay Fold, a held Bound Singularity | A handful per era |
| Legend | Closed-form `Xi(Ae, g)` with `R_dom` pushed to effective permanence (Eq. 3.1g) | Regional-scale metric engineering; standing folds; singularities as lasting geographic features | A handful across recorded history |

**The Unsolved Ceiling** — the full `A_op` integral: total, unconditional reality rewriting. Not a tier, and occupied by no one; it is the limit the whole ladder points at without reaching. See §3.4.

Read against §1.3, this table is a map of which coupling channel a tier has opened and how much of it. Novice through Adept live entirely inside `delta(F_f)`, the gauge-sector channel — one coupling constant, then several, then several combined. Artisan and Master live inside `delta(M_op)`, the quark-sector channel, differing only in how much of `S`, the solved eigenvector subset in Eq. 3.1e, has been filled in. Warden through Legend live inside `delta(g)`, the metric-sector channel — the one channel where, per §1.4, solving more of it does not simply mean "a bigger version of the same kind of proof," because the propagator each new increment relies on has already been reshaped by every increment solved before it. This is also why the table's five gauge-and-matter tiers can, in principle, be pursued to full closed-form completion by a sufficiently dedicated caster within an ordinary lifetime, while even the earliest metric-sector tier is marked "very rare": the first two channels are hard because there is a great deal to prove; the third is hard because proving any of it changes the terms of what's left to prove.

Note that tier reflects *comprehension* only. A Novice with excellent execution fidelity (§3.5) can reliably outperform an Adept who casts carelessly — tier sets the ceiling, not the outcome of any single casting. This holds identically for every subclass: a Warden who has drilled their one proven special case under `Sim[...]` (§3.7) until it is flawless will outperform a careless Sovereign, without either of their actual comprehension having changed.

**Journeyman**, **Artisan**, and **Warden** share a common shape worth naming once rather than three times: each is defined by holding a real, non-zero *piece* of the next tier's term rather than none of it. That piece is exactly as usable — and exactly as risky (§2) — as any other partial solution in this system. A Journeyman's two `k_f` terms are each individually as solid as a Novice's one; what's missing is the cross-term connecting them, and attempting to force one anyway is an unproven claim like any other. An Artisan's diagonalized subset of `M_op` is genuinely solved — Eq. 3.1e below formalizes exactly which eigenvectors — but reaching for a material outside that subset is not "harder Artisan work," it's Master-tier work attempted without Master-tier comprehension, and it fails the way §2 says it should. A Warden's perturbative slice of `Xi(Ae, g)` is the same story at the highest ordinary stakes: real, solved, narrow, and unforgiving of extrapolation.

**Eq. 3.1e — Partial Diagonalization** (extends the mass operator in Eq. 3.1d)
```
M_op_partial = Sum_{i in S} lam_i * |e_i><e_i|
```
`S` is the finite, proper subset of `M_op`'s eigenvectors an Artisan has actually solved — as opposed to the complete basis required for Master tier. Effects drawn from an eigenvector inside `S` behave exactly as Eq. 3.1d describes; a material or transformation whose eigenvector isn't in `S` isn't merely weaker, it's unmodeled, and invoking it anyway is a comprehension gamble, not an execution one. This is why Artisans are so often defined by a signature material or effect — steel, bone, salt, rot — rather than a percentage of general competence: `S` tends to grow one hard-won eigenvector at a time, and a career can pass with `S` holding only two or three.

**Eq. 3.1f — Perturbative Aether-Geometry Coupling** (extends `Xi(Ae, g)` from Eq. 3.1b)
```
Xi_pert(Ae, g) = Xi_0 + eps * Xi_1 + O(eps^2)
```
A Warden has solved `Xi_0` and `Xi_1` — the leading terms of a perturbation series around flat, uncurved spacetime — but not the closed form `Xi(Ae, g)` itself that Sovereign tier requires. `O(eps^2)` and beyond are simply unknown. This is why Warden techniques only work "in already-proven special cases": the series was only ever validated near the specific configurations it was expanded around, and pushing `eps` — the size of the departure from flat space — past where it was tested is exactly the kind of extrapolation §2 warns about, with metric-level consequences instead of merely thermal or material ones.

**Eq. 3.1g — Domain Persistence** (governs how far a solved `Xi(Ae, g)` reaches)
```
Xi_valid(x, t):  |x - x0| < R_dom   and   t < t_dom
```
Sovereign and Legend are the same mathematics at different scales of `R_dom` and `t_dom`, not different equations. A Sovereign's closed-form solution is genuinely complete — no perturbative gap, unlike a Warden's — but only within a bounded radius and for a bounded duration: a held fold, a contained singularity, a warp that must eventually be released. A Legend has pushed those same two dials far enough that, for any practical purpose, the effect no longer has a measurable edge: a singularity that has stood for a generation, a causality bend that reshaped a region's history rather than one afternoon of it. Neither `R_dom` nor `t_dom` is ever literally infinite — that would require the term to escape Eq. 3.1's dependence on a caster's finite `dM` entirely, which is precisely what §3.4 forbids. Legend is a very large finite number, not an exception to the rule that finite numbers are all this system permits.

#### The Ascent Beyond Legend

Every path above shares one property: it extends exactly one term of `L_total`, in isolation, and stops the moment that term is fully solved. Legend is where that pattern runs out of room — `Xi(Ae, g)` has no further "more solved" to reach for once its domain is effectively unbounded. What lies beyond isn't a ninth tier. It's a fork: four historically-attested directions, each abandoning the "one term at a time" discipline that got a caster to Legend and reaching instead for something the Grand Equation was never decomposed to make easy. None has ever been completed. None ever can be, per §3.4 — the reasons differ by path, but the impossibility is the same impossibility. That is what makes them paths *toward* divinity rather than routes to it: a character can spend a lifetime, or several, closing the distance, and the distance does not reach zero.

In §1.3's terms, three of the four paths still target a coupling channel — they simply target it whole rather than as a single instance. The Tetrarch Path targets the entire gauge channel at once, seeking one coupling in place of all four `k_f` values. The Demiurge Path targets the entire quark channel at once, seeking the rule that generates `M_op`'s eigenvectors rather than any finite collection of them. The Cosmographer Path targets the entire metric channel pushed past where even Legend stops, and inherits every self-referential difficulty §1.4 attaches to that channel, compounded rather than resolved by how much of it has already been solved. Only the Communion Path steps outside Eq. 1.3 entirely — it does not touch a coupling channel at all, but the boundary `dM` in Eq. 3.1 that determines which channels are reachable in the first place, which is exactly what makes it the odd one out in every account of these four paths that survives from the traditions that attempted them.

- **The Tetrarch Path** (gauge unification) targets a single coupling that would replace all four `k_f` terms in Eq. 3.1c at once:
  ```
  L_gauge -> k_unified * Tr(F_unified . F_unified)      -- no closed form for k_unified is known
  ```
  A caster who gets meaningfully close no longer needs to choose which force an effect expresses through — fire, gravity, and the strong force become facets of one coupling rather than four separate ones. What this path never touches is `L_quark` or `Xi(Ae, g)`: a Tetrarch is close to unstoppable in raw force application and no more able to reshape matter or spacetime than whatever Artisan- or Sovereign-level work they separately hold.

- **The Demiurge Path** (matter-generation) pushes past Master's full diagonalization toward deriving the *generating structure* of `M_op` itself — not a complete list of solved eigenvectors, but the rule that produces them, letting the caster predict and originate stable matter configurations that have never been observed rather than only manipulate known ones:
  ```
  M_op -> Gen(dM)      -- no closed form for Gen is known
  ```
  This is the most overtly "creator-god" path — new substances, new organisms, brought into being directly from the aether — and the most narrowly bounded: it says nothing whatsoever about force, geometry, or causality. A Demiurge who has never touched `Xi(Ae, g)` can be killed by a well-placed fold like anyone else.

- **The Cosmographer Path** (unbounded geometry) is Sovereign/Legend's own trajectory carried past where Legend stopped — `R_dom` and `t_dom` pushed toward true global, permanent scope rather than merely very large:
  ```
  Xi_valid(x, t)  as  R_dom -> infinity, t_dom -> infinity      -- never attained; see Eq. 3.1g
  ```
  A Cosmographer within reach of this limit can reshape terrain, climate, or the causal structure of an entire region as a permanent fact of geography rather than a held effect. The limit itself is §3.4's Unsolved Ceiling wearing a single term's clothing: reaching it in full would mean `Xi(Ae, g)` alone had escaped the finite-`dM` dependence every other term in this system obeys, which the Ceiling's proof forbids for the equation as a whole and, by the same argument, for any one of its pieces pushed to totality.

- **The Communion Path** (comprehension itself) is the only one of the four that does not target a term of `L_total` at all — it targets `dM`, the boundary in Eq. 3.1 that every other path treats as a fixed limit to push against from inside:
  ```
  dM_total = Union(dM_1, dM_2, ..., dM_n)      -- pooling proven comprehension across n minds
  ```
  Rather than one mind solving more mathematics, a Communion merges the *proven* — never the merely believed, per §3.7's warning about `Sim[...]` — comprehension domains of several practitioners into one acting boundary. It is the fastest of the four paths to produce dramatic short-term gains, and the most explicitly horrifying in most traditions that have attempted it, since what's merged is not knowledge alone but the minds that held it. `dM_total` still cannot exceed the union of what its members actually solved; a Communion of a thousand Novices is a very large Novice, not a Legend, and folding a Legend into one changes the ceiling of the merge but not the mathematics of what the Ceiling itself forbids.

No character, order, or god-king in this setting has ever completed one of these four paths, let alone more than one at once — and completing more than one would still fall short, since a true solution to Eq. 3.1 requires `L_gauge`, `L_quark`, `Xi(Ae, g)`, and `dM` all at once, coupled to each other in ways none of these paths even attempts to resolve. This is deliberate room for a story rather than a gap in the mechanics: a Cosmographer and a Demiurge can each be the most powerful individual in their own domain and mutually vulnerable outside it, a self-proclaimed god can be sincerely wrong about having arrived, and the actual endpoint of any path can remain permanently, provably out of frame.
