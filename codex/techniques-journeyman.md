# THE AETHER CODEX — Applied Techniques: Journeyman Tier
### §4.5 Journeyman Techniques

*Part of the Aether Codex reference set — see `codex/overview.md` for the file map. All § and Eq. numbers are global across the Codex. Novice worked examples (§4.0) are housed in `codex/techniques-novice.md`; the Spell Directory's Journeyman entries (J-01–J-07, §4.4) are formalized by this section's equation.*

---

### 4.5 Journeyman Techniques

A Novice solves exactly one `k_f` term of Eq. 3.1c in closed form. A Journeyman solves two or more of the same terms — each still closed-form, each still a Novice-tier equation in its own right — without the cross-term `Chi(f1, f2)` (§3.3, §4.6) that would let one sourced ripple satisfy both channels of Eq. 1.3 at once. That absence is not a gap waiting to be filled by effort; it is the tier's defining structural fact. Lacking `Chi`, a Journeyman cannot blend two effects — only alternate between them, completely resolving one before the other begins. Eq. 4.13 formalizes exactly this: the total output of a Journeyman working two techniques is not a sum of simultaneous contributions but a sum of non-overlapping ones.

**Eq. 4.13 — Sequential Invocation Overhead**
```
X_seq(t) = X_1(x,t) * Win_1(t) + X_2(x,t) * Win_2(t)
Win_1(t) . Win_2(t) = 0   for all t
tau_switch = t_start(Win_2) - t_end(Win_1)
```
`X_1` and `X_2` are any two solved Novice-tier expressions from §4.0 or the Spell Directory (§4.4) — Eq. 4.0a through 4.0d or any entry built on them. `Win_1(t)` and `Win_2(t)` are activation-window indicator functions: each is 1 while its technique is actively producing output and 0 otherwise. The product constraint `Win_1(t) . Win_2(t) = 0` is the entire content of "closed form without a cross-term" written as an equation — at no instant is a Journeyman drawing output from both channels at once, because no `Chi(f1,f2)` exists yet to let a single ripple satisfy Eq. 1.3 twice simultaneously. Every entry in the Spell Directory's Journeyman section (J-01 through J-07) is a named illustration of `X_seq(t)`: Ember Handoff (J-01) is Eq. 4.0a's window closing before N-GR-03's opens; Two-Handed Smith (J-05) is Eq. 4.0a and Eq. 4.0c alternating for as long as the hammering lasts.

`tau_switch` is the dead time between windows — the interval a Journeyman spends re-inscribing a glyph or re-settling a cadence (§3.6) between one closed-form casting and the next. It is real cost, not bookkeeping: a caster is producing neither `X_1` nor `X_2` while `tau_switch` elapses, and a task that assumes continuous output (a Storm-Step-style discharge-into-leap, say) simply cannot be performed at Journeyman tier no matter how short `tau_switch` gets, because Eq. 4.13 has no term for simultaneous output at all. Drilled practice — the kind Bladeline Feint (J-07) or Watch-Fire Relay (J-06) exist to train — shrinks `tau_switch` considerably, and a seasoned Journeyman's switch can become nearly imperceptible to an observer. But "nearly imperceptible" is not zero, and it cannot structurally become zero without `Chi(f1,f2)`: the instant `tau_switch -> 0` with the windows still disjoint is not a faster Journeyman, it is the Adept transition itself, since a genuine zero-gap alternation and a true simultaneous blend become indistinguishable only once `Chi` exists to make the blend real rather than merely fast. This is why Adept fidelity enters the Adept Combination Pattern (Eq. 4.15, §4.6; catalogued in §4.4) squared rather than linearly — the two effects are no longer protected from each other's wobble by taking turns.
