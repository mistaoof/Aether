# THE AETHER CODEX — Applied Techniques: Master Tier
### §4.8 Master Techniques

*Part of the Aether Codex reference set — see `codex/overview.md` for the file map. All § and Eq. numbers are global across the Codex. Artisan's partial-diagonalization techniques (§4.7, Eq. 4.16–4.17) are housed in `codex/techniques-artisan.md`; this section is the natural completion of that work once `S` closes over the full eigenbasis.*

---

### 4.8 Master Techniques

Every technique below is downstream of one fact, and one fact only: a Master has closed `S`. Where Eq. 3.1e restricts an Artisan to a finite, proper subset of `M_op`'s eigenvectors — a signature material, and nothing outside it — Master tier is defined in the Power Hierarchy (§3.3) as possession of the *full* eigenbasis. Nothing about the underlying mechanics changes between the two tiers; what changes is that `S` stops being a boundary. A Master has not learned a new kind of magic. A Master has finished solving the one `M_op` every caster has been working inside since Eq. 3.1d.

**Eq. 4.18 — Full Transmutation**
```
M_op_full = Sum_{all i}[ lam_i * |e_i><e_i| ],      S = complete eigenbasis
q_new = U_transmute(M_op_full) * q_old
```
An Artisan's `M_op_partial` (Eq. 3.1e) addresses whatever eigenvectors that Artisan's signature material happens to fall under, and only those — an Artisan of Iron can true a blade because iron's lattice is solved, and cannot touch bronze for the identical reason. `M_op_full` removes that restriction by exhaustion rather than by any new operator: every `lam_i` is known, so `S` is no longer a proper subset of anything, it *is* the eigenbasis. `U_transmute` is the unitary that acts on that completed basis, reassigning which combination of solved eigenvectors a given quantity of matter expresses — it moves `q_old` to `q_new` the way `U_op` (Eq. 4.1) moves a caster between two points, except the "points" here are two material identities rather than two locations. This is the mechanical content of "true transmutation": not a nudge to one property of a known material, but a rewrite of which material the field is, using an operator that Eq. 4.0c's authors never had the eigenbasis to write. Wood becomes stone, lead becomes something nearer gold, decayed tissue becomes sound tissue — not by analogy, but because `q_new` is a different solution of the same operator `q_old` was.

**Eq. 4.19 — Universal Binding & Decay Control**
```
E_bind_eff(x) = E_bind(x) * (1 + s * c_M * Fid),        any x  (S complete)
Gamma_eff(x)   = Gamma_0(x) * (1 + s * c_M * Fid)
s = +1 (boost / hasten)  or  s = -1 (weaken / arrest),  chosen at inscription
```
This is Eq. 4.0c and Eq. 4.0d, generalized in the one direction Novice tier could never take them. Eq. 4.0c boosts `E_bind` for a single material at a single point; Eq. 4.0d nudges `Gamma_0` for whatever trace unstable material happens to be present. Both are narrow because `k_strong` and `k_weak` are single-channel couplings applied to whatever is already at hand. Eq. 4.19 instead runs on `c_M`, the matter-coupling constant Eq. 1.3 folds directly into `M_op`'s own definition — and with `S` complete, `c_M` is no longer confined to a signature subset. The variable `x` ranges over any material a Master's eigenbasis covers, which is to say all of it.

The consequence worth stating plainly: Eq. 4.19 is a single equation, and `E_bind_eff` and `Gamma_eff` are its two faces. Cast with `s = +1` at living tissue's `E_bind(x)`, it is accelerated healing — wounds closing at a pace no Novice cohesion boost could sustain across a whole body rather than one seam. The same equation pointed at `Gamma_eff(x)` is controlled aging or decay — a Master can hasten decomposition (`s = +1`) as precisely as another Master arrests it (`s = -1`), because both are the same term with the direction `s` and `x`'s target chosen differently. The direction parameter is the same operator-level choice a Novice already makes between Eq. 4.0c and Brittle Ease (N-ST-02), or between Eq. 4.0a and Cold Ember (N-EM-02) — never a sign on `Fid` itself, which Eq. 3.2 bounds to `0 <= Fid <= 1`. What Novice tier taught as two unrelated techniques narrow enough to need separate names — Eq. 4.0c's cohesion boost, Eq. 4.0d's decay nudge — Master tier reveals as one equation that was always going to unify once `c_M` stopped being fenced off by an incomplete `S`. Binding-energy control and decay control were never two magics. They were one equation, waiting on a complete eigenbasis to be written down.
