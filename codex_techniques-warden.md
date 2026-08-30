# THE AETHER CODEX — Applied Techniques: Warden Tier
### §4.9 Warden Techniques

*Part of the Aether Codex reference set — see `codex/overview.md` for the file map. All § and Eq. numbers are global across the Codex. This is the first metric-sector (`delta(g)`) applied technique below Sovereign (§4.1–§4.3, `codex/techniques-sovereign.md`) and Legend (§4.10, `codex/techniques-legend.md`), and the first place §1.4's propagator self-dependence bites at ordinary-technique scale rather than only in theory.*

---

### 4.9 Warden Techniques

A Warden works the metric channel one order past where a Novice can safely stand. Where Novice technique moves `Ae_local` at an arbitrary point without ever touching `g`, a Warden has solved the leading terms of Eq. 3.1f's perturbation series — `Xi_0` and `Xi_1` — and can therefore nudge spacetime's own curvature by a small, known amount. The catch is built into the word "perturbative": the series was expanded around flat, uncurved spacetime and validated only near that expansion point. Nothing licenses using it anywhere else. A Warden's entire practical range is therefore defined not by how strong `eps` (departure from flat space) they *can* push, but by how far a specific configuration has already been *proven safe*.

**Eq. 4.20 — Perturbative Curvature Whisper**
```
delta(g)_warden = eps * Xi_1 * Bump(r, R_proven)
```
`R_proven` is not a radius chosen for convenience — it is a specific, previously-validated geometry: a familiar room, a mapped stretch of road, a fold-site the Warden (or their teacher) has tested before. `Bump(r, R_proven)` reuses Eq. 4.8's localization shape to confine `eps * Xi_1` to that neighborhood and let it fall to zero outside it. This is why Warden effects read as small and domestic rather than grand: a doorway that briefly weighs less to cross, a step that briefly doesn't quite touch the floor. There is no version of this technique that produces a general-purpose geometry effect — the moment the target leaves `R_proven`, the underlying series has left the region it was ever shown to track.

**Eq. 4.21 — Perturbative Extrapolation Backlash**
```
E_back_pert = Int_V[ | Xi(Ae,g) - (Xi_0 + eps*Xi_1) |^2 ] dV,      for  eps > eps_valid(R_proven)
```
`eps_valid(R_proven)` is the largest departure-from-flat-space that the Warden's specific proven configuration has actually tested — not a theoretical bound, a demonstrated one. Push `eps` past it and the truncated series `Xi_0 + eps*Xi_1` quietly stops tracking the true, closed-form `Xi(Ae,g)` that only a Sovereign has solved (§1.4, §3.3). The gap between what the Warden's math predicts and what the aether field actually does does not vanish; per §1.3's claim that this mechanism is universal across channels, it reflects back as absorbed curvature stress — the identical shape already seen in Eq. 4.7's Overlay Fold mismatch and in the sibling Artisan backlash equation, just written in the metric channel's own terms. A Warden who extends a proven doorway-weight trick to an unmapped stairwell, or widens `eps` past what a tested fold-site has shown, is not attempting a bigger version of the same trick — they are extrapolating an unvalidated curve and eating whatever the true `Xi(Ae,g)` turns out to be at that point.

In practice this makes Warden discipline almost entirely about `R_proven` bookkeeping: knowing exactly which geometries have been tested, to what `eps_valid`, and refusing every request — including one's own — to reuse the result somewhere merely *similar*. It is also why so little Warden technique is ever formally shared: a proof of safety is tied to one specific geometry, not portable to the next.
