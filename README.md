# Aether

<title>The Aether Codex</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,450;9..144,600;9..144,700&family=Spectral:ital,wght@0,400;0,500;0,600;1,400&family=IBM+Plex+Mono:wght@400;500&display=swap">
<style>
:root{
  --ground:#F4F6F7; --panel:#FBFCFC; --ink:#1B2530; --ink-soft:#4A5A66;
  --hairline:#C9D3D8; --accent:#0F7A85; --accent-ink:#0B5C64;
  --eq-wash:#E7EFF1; --eq-border:#B9CDD1; --mark:#8A6D1F;
  --nav-active:#DDE9EB;
}
:root:not([data-theme="light"]){}
@media (prefers-color-scheme: dark){
  :root:not([data-theme="light"]){
    --ground:#0F151B; --panel:#151D24; --ink:#D6DFE6; --ink-soft:#93A4B0;
    --hairline:#2B3742; --accent:#57C4CC; --accent-ink:#7BD3D9;
    --eq-wash:#131E23; --eq-border:#2C4348; --mark:#D8B45A;
    --nav-active:#1C2A33;
  }
}
:root[data-theme="dark"]{
  --ground:#0F151B; --panel:#151D24; --ink:#D6DFE6; --ink-soft:#93A4B0;
  --hairline:#2B3742; --accent:#57C4CC; --accent-ink:#7BD3D9;
  --eq-wash:#131E23; --eq-border:#2C4348; --mark:#D8B45A;
  --nav-active:#1C2A33;
}
*{box-sizing:border-box}
body{
  margin:0; background:var(--ground); color:var(--ink);
  font-family:"Spectral", Georgia, serif; font-size:16.5px; line-height:1.72;
}
.wrap{display:flex; min-height:100vh}
nav.rail{
  width:272px; flex:none; position:sticky; top:0; align-self:flex-start;
  height:100vh; overflow-y:auto; padding:28px 14px 40px 20px;
  border-right:1px solid var(--hairline); background:var(--panel);
}
.rail-title{
  font-family:"Fraunces", Georgia, serif; font-weight:700; font-size:21px;
  letter-spacing:.01em; margin:0 0 2px; color:var(--ink);
}
.rail-sub{
  font-family:"IBM Plex Mono", monospace; font-size:11px; color:var(--ink-soft);
  text-transform:uppercase; letter-spacing:.14em; margin:0 0 22px;
}
nav.rail a{
  display:flex; justify-content:space-between; align-items:baseline; gap:10px;
  padding:7px 10px; margin:1px 0; border-radius:6px; text-decoration:none;
  color:var(--ink-soft); font-size:14px; line-height:1.35;
}
nav.rail a .nav-tag{font-family:"IBM Plex Mono", monospace; font-size:10.5px; color:var(--ink-soft); opacity:.75; white-space:nowrap}
nav.rail a:hover{background:var(--nav-active); color:var(--ink)}
nav.rail a.active{background:var(--nav-active); color:var(--accent-ink)}
nav.rail a.active .nav-label{font-weight:600}
nav.rail a:focus-visible{outline:2px solid var(--accent); outline-offset:1px}
main{flex:1; min-width:0; padding:0 clamp(20px, 5vw, 72px) 96px}
.masthead{
  padding:64px 0 30px; border-bottom:1px solid var(--hairline); margin-bottom:8px;
}
.masthead .eyebrow{
  font-family:"IBM Plex Mono", monospace; font-size:12px; letter-spacing:.18em;
  text-transform:uppercase; color:var(--accent-ink); margin:0 0 10px;
}
.masthead h1{
  font-family:"Fraunces", Georgia, serif; font-weight:700; font-size:clamp(34px, 5vw, 52px);
  margin:0 0 12px; text-wrap:balance; letter-spacing:-.01em;
}
.masthead p{max-width:66ch; color:var(--ink-soft); margin:0; font-size:17px}
section.book{padding:52px 0 8px; border-bottom:1px solid var(--hairline)}
section.book:last-of-type{border-bottom:none}
.book-head{margin:0 0 18px}
.book-tag{
  font-family:"IBM Plex Mono", monospace; font-size:11.5px; letter-spacing:.14em;
  text-transform:uppercase; color:var(--accent-ink);
}
.book-head h1{
  font-family:"Fraunces", Georgia, serif; font-weight:600; font-size:31px;
  margin:4px 0 0; text-wrap:balance;
}
.book-body{max-width:70ch}
.book-body h2{font-family:"Fraunces", Georgia, serif; font-weight:600; font-size:24px; margin:2.2em 0 .6em; text-wrap:balance}
.book-body h3{font-family:"Fraunces", Georgia, serif; font-weight:600; font-size:20px; margin:2em 0 .5em; text-wrap:balance}
.book-body h4{font-family:"Fraunces", Georgia, serif; font-weight:600; font-size:17px; margin:1.8em 0 .4em; color:var(--accent-ink)}
.book-body p{margin:.9em 0}
.book-body em{color:inherit}
.book-body hr{border:none; border-top:1px solid var(--hairline); margin:2.2em 0}
.book-body a{color:var(--accent-ink)}
.book-body code{
  font-family:"IBM Plex Mono", monospace; font-size:.86em;
  background:var(--eq-wash); border:1px solid var(--eq-border);
  border-radius:4px; padding:.06em .32em; white-space:nowrap;
}
.book-body pre{
  background:var(--eq-wash); border:1px solid var(--eq-border);
  border-left:3px solid var(--accent); border-radius:6px;
  padding:14px 18px; overflow-x:auto; margin:1.1em 0;
}
.book-body pre code{background:none; border:none; padding:0; white-space:pre; font-size:13.5px; line-height:1.6}
.book-body blockquote{
  margin:1.4em 0; padding:.2em 1.2em; border-left:3px solid var(--mark);
  color:var(--ink-soft); font-style:italic;
}
.table-scroll, .book-body .tablewrap{overflow-x:auto}
.book-body table{
  border-collapse:collapse; margin:1.2em 0; font-size:14.5px; line-height:1.5;
  min-width:100%;
}
.book-body th{
  text-align:left; font-family:"IBM Plex Mono", monospace; font-size:11.5px;
  text-transform:uppercase; letter-spacing:.09em; color:var(--ink-soft);
  border-bottom:2px solid var(--hairline); padding:8px 14px 8px 0;
}
.book-body td{border-bottom:1px solid var(--hairline); padding:8px 14px 8px 0; vertical-align:top}
.book-body td code, .book-body th code{white-space:nowrap}
.book-body ul, .book-body ol{padding-left:1.4em; margin:.9em 0}
.book-body li{margin:.45em 0}
.book-body li p{margin:.4em 0}
.footer-note{
  margin-top:56px; padding-top:20px; border-top:1px solid var(--hairline);
  font-family:"IBM Plex Mono", monospace; font-size:12px; color:var(--ink-soft);
}
.menu-btn{display:none}
@media (max-width: 900px){
  nav.rail{
    position:fixed; z-index:20; left:0; top:0; transform:translateX(-100%);
    transition:transform .2s ease; width:280px; box-shadow:0 0 40px rgba(0,0,0,.25);
  }
  nav.rail.open{transform:none}
  .menu-btn{
    display:block; position:fixed; z-index:21; top:14px; left:14px;
    background:var(--panel); color:var(--ink); border:1px solid var(--hairline);
    border-radius:8px; padding:8px 14px; font-family:"IBM Plex Mono", monospace;
    font-size:12px; letter-spacing:.08em; cursor:pointer;
  }
  .masthead{padding-top:76px}
}
@media (prefers-reduced-motion: reduce){
  nav.rail{transition:none}
  html{scroll-behavior:auto}
}
html{scroll-behavior:smooth}
</style>
<button class="menu-btn" id="menuBtn" aria-label="Open contents">Contents</button>
<div class="wrap">
<nav class="rail" id="rail" aria-label="Codex contents">
<p class="rail-title">The Aether Codex</p>
<p class="rail-sub">v2.4 · Reference Set</p>
<a href="#overview" data-target="overview"><span class="nav-label">Overview &amp; File Map</span><span class="nav-tag">Index</span></a>
<a href="#foundations" data-target="foundations"><span class="nav-label">Foundations</span><span class="nav-tag">§1–§2</span></a>
<a href="#grand-equation" data-target="grand-equation"><span class="nav-label">The Grand Equation</span><span class="nav-tag">§3.1–3.7</span></a>
<a href="#power-hierarchy" data-target="power-hierarchy"><span class="nav-label">The Power Hierarchy</span><span class="nav-tag">§3.3</span></a>
<a href="#techniques-novice" data-target="techniques-novice"><span class="nav-label">Novice Techniques</span><span class="nav-tag">§4.0</span></a>
<a href="#techniques-journeyman" data-target="techniques-journeyman"><span class="nav-label">Journeyman Techniques</span><span class="nav-tag">§4.5</span></a>
<a href="#techniques-adept" data-target="techniques-adept"><span class="nav-label">Adept Techniques</span><span class="nav-tag">§4.6</span></a>
<a href="#techniques-artisan" data-target="techniques-artisan"><span class="nav-label">Artisan Techniques</span><span class="nav-tag">§4.7</span></a>
<a href="#techniques-master" data-target="techniques-master"><span class="nav-label">Master Techniques</span><span class="nav-tag">§4.8</span></a>
<a href="#techniques-warden" data-target="techniques-warden"><span class="nav-label">Warden Techniques</span><span class="nav-tag">§4.9</span></a>
<a href="#techniques-sovereign" data-target="techniques-sovereign"><span class="nav-label">Sovereign Techniques</span><span class="nav-tag">§4.1–4.3</span></a>
<a href="#techniques-legend" data-target="techniques-legend"><span class="nav-label">Legend Techniques</span><span class="nav-tag">§4.10</span></a>
<a href="#techniques-ascension" data-target="techniques-ascension"><span class="nav-label">The Ascent Beyond Legend</span><span class="nav-tag">§4.11</span></a>
<a href="#spell-directory" data-target="spell-directory"><span class="nav-label">The Spell Directory</span><span class="nav-tag">§4.4</span></a>
<a href="#glossary" data-target="glossary"><span class="nav-label">Glossary &amp; Equation Index</span><span class="nav-tag">§5–§6</span></a>
<a href="#changelog" data-target="changelog"><span class="nav-label">Changelog</span><span class="nav-tag">§7</span></a>
</nav>
<main>
<div class="masthead">
<p class="eyebrow">Aether Power System · Complete Reference</p>
<h1>The Aether Codex</h1>
<p>All sixteen books of the Codex in one place — foundations, the Grand Unified Aether Equation, the Power Hierarchy, applied techniques from Novice through the Ascent Beyond Legend, the Spell Directory, and the full glossary. All § and Eq. numbers are global across the set.</p>
</div>
<section class="book" id="overview"><header class="book-head"><span class="book-tag">Index</span><h1>Overview &amp; File Map</h1></header><div class="book-body"><p><strong>Version:</strong> 2.4
<strong>Status:</strong> Living document — see <code>codex/changelog.md</code> for how to extend it
<strong>Notation:</strong> All equations use plain ASCII (no Greek letters, hats, daggers, or special symbols) so they can be typed directly into a manuscript. See the changelog (v1.3 entry) for the legacy symbol mapping if cross-referencing earlier drafts.</p>
<hr>
<h2>How this reference is organized</h2>
<p>The Codex was originally a single document; as of v2.2 it is split into files under <code>codex/</code> so each area can be edited and extended independently. <strong>All section (§) and equation (Eq.) numbers are global and unchanged from the single-document versions</strong> — a cross-reference like "§3.5" or "Eq. 4.7" means the same thing everywhere, regardless of which file it appears in. Use the map below to find which file houses any given section.</p>
<div class="table-scroll"><table>
<thead>
<tr>
<th>File</th>
<th>Contents</th>
<th>Sections</th>
<th>Equations defined</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>codex/overview.md</code></td>
<td>This file — version, notation, file map, reading order</td>
<td>—</td>
<td>—</td>
</tr>
<tr>
<td><code>codex/foundations.md</code></td>
<td>Premise (the layered-field mechanism) and Core Philosophy</td>
<td>§1 (1.1–1.4), §2</td>
<td>Eq. 1.1–1.4</td>
</tr>
<tr>
<td><code>codex/grand-equation.md</code></td>
<td>The Grand Unified Aether Equation, term reference, the Unsolved Ceiling, Fidelity, Unassisted Invocation, Simulated Invocation</td>
<td>§3.1, §3.2, §3.4–§3.7</td>
<td>Eq. 3.1–3.1d, 3.2–3.5</td>
</tr>
<tr>
<td><code>codex/power-hierarchy.md</code></td>
<td>The Power Hierarchy, subclasses, and the Ascent Beyond Legend</td>
<td>§3.3</td>
<td>Eq. 3.1e–3.1g</td>
</tr>
<tr>
<td><code>codex/techniques-novice.md</code></td>
<td>Part 4 preamble (the ripple-to-result chain) and Novice worked examples</td>
<td>§4 intro, §4.0</td>
<td>Eq. 4.0a–4.0c, 4.0e</td>
</tr>
<tr>
<td><code>codex/techniques-journeyman.md</code></td>
<td>Journeyman techniques — formalizing sequential, un-cross-coupled casting</td>
<td>§4.5</td>
<td>Eq. 4.13</td>
</tr>
<tr>
<td><code>codex/techniques-adept.md</code></td>
<td>Adept techniques — formal definition of the <code>Chi(f1,f2)</code> cross-coupling function</td>
<td>§4.6</td>
<td>Eq. 4.14–4.15</td>
</tr>
<tr>
<td><code>codex/techniques-artisan.md</code></td>
<td>Artisan techniques — the quark-sector analogue of a Novice worked example, and its backlash mode</td>
<td>§4.7</td>
<td>Eq. 4.16–4.17</td>
</tr>
<tr>
<td><code>codex/techniques-master.md</code></td>
<td>Master techniques — full transmutation and universal binding/decay control</td>
<td>§4.8</td>
<td>Eq. 4.18–4.19</td>
</tr>
<tr>
<td><code>codex/techniques-warden.md</code></td>
<td>Warden techniques — the first metric-sector effect below Sovereign</td>
<td>§4.9</td>
<td>Eq. 4.20–4.21</td>
</tr>
<tr>
<td><code>codex/techniques-sovereign.md</code></td>
<td>The Overlay Fold, the Collapse Condition, the Bound Singularity (Sovereign scope)</td>
<td>§4.1–§4.3</td>
<td>Eq. 4.1–4.12</td>
</tr>
<tr>
<td><code>codex/techniques-legend.md</code></td>
<td>Legend-scale extensions of the Overlay Fold and Bound Singularity — the same mathematics, held across a standing domain</td>
<td>§4.10</td>
<td>Eq. 4.22–4.23</td>
</tr>
<tr>
<td><code>codex/techniques-ascension.md</code></td>
<td>The Ascent Beyond Legend — closeness/progress equations for the four unattainable paths</td>
<td>§4.11</td>
<td>Eq. 4.24–4.27</td>
</tr>
<tr>
<td><code>codex/spell-directory.md</code></td>
<td>The Spell Directory — coded catalog of named techniques, Novice through Beyond Legend (every rank except Sovereign, whose canonical workings live in §4.1–§4.3)</td>
<td>§4.4</td>
<td>Eq. 4.0d</td>
</tr>
<tr>
<td><code>codex/glossary.md</code></td>
<td>Symbol &amp; Term Glossary and the Equation Index</td>
<td>§5, §6</td>
<td>—</td>
</tr>
<tr>
<td><code>codex/changelog.md</code></td>
<td>Version history and extension conventions</td>
<td>§7</td>
<td>—</td>
</tr>
</tbody>
</table></div>
<h2>Reading order</h2>
<p>For a first read, or for onboarding a collaborator: <code>foundations.md</code> (why the system works the way it does), then <code>grand-equation.md</code> (the formal core and the three axes), then <code>power-hierarchy.md</code> (who can do what), then the technique files in tier order — <code>techniques-novice.md</code>, <code>techniques-journeyman.md</code>, <code>techniques-adept.md</code>, <code>techniques-artisan.md</code>, <code>techniques-master.md</code>, <code>techniques-warden.md</code>, <code>techniques-sovereign.md</code>, <code>techniques-legend.md</code>, <code>techniques-ascension.md</code> — with <code>spell-directory.md</code> and <code>glossary.md</code> as references to consult rather than read straight through.</p>
<h2>Extension conventions</h2>
<p>New techniques, refinements, and derivations are appended to the relevant file with a version bump and a one-line summary in <code>codex/changelog.md</code>. New equations continue the running global numbering tracked in <code>codex/glossary.md</code> (§6). As of v2.3, every rank in the Power Hierarchy — Novice through Legend — has at least one dedicated applied-technique file and at least one formalized equation, and the four Ascent Beyond Legend paths each have a closeness/progress equation in <code>codex/techniques-ascension.md</code>. Future growth from here is depth (more Spell Directory entries per rank, deeper derivations) rather than filling gaps in the hierarchy's coverage.</p></div></section>
<section class="book" id="foundations"><header class="book-head"><span class="book-tag">§1–§2</span><h1>Foundations</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex.</em></p>
<hr>
<h2>1. Premise</h2>
<p>Aether is a field in its own right, not a name for what the four fundamental forces are made of. It occupies a layer beneath electromagnetism, the weak interaction, the strong interaction, and gravity: coupled to all four, sourced by none of them, and — critically — not observable except through that coupling. Nothing about the aether field itself glows, burns, pulls, or bends light. What a witness actually sees when an aether-user works is never the aether field directly; it is electromagnetism, the strong force, gravity, or the metric itself, momentarily wearing a shape those fields would not have taken on their own. A person able to perceive and address the aether field directly is not casting a spell in the traditional sense. They are disturbing a field that sits underneath the ones matter and radiation actually experience, and using that disturbance's own onward spread — a ripple — to push the upper fields into a configuration of the caster's choosing.</p>
<p>This document used to describe aether more loosely, as "the field the four forces are woven from" — convenient language for a first pass, but not one this document's own equations ever actually required, and not one that survives close reading of §3.1, where aether enters the total Lagrangian through a single explicit term, <code>Xi(Ae, g)</code>, rather than appearing inside the gauge or quark terms at all. §1.1 through §1.4 replace that loose description with the mechanism the rest of this document has been assuming all along, expressed as four new equations that sit ahead of the Grand Aether Equation itself rather than inside it — a foundation underneath the foundation. Nothing about this changes any equation in §3 or §4: every <code>k_f</code>, every eigenvector of <code>M_op</code>, every fidelity coefficient, every failure mode described later in this document is exactly as this section leaves it. What changes is that those pieces stop being separately asserted rules and start being visible consequences of one underlying picture.</p>
<p>The system is built around two independent constraints, developed across this document. What an aether-user can <em>theoretically</em> achieve is bounded by what they have mathematically solved (§2, §3.4) — in the vocabulary this section introduces, by which coupling channels between the aether layer and the upper fields have a proven functional form. What they <em>actually</em> achieve in a given moment is bounded by how faithfully they execute that solved mathematics (§3.5, §3.6) — by how clean and coherent the ripple they source actually is. Neither stamina, birthright, nor a supply of any consumable resource enters into it at any point, for a reason §1.1 makes literal rather than merely asserted: there is nothing to consume.</p>
<h3>1.1 The Layered-Field Picture</h3>
<p>Picture two surfaces of water, one directly above the other, connected only by narrow, invisible channels rather than by direct contact. The upper surface is the one anyone can see: it is the four fundamental fields, doing what fields do, indifferent to whatever lies beneath them. The lower surface is aether. Nothing about the lower surface is visible from above unless something disturbs it — but a disturbance at the lower surface, if it is shaped correctly and finds one of those channels, arrives at the upper surface as a ripple: a real, physical distortion of the field that channel connects to. A caster works entirely at the lower surface. Every visible effect — heat, light, lift, curvature — is what the upper surface does once a ripple reaches it, not something the caster reaches up and does directly.</p>
<p>This is worth stating formally, because a great deal of what the rest of this document treats as separate rules is a direct consequence of this one decomposition:</p>
<p><strong>Eq. 1.1 — Aether Field Decomposition</strong></p>
<pre><code>Ae(x, t) = Ae_0 + dAe(x, t)
</code></pre>
<p><code>Ae_0</code> is the ambient value of the aether field discussed at length in §3.5: uniform, inexhaustible, present at every point in spacetime whether or not anyone is casting, and — this is the important part for this section — on its own, entirely inert. An untouched <code>Ae_0</code> produces no heat, no lift, no curvature; it is a background, not a source. <code>dAe(x, t)</code> is the local perturbation superimposed on that background at the moment and location of a casting: the ripple itself, and the only part of the aether field that ever actually does anything. Casting, in the vocabulary this section introduces, is nothing more or less than sourcing a <code>dAe</code> with a particular shape. Everything a caster spends years learning to do — comprehension, fidelity, tier, technique — is entirely about what shape of <code>dAe</code> they are capable of sourcing, and how reliably.</p>
<p>This decomposition is also what makes the non-consumable nature of aether (§3.5) a structural fact rather than a setting rule someone could quietly retcon. <code>Ae_0</code> isn't drawn down by a casting any more than the floor of a pond is drawn down by a ripple crossing its surface. A caster contributes <code>dAe</code>; they never touch <code>Ae_0</code> at all, which is precisely why two casters working nearby don't compete for a shared supply, why exhaustion has no aether-scarcity component anywhere in this system, and why an aether-poor or aether-rich location is not a coherent idea within this framework — <code>Ae_0</code> does not vary by geography any more than a vacuum field does in ordinary physics. What can vary by location is how easily a caster's <code>dAe</code> reaches a channel worth using, which §1.2 makes precise.</p>
<h3>1.2 The Ripple: Sourcing and Propagation</h3>
<p>A perturbation sourced at one point in the aether field does not simply appear at the location a caster wants it to affect. It has to get there, and how it gets there is itself a real, calculable process — not an instantaneous, willed transaction between caster and effect. This is the propagation half of the mechanism, and it is where the caster's actual invocation — glyph, cadence, gesture, or a purely mental structure at sufficient mastery (§3.6) — enters the picture as a physical quantity rather than a narrative flourish.</p>
<p><strong>Eq. 1.2 — Ripple Sourcing and Propagation</strong></p>
<pre><code>dAe(x, t) = Int[ G(x, x'; t, t'; g) * J_cast(x', t') ] d4x'
</code></pre>
<p><code>J_cast(x', t')</code> is the source current the caster's invocation injects into the aether field at the point and moment of casting — formally, this is <code>phi_actual</code> from Eq. 3.2, restated here in its role as a physical source rather than as an abstract "structure being reproduced." Every property Eq. 3.2 already assigns to <code>phi_actual</code> — that it can be more or less faithful to an ideal target, that its quality depends on precision of inscription and steadiness of execution, that it is trainable independently of theory — is a property of a real, physical current under this equation, not a metaphor sitting on top of one. <code>G(x, x'; t, t'; g)</code> is the propagator: it answers the question of how strongly, and after how much delay, a disturbance sourced at <code>(x', t')</code> is felt at <code>(x, t)</code>, given the surrounding geometry <code>g</code>. This is the "channel" from §1.1's picture, made mathematically explicit — and, as §1.4 develops at length, the fact that <code>G</code> itself depends on <code>g</code> rather than treating it as a fixed backdrop is the single most consequential detail in this entire document.</p>
<p>Two things follow immediately from writing the ripple this way, and both were already true throughout §3 and §4 without ever being derived from anything — they were simply true by assertion. Here they are true by construction. First, a ripple sourced with a weak or poorly-shaped <code>J_cast</code> produces a correspondingly weak or poorly-shaped <code>dAe</code>, regardless of how well the caster understands the underlying mathematics — this is fidelity (§3.5), and Eq. 1.2 is the equation Eq. 3.2's <code>Fid</code> coefficient was always secretly describing the front end of. Second, <code>dAe</code> is computed by integrating over every point the propagator connects to the casting location, not just the casting location itself — which is why the difficulty of a technique like the Overlay Fold (§4.1) scales with the conformal mismatch between origin and destination rather than being a flat cost: a larger mismatch means <code>G</code> has to carry the disturbance across a less hospitable stretch of geometry, and a poorly propagated ripple arrives distorted no matter how cleanly it was sourced.</p>
<p>None of this changes what a caster experiences. No one perceives an integral; they perceive heat, or lift, or a held fold. But every equation in §3 and §4 that scales an effect by <code>Fid</code>, or that ties a failure to interference or a mismeasured destination, is describing what Eq. 1.2 predicts a ripple does under those exact conditions.</p>
<h3>1.3 Surface Coupling: From Ripple to Effect</h3>
<p>A ripple that has propagated to the right place still has to do something once it gets there — it has to distort one of the upper fields, and it can only do that along a channel whose shape is actually known. This is the coupling half of the mechanism, and it is where comprehension (§2, §3.4) stops being an abstract "how much math have you solved" and becomes a concrete statement about which of the following three channels a given caster has a proven functional form for.</p>
<p><strong>Eq. 1.3 — Surface Coupling</strong></p>
<pre><code>delta(F_f)  = k_f  * dAe(x, t)                         -- gauge-sector distortion
delta(M_op) = c_M  * dAe(x, t)                         -- quark-sector distortion
delta(g)    = Xi(Ae, g),   with Ae = Ae_0 + dAe        -- metric-sector distortion
</code></pre>
<p>Each line names a different upper-layer field being pushed by the same ripple, through a different channel, at a coupling strength that is either known or it isn't. <code>delta(F_f)</code> is the channel every Novice technique in §4.0 uses: a ripple reaching the gauge sector, distorting the field-strength tensor for one fundamental force by an amount set by that force's coupling constant <code>k_f</code> — already defined in Eq. 3.1c, unchanged here, now with an explicit account of what actually delivers the disturbance to it. <code>delta(M_op)</code> is the channel Artisan and Master techniques use: a ripple reaching the quark sector, distorting the mass operator that governs matter's structure, at a strength set by <code>c_M</code> — a matter-coupling analogue of <code>k_f</code>, folded for convenience into <code>M_op</code>'s own definition (Eq. 3.1d) rather than tracked as a separate constant, since it is never invoked except as part of that operator. <code>delta(g)</code> is the channel Warden through Legend use, and it is not like the other two in ways §1.4 exists specifically to explain.</p>
<p>This is the concrete meaning of "comprehension caps power" (§2): a caster can only reliably use a coupling channel whose strength — <code>k_f</code> for a specific force, a specific eigenvector's contribution to <code>c_M</code>, a specific order of <code>Xi(Ae, g)</code>'s expansion — has actually been solved. Sourcing a <code>dAe</code> is possible for anyone who can invoke at all; it is the same physical act regardless of what the caster believes about where it's going. What differs is whether the caster knows, correctly, what that ripple will do once it arrives. A term of <code>L_total</code> that hasn't been solved isn't a channel that produces a weaker effect — it's a channel whose strength and shape the caster is guessing at, and Eq. 1.3 doesn't care whether a guess is confident.</p>
<p>This is also, now, the exact mechanism separating a fizzle from a backlash — two failure modes that §3.5 and §4.2 each described independently, without either explanation drawing on the other. Both descriptions were correct. Neither was complete.</p>
<ul>
<li><strong>A fizzle is a coupling problem on the sourcing side.</strong> The channel's strength is correctly known — comprehension is sound — but <code>J_cast</code> in Eq. 1.2 was weak or incoherent, so the <code>dAe</code> that actually arrives at the coupling point is too small or too poorly shaped to produce a <code>delta(X)</code> above the resolution threshold (Eq. 3.3). The ripple doesn't misfire; it simply doesn't arrive with enough coherent amplitude to register, and what little of it there is dissipates back into the ambient <code>Ae_0</code> background without incident. Nothing reflects. Nothing is absorbed. This is why a fizzle is safe: there was never enough there to go wrong.</li>
<li><strong>A backlash is a coupling problem on the receiving side.</strong> <code>J_cast</code> was well-formed — fidelity was fine, possibly excellent — but the coupling constant or eigenvector the caster used to shape their intended effect was wrong: unproven, misjudged, or extrapolated past where it was actually solved. The ripple arrives coherent and on schedule, but Eq. 1.3's coupling channel has no correct functional form to resolve it against, because the caster's model of that channel doesn't match the one the field actually has. The mismatch between what was sourced and what the channel can actually accept doesn't vanish — it has nowhere to dissipate to, because dissipation into <code>Ae_0</code> was only ever available to a ripple that arrived too weak to resolve in the first place, and this one didn't. It reflects back along the same channel that carried it out, arriving at the caster as absorbed stress. This is precisely what Eq. 4.7 already computes for the Overlay Fold's specific case — an unresolved metric mismatch, absorbed as curvature stress — and it was never a rule invented specifically for that one technique. It is what this mechanism predicts happens to <em>any</em> mismatched coupling, with the Overlay Fold simply being the first place this document worked out the arithmetic.</li>
</ul>
<p>This is also why Simulated Invocation (§3.7) draws exactly the line it draws, and no other. <code>Sim[...]</code> measures the coherence of <code>J_cast</code> against a caster's <em>believed</em> target structure — it is, precisely, a readout of how well Eq. 1.2's sourcing side would perform, run without ever letting the result reach Eq. 1.3's coupling side at all. That is why it can certify fidelity perfectly and comprehension not at all: a flawlessly sourced ripple aimed at a channel whose strength was never actually solved will simulate beautifully, because simulation was never checking whether the channel's assumed strength was correct. It was only ever checking whether the caster could reliably produce the ripple they intended to produce. Whether that ripple was aimed at a real, provable channel is a question <code>Sim[...]</code> structurally cannot ask.</p>
<h3>1.4 Why the Metric Is Different</h3>
<p>Two of Eq. 1.3's three channels — <code>delta(F_f)</code> and <code>delta(M_op)</code> — behave exactly the way a first read of "comprehension caps power" would suggest: solve the coupling once, and it stays solved, permanently, for every future casting that uses it, because nothing about using it changes the conditions under which it was solved. The third channel does not behave this way, and the reason is not a difference in how hard the mathematics is. It is a difference in what kind of mathematics it is.</p>
<p><strong>Eq. 1.4 — Propagator Self-Dependence</strong></p>
<pre><code>G(x, x'; t, t'; g)   depends explicitly on g

delta(g) = Xi(Ae, g)   whenever the metric channel is engaged

=&gt;  G(x, x'; t, t'; g + delta(g))  !=  G(x, x'; t, t'; g)
</code></pre>
<p>The propagator in Eq. 1.2 — the function governing how any ripple travels from where it's sourced to where it's meant to arrive — takes the surrounding geometry <code>g</code> as one of its inputs, because how a disturbance spreads through space depends on the shape of that space. This is true whether or not any casting is underway; it is simply a fact about how propagation works. It becomes a problem the moment a caster actually engages the metric channel, because <code>delta(g)</code> in Eq. 1.3 is itself a change to <code>g</code> — and <code>g</code> is the very quantity <code>G</code> depends on. A caster invoking <code>Xi(Ae, g)</code> is not sending a ripple through a fixed, indifferent medium the way a Novice heating water is. They are sending a ripple through a medium that their own ripple, once it arrives, will have already begun to reshape — and the reshaped medium is what determines how the rest of that same ripple propagates, mid-cast, including the parts of it still in transit when the reshaping starts.</p>
<p>Nothing else in this system has this property. Solving <code>k_EM</code> doesn't change how the gauge sector propagates disturbances; solving an eigenvector of <code>M_op</code> doesn't change how the quark sector does either. Those channels are static targets — hard to hit precisely, in the sense that comprehension and fidelity are both genuinely required, but the target itself doesn't move while you're aiming at it. <code>Xi(Ae, g)</code> is a channel that edits the range at which it's being fired from, in real time, using the same shot that's currently in flight. This is not a difference of degree from the other two channels. It is a difference in kind, and it is the entire reason the Power Hierarchy (§3.3) treats geometry-level comprehension as categorically harder to reach than full command of all four fundamental forces and the complete mass operator combined, rather than merely one further rung on the same ladder.</p>
<p>It is also, precisely, why <code>Xi(Ae, g)</code> cannot be solved once, in closed form, for arbitrary configurations, and why every technique in this document that reaches it does so through one of exactly two strategies rather than through the straightforward "prove the constant, then use it anywhere" approach that works for <code>k_f</code> and <code>M_op</code>. A Warden's perturbative expansion (Eq. 3.1f) sidesteps the self-dependence by staying close enough to flat, unperturbed space that <code>G[g + delta(g)]</code> and <code>G[g]</code> are approximately the same propagator to whatever order in <code>eps</code> has actually been solved — which is exactly why a Warden's techniques stop working the moment they're pushed past the configuration the expansion was validated around: past that point, the approximation that let them ignore the self-dependence in the first place quietly stops holding, and the caster is extrapolating a channel whose true shape they were never actually solving. A Sovereign or Legend's closed-form solution (Eq. 3.1g) doesn't sidestep the self-dependence at all — it solves the fully backreacting system honestly, but only within a bounded domain, <code>R_dom</code> and <code>t_dom</code> small enough, or well-enough studied in advance, that the coupled evolution of <code>dAe</code> and <code>g</code> together has actually been worked out for that specific configuration rather than assumed to generalize. Neither strategy produces a channel with the unconditional, anywhere-anytime validity that a solved <code>k_f</code> term has, and Eq. 1.4 is the reason neither one ever could.</p>
<p>This same self-dependence is also what makes the Unsolved Ceiling (§3.4) bite hardest, specifically, against any of the four Ascent paths that reach for <code>Xi(Ae, g)</code> pushed toward its limit. The Cosmographer Path's unbounded <code>R_dom, t_dom -&gt; infinity</code> isn't merely "a very large Sovereign domain" — every increment of domain a Cosmographer tries to add requires re-solving the coupled <code>dAe</code>–<code>g</code> system for a configuration that includes everything solved so far plus more, because Eq. 1.4 means the medium the next increment propagates through has already been changed by every increment before it. There is no version of this problem that becomes easier by having solved more of it already; each solved region makes the geometry the next attempt has to account for strictly more complicated, not less. This is the mechanism behind the Ceiling's proof (§3.4) wearing the Cosmographer Path's clothing specifically, rather than a separate obstacle layered on top of it.</p>
<p>The remainder of this document is unchanged by any of this. Every equation in §3 and §4 says exactly what it said before §1.1 through §1.4 existed. What those four subsections provide is an answer to a question the rest of the document was never obligated to ask, but that this version of it now can: not just <em>that</em> comprehension caps power, fidelity governs execution, and geometry is categorically harder than the four forces, but <em>why</em> — one mechanism, expressed in four equations, underneath everything else this document describes.</p>
<hr>
<h2>2. Core Philosophy</h2>
<p>There is no discrete resource pool — no mana, no stamina meter, no supply of aether to run out of — governing an aether-user's ceiling. The primary quantity that determines what is <em>possible</em> for a given practitioner is solved understanding of specific terms within the Grand Aether Equation (§3) — or, in the more mechanical vocabulary §1.3 introduces, of specific coupling channels between the aether layer and the fields above it. This has three consequences worth stating plainly.</p>
<p>First, theoretical capability scales with research rather than lineage: a character's ceiling is a direct function of what they, their teacher, or their order has actually proven. This has a specific, testable shape rather than being a vague appeal to "knowledge is power." A practitioner's ceiling is exactly the union of the coupling channels (§1.3) they personally have a proven functional form for — nothing more generous than that, and nothing less. Two siblings raised by the same teacher can diverge sharply in capability if one spends a decade proving a second <code>k_f</code> term while the other spends it drilling fidelity on the one they already have; the first gains ceiling, the second gains reliability, and neither gain transfers to the other automatically. An order that has spent three centuries fully diagonalizing <code>M_op</code> produces Master-tier practitioners as a matter of course, not because its members are innately gifted, but because the channel is simply sitting there, proven, waiting for anyone with the discipline to learn what has already been solved. This is also what makes theft of a rival's notes mean something specific in this system: it doesn't hand over their fidelity or their years of practice, but it can hand over a proven channel outright, collapsing what would otherwise be a lifetime of independent derivation into however long it takes to read and verify someone else's work.</p>
<p>Second, partial understanding is usable — a practitioner does not need to fully diagonalize a term to attempt an effect drawn from it — but committing that attempt to reality is an act of controlled risk, since they are asserting an outcome the mathematics has not yet guaranteed will hold. Partial understanding being usable is what keeps the ceiling from being an all-or-nothing wall. A caster three-quarters of the way to a full eigenbasis of <code>M_op</code> is not locked out of matter manipulation until the day the last eigenvector falls; they have real, usable command over whatever eigenvectors they have already solved (§3.3, Eq. 3.1e), and can extend an effect toward a specific, previously unsolved material the same way any other unproven claim gets made — by attempting it and finding out. What separates ordinary ambition from recklessness here is not the attempt itself, which this system never forbids, but whether the attempt is treated as the controlled risk it actually is. A caster who reaches for an unsolved eigenvector believing it behaves like an already-solved neighbor, without first testing that belief under <code>Sim[...]</code> (§3.7) wherever <code>Sim[...]</code> can actually test it, is gambling with a channel that Eq. 1.3 has no proven strength for — and the field does not extend a courtesy discount for a reasonable-sounding guess. That same attempt can be rehearsed first at zero real-world risk (§3.7); what cannot be rehearsed away is whether the underlying claim was sound. This is also why the most dangerous casters in this system are rarely the most powerful ones on paper; they are the ones whose confidence in an extrapolation has outrun what they have actually proven.</p>
<p>Third, the ceiling itself is mathematical rather than political: the complete equation cannot be solved in closed form by any finite mind (§3.4), so no character, however brilliant or ancient, can attain unconditional power. They can only extend how much of the equation they have solved. This is what keeps power in this system from ever being a matter of permission. No council, throne, or elder order can grant a practitioner comprehension they have not actually earned by solving the mathematics themselves — at best, an institution can hand over a channel it has already proven, as above, and that channel still has to be learned and internalized before it does anything. By the same logic, no council, throne, or elder order can effectively revoke comprehension once it has been solved; banishing a caster from an archive does not unsolve what that caster already carries in their own proven understanding. Political power and aether-comprehension can reinforce each other — a long-lived order with resources to fund centuries of research will out-produce an impoverished lone practitioner over time — but they are not the same axis, and a setting is free to use the gap between them: a deposed god-king who solved <code>Xi(Ae, g)</code> decades before losing his throne is exactly as dangerous stripped of his title as he was wearing it.</p>
<p>This is only half the system, however. What a practitioner has solved sets the <em>ceiling</em> on what they can do. It says nothing about how close to that ceiling any single casting actually lands — that is governed by two further, independent axes addressed in §3.5 and §3.6.</p>
<h4>The Three Axes, Named</h4>
<p>It is worth naming all three axes explicitly in one place, since §3 and §4 go on to develop each one separately and it is easy to lose track of how they relate. <strong>Comprehension</strong> (§2, §3.3, §3.4) is the ceiling: which coupling channels (§1.3) a practitioner has a proven functional form for, full stop. It does not vary casting to casting — on a given day, a practitioner's comprehension is exactly what it was the day before, unless the interval was spent extending it. <strong>Fidelity</strong> (§3.5, Eq. 3.2) is sourcing quality: how coherently a specific casting's <code>J_cast</code> (§1.2) reproduces the ideal structure for a channel the practitioner already has comprehension of. It varies casting to casting, hour to hour, and is exactly as sensitive to injury, distraction, and rush as §3.5 describes. <strong>Practice depth</strong> (§3.6, Eq. 3.4) is the medium-independence axis: whether a specific, individual channel has been drilled — live or under <code>Sim[...]</code>, per §3.7 — past the threshold <code>prac_min</code> at which it can be sourced through visualization alone, with no external scaffolding to stabilize <code>phi_actual</code> against.</p>
<p>These three axes are independent in the specific sense that moving along one does nothing to the other two by default, and each protects the system against a different failure mode a simpler design would fall into. Without comprehension as a hard ceiling, power would reduce to a fidelity-only contest — purely a measure of steady hands and practiced cadence, with no room for a setting to treat research, theory, and institutional knowledge as meaningfully load-bearing. Without fidelity as an independent, trainable axis, comprehension alone would make power a pure knowledge-check — a caster either "knows the spell" and it works at full strength, or doesn't and it doesn't — with no room for the ordinary craft-and-practice arc that makes an old, disciplined Novice a satisfying foil to a young, brilliant, sloppy Adept. Without practice depth as its own threshold, unassisted casting would either be free — undermining every scene where a visible glyph or audible cadence matters, tactically or dramatically — or impossible, foreclosing the entire silent, unreadable caster archetype, rather than being the earned, per-technique achievement §3.6 makes it.</p>
<p>None of the three is a proxy for either of the others, and any description of a character's power that tracked only one of them would misrepresent what that character can actually do. A hundred-year-old archivist with encyclopedic comprehension and unsteady hands, a battlefield-hardened duelist with a narrow repertoire executed flawlessly under pressure, and a prodigy who has drilled exactly one unassisted technique to invisible perfection while still needing a drawn glyph for everything else are three entirely different kinds of dangerous — and this system is built so that all three remain simultaneously coherent, comparable, and clearly distinguishable from one another by which axis, or axes, each one has actually maximized.</p>
<p><code>Sim[...]</code> (§3.7) is not a fourth axis. It is a zero-risk training method that accelerates progress along the second and third axes — fidelity and practice depth — without ever touching the first. This is worth stating plainly, because it is easy to mistake "a caster who drills obsessively under simulation" for "a caster gaining power for free." What <code>Sim[...]</code> actually grants is a caster who reaches their existing ceiling more reliably, and with less external scaffolding required to do it — never a caster whose ceiling has moved. Comprehension is earned exactly one way in this system: by solving mathematics that was not solved before. No amount of rehearsal, safe or otherwise, substitutes for that.</p>
<blockquote>
<p>If a term of the Grand Aether Equation has been fully solved, any effect it describes can be produced, at any scale. If a term has not been solved, no amount of intuition, willpower, or physical effort can substitute for the missing mathematics.</p>
</blockquote></div></section>
<section class="book" id="grand-equation"><header class="book-head"><span class="book-tag">§3.1–3.7</span><h1>The Grand Equation</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. §3.3 (The Power Hierarchy, with Eq. 3.1e–3.1g) is housed in <code>codex/power-hierarchy.md</code>.</em></p>
<hr>
<h2>3. The Grand Unified Aether Equation</h2>
<h3>3.1 Formal Statement</h3>
<p>The Grand Aether Equation is easiest to read as a small stack of named pieces rather than one dense line. The top level says only that reality-selection is a path integral over field configurations, weighted by an exponential of the aether action — everything else is what goes into that action.</p>
<p><strong>Eq. 3.1 — Grand Unified Aether Equation</strong></p>
<pre><code>A_op = Loop_dM[ Dpath(Ae) * exp( (i/hbar) * Action ) ]
</code></pre>
<p><strong>Eq. 3.1a — Aether Action</strong></p>
<pre><code>Action = Int[ sqrt(-g) * L_total ] d4x
</code></pre>
<p><strong>Eq. 3.1b — Total Lagrangian Density</strong></p>
<pre><code>L_total = L_gauge + L_quark + Xi(Ae, g)
</code></pre>
<p><strong>Eq. 3.1c — Gauge Term</strong> (the four fundamental forces)</p>
<pre><code>L_gauge = Sum_f[ k_f * Tr(F_f . F_f) ]
</code></pre>
<p><strong>Eq. 3.1d — Quark Term</strong> (matter coupling)</p>
<pre><code>L_quark = q_bar * (i*gam^u*D_u - M_op) * q
</code></pre>
<p>Read top-down: Eq. 3.1 selects a reality by weighting every possible field configuration by <code>exp(i/hbar * Action)</code>; the Action (Eq. 3.1a) integrates a single density, <code>L_total</code>, over all of spacetime; and <code>L_total</code> (Eq. 3.1b) is just the sum of three physically distinct contributions — how the four fundamental forces behave (Eq. 3.1c), how matter behaves (Eq. 3.1d), and how the aether field couples directly to spacetime's geometry, <code>Xi(Ae, g)</code>, which is developed further wherever it governs an effect (§3.3, §4.3, §4.9).</p>
<p>Note what this decomposition does, and does not, say about <code>Ae</code> itself. <code>Ae</code> appears explicitly only inside <code>Xi(Ae, g)</code> (Eq. 3.1b) — it does not appear inside <code>L_gauge</code> (Eq. 3.1c) or <code>L_quark</code> (Eq. 3.1d) at all, which is easy to misread as meaning aether has nothing to do with fire, lightning, or matter-level effects. §1.1 through §1.4 resolve this: a caster does not write <code>Ae</code> into <code>L_gauge</code> or <code>L_quark</code> directly. They source a ripple, <code>dAe</code> (Eq. 1.1), that propagates outward (Eq. 1.2) and couples into <code>F_f</code> or <code>M_op</code> from outside <code>L_total</code> altogether — distorting the values those terms take on, rather than appearing as an additional term written inside them. <code>Xi(Ae, g)</code> is the one place <code>Ae</code> is written directly into the Lagrangian, because the metric-sector coupling is native to <code>L_total</code> in a way the other two channels never are — §1.4 develops exactly why that one channel is built differently.</p>
<p>This equation is not solved for a single output. It selects which configuration becomes real within the caster's domain of comprehension, <code>dM</code> — comprehension of any one of Eq. 3.1a through 3.1d, or of <code>Xi(Ae, g)</code> specifically, is what defines how much of reality a given practitioner can actually reach. In the vocabulary of §1.3, <code>dM</code>'s boundary is precisely the set of coupling channels — <code>k_f</code> values, <code>M_op</code> eigenvectors, orders of <code>Xi(Ae, g)</code>'s expansion — for which a functional form has actually been proven. Nothing outside that boundary is reachable, no matter how favorably the rest of the path integral might otherwise weight it.</p>
<h3>3.2 Term Reference</h3>
<p>The table below restates the symbols from Eq. 3.1a–3.1d for quick reference. Symbols governing how a caster's invocation actually reaches these terms — <code>Ae_0</code>, <code>dAe</code>, <code>J_cast</code>, <code>G(x, x'; t, t'; g)</code> — belong to the mechanism developed in §1.1–§1.4 rather than to the Grand Equation's own definition, and are catalogued separately in §5.</p>
<div class="table-scroll"><table>
<thead>
<tr>
<th>Term</th>
<th>Eq.</th>
<th>Meaning</th>
<th>Governs</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Ae</code></td>
<td>3.1</td>
<td>The aether field itself</td>
<td>The substance every technique draws from</td>
</tr>
<tr>
<td><code>k_f</code></td>
<td>3.1c</td>
<td>Coupling constant for fundamental force <em>f</em> (EM, weak, strong, gravity)</td>
<td>Which force a caster's power expresses through</td>
</tr>
<tr>
<td><code>F_f</code></td>
<td>3.1c</td>
<td>Field-strength tensor for force <em>f</em></td>
<td>The "raw material" being bent</td>
</tr>
<tr>
<td><code>q_bar*(i*gam^u*D_u - M_op)*q</code></td>
<td>3.1d</td>
<td>Quark field dynamics with mass operator <code>M_op</code></td>
<td>Matter-level manipulation: density, decay, transmutation</td>
</tr>
<tr>
<td><code>M_op</code></td>
<td>3.1d</td>
<td>Mass operator (matrix, not scalar)</td>
<td>Must be diagonalized before matter manipulation is safe</td>
</tr>
<tr>
<td><code>Xi(Ae, g)</code></td>
<td>3.1b</td>
<td>Aether-to-spacetime coupling</td>
<td>Geometry- and causality-level effects</td>
</tr>
<tr>
<td><code>dM</code></td>
<td>3.1</td>
<td>Boundary of the caster's comprehension</td>
<td>Limits which field configurations are reachable</td>
</tr>
</tbody>
</table></div>
<p><em>§3.3 — The Power Hierarchy — follows here in the global numbering; it is housed in <code>codex/power-hierarchy.md</code>.</em></p>
<h3>3.4 The Unsolved Ceiling</h3>
<p>The full integral in Eq. 3.1 sums over infinitely many field configurations. No finite mind, artifact, or civilization can hold infinite information, so complete mastery is not merely difficult — it is provably impossible, in the same sense that no finite list can enumerate all real numbers. This is a property of the equation itself, not a rule imposed by any authority in the setting, which is what makes it uncheatable. It also gives long-lived factions a natural, centuries-long project: extending <code>dM</code> outward by solving one additional sub-term at a time.</p>
<p>This is also precisely the limit Eq. 1.4 attaches specifically to <code>Xi(Ae, g)</code>: even setting aside the sheer combinatorics of infinitely many field configurations, the metric channel's self-dependence means a complete solution would have to account for how solving it changes the very propagator being solved for — a moving target the other two channels never present. The Ceiling is therefore not one obstacle but at least two, stacked: an information-theoretic one that applies to <code>A_op</code> as a whole, and a specifically worse structural one that applies to <code>Xi(Ae, g)</code> in particular. This is why every serious attempt in this setting's history to push toward Legend and beyond has run out of both time and tractable mathematics at almost exactly the same point, rather than one giving out well before the other.</p>
<p>None of this makes long-term progress meaningless — it makes it cumulative rather than terminal. An order that treats extending <code>dM</code> as a multi-generational project is doing the only kind of progress this equation actually rewards: no member of that order will ever hold the complete integral, but the boundary itself moves outward permanently with each sub-term any of them manages to prove, in exactly the way Eq. 1.3's channels describe. An archive that has spent four centuries accumulating solved <code>k_f</code> values, a partial <code>M_op</code> eigenbasis, and a handful of validated perturbative orders of <code>Xi(Ae, g)</code> has produced something no single lifetime could: not a caster who has completed the equation, since §3.4 forbids that outright, but a caster trained inside that archive inherits a <code>dM</code> boundary that took four centuries to place, and can spend a single lifetime extending it a little further rather than rebuilding it from nothing. This is also worth remembering when weighing any claim, in-world, that a given order or bloodline is "closer" to completing the equation than a rival: closeness is measured in solved sub-terms, is auditable in principle — a term is either proven or it isn't — and confers no exemption from the underlying impossibility no matter how large the accumulated <code>dM</code> becomes.</p>
<h3>3.5 The Fidelity Principle</h3>
<p>Aether is not a consumable or storable form of energy. It is an ambient field, comparable in structure to a vacuum field that permeates all of spacetime uniformly — loosely analogous to the Higgs field in ordinary physics, which is present everywhere in equal measure and is not depleted by things coupling to it. Aether is not "gathered," drawn from a finite source, channeled from a reservoir, or restored by rest. There is no fatigue mechanic anywhere in this system that arises from aether scarcity, because there is nothing to be scarce.</p>
<p>What varies — and what actually determines the potency of any invoked effect — is not how much aether is available but how faithfully the caster's real-time invocation reproduces the ideal mathematical structure of the term being drawn on. This is formalized as the fidelity coefficient:</p>
<p><strong>Eq. 3.2 — Fidelity-Weighted Output</strong></p>
<pre><code>X_eff = X_ideal * Fid(t_ins)
Fid   = | &lt;phi_ideal | phi_actual(t_ins)&gt; |^2
0 &lt;= Fid &lt;= 1
</code></pre>
<p><code>X_ideal</code> is the theoretical output of a fully solved term, as established in §3.1–§3.3. <code>Fid</code> is the overlap between the ideal formal structure of that term, <code>phi_ideal</code>, and the caster's actual invocation of it, <code>phi_actual</code>, at inscription time <code>t_ins</code> — the literal precision of the handwriting, notation, gesture, or spoken cadence used to invoke it, whatever medium a given tradition favors. <code>Fid</code> is bounded above by 1: no invocation can exceed the potency the underlying, fully solved equation permits. It has no fixed floor: a rushed, careless, or distracted invocation of a perfectly well-understood equation can still produce an arbitrarily weak result.</p>
<p><code>phi_actual</code> here is exactly the source current <code>J_cast</code> introduced in Eq. 1.2, and <code>Fid</code> is a direct readout of how coherently that current matches the ideal shape a fully solved channel calls for. A caster does not experience this as an overlap integral, any more than they experience Eq. 1.2 as one; what they experience is that a careful, unhurried inscription produces a stronger flame, a firmer lift, or a cleaner fold, and a careless one produces a weaker version of the same thing. Eq. 3.2 is simply the bookkeeping that makes that everyday experience precise enough to reason about.</p>
<p><code>Fid</code> depends on the precision of the act of inscription itself, the caster's steadiness while performing it (injury, panic, or divided attention lowers achievable overlap), and time invested (a rushed inscription caps how high <code>Fid</code> can climb, regardless of underlying skill). Critically, this makes precision trainable independently of theory. A caster who has fully solved a term but executes it sloppily produces a weaker effect than one who has solved the identical term and inscribes it with care. Repeated, deliberate practice raises a caster's achievable <code>Fid</code> ceiling for a given equation over time — a distinct axis of growth from learning new mathematics, and one that rewards discipline and craft on its own terms. That repetition does not need to be live: §3.7 introduces a prefix notation that lets the same practice happen without ever committing the equation to reality.</p>
<p>Consider two casters, both holding an identical, fully solved <code>k_EM</code> term (§4.0, Eq. 4.0a), asked to bring a kettle to a boil. The first takes the time to trace the inscription with full attention, achieving <code>Fid</code> close to 1; the kettle boils in roughly the time a small stove flame would take. The second, distracted mid-inscription by an unrelated argument, achieves a <code>Fid</code> perhaps a third as high; the same kettle takes proportionally longer to reach the same temperature, with no risk to anyone involved regardless of how badly the second attempt is botched, since <code>k_EM</code> is a fully solved gauge-sector channel and this is a pure fidelity problem rather than a comprehension one (§1.3). Neither caster's theoretical ceiling changed at any point in this example. Only how close either of them landed to it did.</p>
<p><strong>Eq. 3.3 — Minimum Resolution Threshold</strong></p>
<pre><code>if Fid &lt; Fid_min:  X_eff ~ 0   (fails quietly — not a backlash)
</code></pre>
<p>Below a minimum threshold, the field simply does not resolve the invocation into any meaningful effect — the attempt fails quietly rather than misfiring destructively. This is the same resolution threshold §1.3 describes mechanically: below <code>Fid_min</code>, the ripple sourced by Eq. 1.2 is too weak or incoherent to register against Eq. 1.3's coupling channel at all, and what little of it exists simply rejoins the ambient <code>Ae_0</code> background rather than producing any distortion worth naming. This distinguishes a fidelity failure from a comprehension failure. Casting a poorly understood equation carefully can still misfire or backlash (Eq. 4.7), because the underlying mathematics itself is unproven. Casting a fully solved equation carelessly merely fails to manifest, because the equation is not in question — only its execution.</p>
<p>This principle applies universally. Any coupling constant, operator, or field term elsewhere in this document — <code>k_f</code>, <code>M_op</code>, <code>U_op</code>, <code>Xi</code> — should be read as implicitly scaled by <code>Fid</code> at the moment of casting, unless a technique's write-up states otherwise.</p>
<h3>3.6 Unassisted Invocation</h3>
<p>Inscription typically requires an external medium: a drawn glyph, a written formula, a spoken cadence, or some comparable physical act that gives <code>phi_actual</code> a stable form to take. The medium acts as scaffolding — it holds the structure steady while the caster reproduces it, which is part of why a careful physical inscription (§3.5) achieves higher fidelity than a rushed one.</p>
<p>In the vocabulary of §1.2, the medium's job is to hold a stable external copy of the target structure the caster is reproducing as <code>J_cast</code> — a drawn glyph doesn't produce the ripple itself; it gives the caster's attention something fixed to trace against while <code>J_cast</code> is generated. This is why a physical anchor raises achievable fidelity: it removes one entire source of drift from the invocation, so the caster's precision is limited only by their hand, breath, or voice, rather than also by how well they can hold an unaided mental copy of the target structure steady on its own.</p>
<p>At sufficient mastery of a specific term, a caster can dispense with that scaffolding entirely and hold <code>phi_actual</code> purely as a mental structure — visualizing the equation directly rather than writing, drawing, or speaking it. This is unassisted invocation. It removes the time cost of physical inscription and leaves no outward tell — no visible glyph, no audible cadence for an opponent to notice or interrupt — but it also removes the external stabilization the medium provided, so sustaining high fidelity without one is considerably harder. This capability is governed by practice depth for that specific term, tracked separately from tier or general comprehension:</p>
<p><strong>Eq. 3.4 — Unassisted Fidelity Ceiling</strong></p>
<pre><code>Fid_max(x, anchor) = Fid_max(x) * ( anchor + (1 - anchor) * Step( prac(x) - prac_min ) )
</code></pre>
<p><code>anchor = 1</code> when a physical medium is used; <code>anchor = 0</code> for pure mental visualization. <code>Step(...)</code> is the Heaviside step function — 0 below the threshold, 1 at or above it. <code>prac(x)</code> is practice depth for term <code>x</code>, built up through repeated deliberate execution, live or simulated (§3.5, §3.7); <code>prac_min</code> is the mastery threshold that must be crossed before that term can be cast without any anchor.</p>
<p>With a physical anchor, a caster's practiced fidelity ceiling always applies, regardless of how much they've specifically drilled unassisted casting. Without one, that ceiling only applies once practice depth for that exact term has crossed <code>prac_min</code>. Below threshold, an unassisted attempt collapses toward <code>Fid_min</code> and fails quietly (Eq. 3.3) — visualizing an unpracticed equation costs nothing but doesn't work, rather than backfiring.</p>
<p>Mechanically, <code>prac(x)</code> measures how well a caster has internalized <code>phi_ideal</code> for term <code>x</code> as a standalone mental structure, independent of any external copy — exactly the resource an anchor otherwise supplies for free. Below <code>prac_min</code>, that internal copy is close enough to correct that Eq. 1.2 still generates a coherent <code>J_cast</code>, but not close enough to hold steady without periodic correction from an external reference; above it, the internal copy is stable enough on its own that the reference is no longer needed at all. This is a threshold rather than a gradient because Eq. 3.4 models it as one — <code>Step(...)</code>, not a smoothly rising curve — reflecting an observation many traditions in this setting report independently of one another: casters consistently describe unassisted invocation as something that clicks into place all at once for a given technique, not as something that improves by fractions the way ordinary fidelity does.</p>
<p>This is a per-equation achievement, not a tier unlock. A practitioner might hold Adept-level comprehension (§3.3) across a dozen terms while only being able to invoke one or two of them unassisted, because <code>prac_min</code> has to be earned separately, through repetition, for each individual term. A narrower but more disciplined practitioner can invoke their one known technique unassisted while a broader, more knowledgeable rival still needs a drawn glyph for everything they do.</p>
<p>Because an unassisted invocation exists as a manipulable structure in the caster's mind rather than a fixed inscribed pattern, its terms can also be recomposed in real time — substituting a coupling constant, redirecting which force a technique expresses through, or merging two separately mastered terms mid-effect. This is still bounded by <code>dM</code> (§3.1): a caster can only ever recombine terms they have actually solved, never invent an unproven one on the spot. A live recombination that has never itself been practiced as a unit is treated, for the purposes of Eq. 3.4, as a fresh construction with <code>prac = 0</code> — it defaults to a quiet fizzle rather than working at full strength on the first attempt, unless the caster's grasp of both constituent pieces is deep enough to justify the combination as a direct corollary rather than a novel claim. Pushing a live recombination past what is actually justified reintroduces the ordinary risk of an under-proven claim (§2) — a mid-effect backlash, not a quiet failure — because at that point the caster is no longer executing solved mathematics with poor form. They are asserting new mathematics without having proven it. This particular risk is a comprehension risk rather than an execution one, which is exactly the piece that simulated invocation (§3.7) cannot pre-empt.</p>
<h3>3.7 Simulated Invocation</h3>
<p>Both axes developed above — comprehension (§2, §3.4) and fidelity (§3.5, §3.6) — are trained the same way: by attempting the equation. For a Novice boiling water, that costs nothing worth mentioning. For a caster drilling the destination calibration of an Overlay Fold, or the three interlocking dials of a Bound Singularity, "attempting the equation" until fidelity climbs has meant repeatedly courting a bleed, a backlash collapse, or a shell rupture just to get better at not causing one.</p>
<p>The <code>Sim[...]</code> prefix removes that cost from the fidelity side of practice. Placed before any equation or technique in this document, it instructs the aether field to evaluate the invocation in full — measuring overlap, projecting output, projecting failure energy where relevant — without ever passing the result into Eq. 3.1's <code>Loop_dM[...]</code> selection. Nothing is heated, moved, folded, or curved. The structure is held, measured, and released.</p>
<p><strong>Eq. 3.5 — Simulated Invocation</strong></p>
<pre><code>Sim[ X ](t_ins) -&gt; { Fid(t_ins), X_eff_proj, E_back_proj }
Loop_dM[ ... ]  not evaluated
</code></pre>
<p><code>X_eff_proj</code> and <code>E_back_proj</code> are exactly what Eq. 3.2 and Eq. 4.7 would output if the invocation were real — the field runs the same calculation either way. What <code>Sim[...]</code> withholds is the final commit: reality is never asked to select a configuration around this particular attempt, so there is nothing left to fizzle, bleed, or collapse into.</p>
<p>In the vocabulary of §1.2 and §1.3, this is exactly what <code>Sim[...]</code> measures, and exactly what it cannot. Eq. 1.2 computes <code>dAe</code> from <code>J_cast</code> regardless of whether the result is ever allowed to reach Eq. 1.3's coupling channel, so a simulation reads off the ripple's coherence in full. What it never does is actually test that ripple against the channel it's aimed at, because <code>Loop_dM[...]</code> — the step that would let reality confirm or reject the caster's assumed coupling strength — is the one step <code>Sim[...]</code> explicitly skips. A caster drilling the Bound Singularity's shell tuning (§4.3) under <code>Sim[...]</code> can run the full three-dial coordination thousands of times, arriving at a shell fidelity indistinguishable from a lifetime of live practice, without once risking the shell rupture that same practice would have courted in the field. What that same caster cannot do is discover, this way, whether their assumed value for <code>Xi(Ae, g)</code> at the shell radius was ever actually correct — that question only gets answered the first time <code>Loop_dM[...]</code> is allowed to run, which is also the first moment a wrong assumption becomes a real backlash rather than a hypothetical one.</p>
<p>Two consequences follow directly from how that readout is generated, and both are load-bearing rather than incidental:</p>
<ul>
<li><strong>Fidelity practice is free.</strong> Because <code>Fid</code> (Eq. 3.2) measures the overlap between <code>phi_ideal</code> and the caster's actual execution, and that overlap can be measured without ever manifesting the effect, <code>prac(x)</code> (§3.6) accumulates identically whether a given repetition was run live or under <code>Sim[...]</code>. A caster can drill the exact glyph, cadence, or mental structure for a technique at full complexity, thousands of times, with nothing at stake, and arrive at the same unassisted fidelity ceiling they would have reached the hard way.</li>
<li><strong>Comprehension is not.</strong> <code>Sim[...]</code> scores the caster against <code>phi_ideal</code> as they currently understand it; it has no independent way to check whether that understanding is actually correct. A fully solved term simulates perfectly, because believed and true <code>phi_ideal</code> are the same object. A term that is only partially solved, or a live recombination the caster believes is a valid corollary (§3.6) but isn't, will simulate beautifully and still backlash the first time it's cast for real — the flaw was never in execution, and execution is all <code>Sim[...]</code> was ever checking. Rehearsal cannot certify a claim that comprehension hasn't earned.</li>
</ul>
<p>This is why the two failure modes established in §3.5 and §3.6 stay asymmetric even after <code>Sim[...]</code> enters the picture. A quiet fizzle from low fidelity is now something no disciplined caster should ever suffer in the field — it can be trained away in complete safety beforehand. A backlash from an unproven or misjudged term cannot be pre-empted this way; the caster learns the mathematics was wrong at the same moment reality does. Simulated invocation makes craft free to perfect. It makes no comparable promise about theory.</p></div></section>
<section class="book" id="power-hierarchy"><header class="book-head"><span class="book-tag">§3.3</span><h1>The Power Hierarchy</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. This file houses §3.3, which sits between §3.2 and §3.4 in <code>codex/grand-equation.md</code>.</em></p>
<hr>
<h3>3.3 The Power Hierarchy</h3>
<p>Five of the tiers below mark qualitative jumps in comprehension — a new term of the Grand Equation opened up entirely, or, for Legend, an already-opened term pushed to a categorically different scale. Between each of the first three of those pairs sits a named subclass: a rung defined not by a new term but by an <em>incomplete</em> version of the next one. The Sovereign→Legend step is the sole exception — per Eq. 3.1g it is the same term at a larger <code>R_dom</code>/<code>t_dom</code> rather than a new one, so it admits no partial-solution rung between them. These are where most named characters in a story actually live, since full tier transitions are rare, momentous events, while partial progress toward the next one is the ordinary, unglamorous work of the vast majority of a practitioner's career.</p>
<div class="table-scroll"><table>
<thead>
<tr>
<th>Tier</th>
<th>What's solved</th>
<th>Capabilities</th>
<th>Prevalence</th>
</tr>
</thead>
<tbody>
<tr>
<td>Novice</td>
<td>One <code>k_f</code> term, closed form</td>
<td>Single-force effects: fire/lightning (EM), localized strong/weak-force bursts — worked examples in §4.0</td>
<td>Common</td>
</tr>
<tr>
<td>Journeyman</td>
<td>Two or more <code>k_f</code> terms, each closed form, not yet cross-coupled</td>
<td>Can produce more than one single-force effect, but must switch between them rather than blend</td>
<td>Common</td>
</tr>
<tr>
<td>Adept</td>
<td>Multiple <code>k_f</code> terms, combined</td>
<td>Cross-force effects, combination techniques</td>
<td>Uncommon</td>
</tr>
<tr>
<td>Artisan</td>
<td>Partial diagonalization of <code>M_op</code> (Eq. 3.1e)</td>
<td>Narrow, proven matter-tricks on specific known materials; general transmutation is not yet safe</td>
<td>Uncommon</td>
</tr>
<tr>
<td>Master</td>
<td>Full eigenbasis of <code>M_op</code></td>
<td>Transmutation, accelerated decay/healing, binding-energy control</td>
<td>Rare; often order leadership</td>
</tr>
<tr>
<td>Warden</td>
<td>First-order perturbative <code>Xi(Ae, g)</code> (Eq. 3.1f)</td>
<td>Narrow, tightly-scoped metric effects, valid only in already-proven special cases</td>
<td>Very rare</td>
</tr>
<tr>
<td>Sovereign</td>
<td>Closed-form <code>Xi(Ae, g)</code> over a bounded domain (Eq. 3.1g, finite <code>R_dom</code>)</td>
<td>Localized spacetime warps, minor time dilation, small causality bends, the Overlay Fold, a held Bound Singularity</td>
<td>A handful per era</td>
</tr>
<tr>
<td>Legend</td>
<td>Closed-form <code>Xi(Ae, g)</code> with <code>R_dom</code> pushed to effective permanence (Eq. 3.1g)</td>
<td>Regional-scale metric engineering; standing folds; singularities as lasting geographic features</td>
<td>A handful across recorded history</td>
</tr>
</tbody>
</table></div>
<p><strong>The Unsolved Ceiling</strong> — the full <code>A_op</code> integral: total, unconditional reality rewriting. Not a tier, and occupied by no one; it is the limit the whole ladder points at without reaching. See §3.4.</p>
<p>Read against §1.3, this table is a map of which coupling channel a tier has opened and how much of it. Novice through Adept live entirely inside <code>delta(F_f)</code>, the gauge-sector channel — one coupling constant, then several, then several combined. Artisan and Master live inside <code>delta(M_op)</code>, the quark-sector channel, differing only in how much of <code>S</code>, the solved eigenvector subset in Eq. 3.1e, has been filled in. Warden through Legend live inside <code>delta(g)</code>, the metric-sector channel — the one channel where, per §1.4, solving more of it does not simply mean "a bigger version of the same kind of proof," because the propagator each new increment relies on has already been reshaped by every increment solved before it. This is also why the table's five gauge-and-matter tiers can, in principle, be pursued to full closed-form completion by a sufficiently dedicated caster within an ordinary lifetime, while even the earliest metric-sector tier is marked "very rare": the first two channels are hard because there is a great deal to prove; the third is hard because proving any of it changes the terms of what's left to prove.</p>
<p>Note that tier reflects <em>comprehension</em> only. A Novice with excellent execution fidelity (§3.5) can reliably outperform an Adept who casts carelessly — tier sets the ceiling, not the outcome of any single casting. This holds identically for every subclass: a Warden who has drilled their one proven special case under <code>Sim[...]</code> (§3.7) until it is flawless will outperform a careless Sovereign, without either of their actual comprehension having changed.</p>
<p><strong>Journeyman</strong>, <strong>Artisan</strong>, and <strong>Warden</strong> share a common shape worth naming once rather than three times: each is defined by holding a real, non-zero <em>piece</em> of the next tier's term rather than none of it. That piece is exactly as usable — and exactly as risky (§2) — as any other partial solution in this system. A Journeyman's two <code>k_f</code> terms are each individually as solid as a Novice's one; what's missing is the cross-term connecting them, and attempting to force one anyway is an unproven claim like any other. An Artisan's diagonalized subset of <code>M_op</code> is genuinely solved — Eq. 3.1e below formalizes exactly which eigenvectors — but reaching for a material outside that subset is not "harder Artisan work," it's Master-tier work attempted without Master-tier comprehension, and it fails the way §2 says it should. A Warden's perturbative slice of <code>Xi(Ae, g)</code> is the same story at the highest ordinary stakes: real, solved, narrow, and unforgiving of extrapolation.</p>
<p><strong>Eq. 3.1e — Partial Diagonalization</strong> (extends the mass operator in Eq. 3.1d)</p>
<pre><code>M_op_partial = Sum_{i in S} lam_i * |e_i&gt;&lt;e_i|
</code></pre>
<p><code>S</code> is the finite, proper subset of <code>M_op</code>'s eigenvectors an Artisan has actually solved — as opposed to the complete basis required for Master tier. Effects drawn from an eigenvector inside <code>S</code> behave exactly as Eq. 3.1d describes; a material or transformation whose eigenvector isn't in <code>S</code> isn't merely weaker, it's unmodeled, and invoking it anyway is a comprehension gamble, not an execution one. This is why Artisans are so often defined by a signature material or effect — steel, bone, salt, rot — rather than a percentage of general competence: <code>S</code> tends to grow one hard-won eigenvector at a time, and a career can pass with <code>S</code> holding only two or three.</p>
<p><strong>Eq. 3.1f — Perturbative Aether-Geometry Coupling</strong> (extends <code>Xi(Ae, g)</code> from Eq. 3.1b)</p>
<pre><code>Xi_pert(Ae, g) = Xi_0 + eps * Xi_1 + O(eps^2)
</code></pre>
<p>A Warden has solved <code>Xi_0</code> and <code>Xi_1</code> — the leading terms of a perturbation series around flat, uncurved spacetime — but not the closed form <code>Xi(Ae, g)</code> itself that Sovereign tier requires. <code>O(eps^2)</code> and beyond are simply unknown. This is why Warden techniques only work "in already-proven special cases": the series was only ever validated near the specific configurations it was expanded around, and pushing <code>eps</code> — the size of the departure from flat space — past where it was tested is exactly the kind of extrapolation §2 warns about, with metric-level consequences instead of merely thermal or material ones.</p>
<p><strong>Eq. 3.1g — Domain Persistence</strong> (governs how far a solved <code>Xi(Ae, g)</code> reaches)</p>
<pre><code>Xi_valid(x, t):  |x - x0| &lt; R_dom   and   t &lt; t_dom
</code></pre>
<p>Sovereign and Legend are the same mathematics at different scales of <code>R_dom</code> and <code>t_dom</code>, not different equations. A Sovereign's closed-form solution is genuinely complete — no perturbative gap, unlike a Warden's — but only within a bounded radius and for a bounded duration: a held fold, a contained singularity, a warp that must eventually be released. A Legend has pushed those same two dials far enough that, for any practical purpose, the effect no longer has a measurable edge: a singularity that has stood for a generation, a causality bend that reshaped a region's history rather than one afternoon of it. Neither <code>R_dom</code> nor <code>t_dom</code> is ever literally infinite — that would require the term to escape Eq. 3.1's dependence on a caster's finite <code>dM</code> entirely, which is precisely what §3.4 forbids. Legend is a very large finite number, not an exception to the rule that finite numbers are all this system permits.</p>
<h4>The Ascent Beyond Legend</h4>
<p>Every path above shares one property: it extends exactly one term of <code>L_total</code>, in isolation, and stops the moment that term is fully solved. Legend is where that pattern runs out of room — <code>Xi(Ae, g)</code> has no further "more solved" to reach for once its domain is effectively unbounded. What lies beyond isn't a ninth tier. It's a fork: four historically-attested directions, each abandoning the "one term at a time" discipline that got a caster to Legend and reaching instead for something the Grand Equation was never decomposed to make easy. None has ever been completed. None ever can be, per §3.4 — the reasons differ by path, but the impossibility is the same impossibility. That is what makes them paths <em>toward</em> divinity rather than routes to it: a character can spend a lifetime, or several, closing the distance, and the distance does not reach zero.</p>
<p>In §1.3's terms, three of the four paths still target a coupling channel — they simply target it whole rather than as a single instance. The Tetrarch Path targets the entire gauge channel at once, seeking one coupling in place of all four <code>k_f</code> values. The Demiurge Path targets the entire quark channel at once, seeking the rule that generates <code>M_op</code>'s eigenvectors rather than any finite collection of them. The Cosmographer Path targets the entire metric channel pushed past where even Legend stops, and inherits every self-referential difficulty §1.4 attaches to that channel, compounded rather than resolved by how much of it has already been solved. Only the Communion Path steps outside Eq. 1.3 entirely — it does not touch a coupling channel at all, but the boundary <code>dM</code> in Eq. 3.1 that determines which channels are reachable in the first place, which is exactly what makes it the odd one out in every account of these four paths that survives from the traditions that attempted them.</p>
<ul>
<li>
<p><strong>The Tetrarch Path</strong> (gauge unification) targets a single coupling that would replace all four <code>k_f</code> terms in Eq. 3.1c at once:
  <code>L_gauge -&gt; k_unified * Tr(F_unified . F_unified)      -- no closed form for k_unified is known</code>
  A caster who gets meaningfully close no longer needs to choose which force an effect expresses through — fire, gravity, and the strong force become facets of one coupling rather than four separate ones. What this path never touches is <code>L_quark</code> or <code>Xi(Ae, g)</code>: a Tetrarch is close to unstoppable in raw force application and no more able to reshape matter or spacetime than whatever Artisan- or Sovereign-level work they separately hold.</p>
</li>
<li>
<p><strong>The Demiurge Path</strong> (matter-generation) pushes past Master's full diagonalization toward deriving the <em>generating structure</em> of <code>M_op</code> itself — not a complete list of solved eigenvectors, but the rule that produces them, letting the caster predict and originate stable matter configurations that have never been observed rather than only manipulate known ones:
  <code>M_op -&gt; Gen(dM)      -- no closed form for Gen is known</code>
  This is the most overtly "creator-god" path — new substances, new organisms, brought into being directly from the aether — and the most narrowly bounded: it says nothing whatsoever about force, geometry, or causality. A Demiurge who has never touched <code>Xi(Ae, g)</code> can be killed by a well-placed fold like anyone else.</p>
</li>
<li>
<p><strong>The Cosmographer Path</strong> (unbounded geometry) is Sovereign/Legend's own trajectory carried past where Legend stopped — <code>R_dom</code> and <code>t_dom</code> pushed toward true global, permanent scope rather than merely very large:
  <code>Xi_valid(x, t)  as  R_dom -&gt; infinity, t_dom -&gt; infinity      -- never attained; see Eq. 3.1g</code>
  A Cosmographer within reach of this limit can reshape terrain, climate, or the causal structure of an entire region as a permanent fact of geography rather than a held effect. The limit itself is §3.4's Unsolved Ceiling wearing a single term's clothing: reaching it in full would mean <code>Xi(Ae, g)</code> alone had escaped the finite-<code>dM</code> dependence every other term in this system obeys, which the Ceiling's proof forbids for the equation as a whole and, by the same argument, for any one of its pieces pushed to totality.</p>
</li>
<li>
<p><strong>The Communion Path</strong> (comprehension itself) is the only one of the four that does not target a term of <code>L_total</code> at all — it targets <code>dM</code>, the boundary in Eq. 3.1 that every other path treats as a fixed limit to push against from inside:
  <code>dM_total = Union(dM_1, dM_2, ..., dM_n)      -- pooling proven comprehension across n minds</code>
  Rather than one mind solving more mathematics, a Communion merges the <em>proven</em> — never the merely believed, per §3.7's warning about <code>Sim[...]</code> — comprehension domains of several practitioners into one acting boundary. It is the fastest of the four paths to produce dramatic short-term gains, and the most explicitly horrifying in most traditions that have attempted it, since what's merged is not knowledge alone but the minds that held it. <code>dM_total</code> still cannot exceed the union of what its members actually solved; a Communion of a thousand Novices is a very large Novice, not a Legend, and folding a Legend into one changes the ceiling of the merge but not the mathematics of what the Ceiling itself forbids.</p>
</li>
</ul>
<p>No character, order, or god-king in this setting has ever completed one of these four paths, let alone more than one at once — and completing more than one would still fall short, since a true solution to Eq. 3.1 requires <code>L_gauge</code>, <code>L_quark</code>, <code>Xi(Ae, g)</code>, and <code>dM</code> all at once, coupled to each other in ways none of these paths even attempts to resolve. This is deliberate room for a story rather than a gap in the mechanics: a Cosmographer and a Demiurge can each be the most powerful individual in their own domain and mutually vulnerable outside it, a self-proclaimed god can be sincerely wrong about having arrived, and the actual endpoint of any path can remain permanently, provably out of frame.</p></div></section>
<section class="book" id="techniques-novice"><header class="book-head"><span class="book-tag">§4.0</span><h1>Novice Techniques</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. Sovereign-tier techniques (§4.1–§4.3) are housed in <code>codex/techniques-sovereign.md</code>; Legend-tier techniques (§4.10) in <code>codex/techniques-legend.md</code>; the Spell Directory (§4.4) in <code>codex/spell-directory.md</code>.</em></p>
<hr>
<h2>4. Applied Techniques</h2>
<p>Every technique below is an instance of the same three-step chain formalized in §1.2–§1.3: source a ripple (<code>J_cast</code>), propagate it (<code>G</code>), and couple it into one of the three channels above (<code>delta(F_f)</code>, <code>delta(M_op)</code>, <code>delta(g)</code>). Most entries compress this chain into a single closed-form line, the way ordinary practice always does — no caster consciously reasons through a propagator integral to boil a kettle. §4.0 walks the chain in full once, for Eq. 4.0a, so that the shorthand used everywhere else in this Part can be read with the underlying mechanism in mind rather than as an unexplained set of coincidentally similar formulas.</p>
<h3>4.0 Novice Techniques</h3>
<p>This section marks the start of the applied curriculum proper — the point where a student moves from reading the Grand Equation's structure (§3) to actually casting from it. Every technique here uses exactly one term from Eq. 3.1c, in closed form, with no combination and no metric-level involvement. The same terms reappear, in far more complete form, throughout the rest of Part 4; the throughline is deliberate — lifting a pebble and binding a singularity both trace back to gravity, at opposite ends of the hierarchy (<code>k_grav</code> in Eq. 3.1c versus <code>Xi(Ae, g)</code>; see Eq. 4.0b's note).</p>
<p><strong>Eq. 4.0a — Thermal Excitation ("Boiling Water")</strong></p>
<pre><code>P_in = k_EM * Fid * Ae_local^2
dT/dt = P_in / (m * c_p)
</code></pre>
<p>The caster concentrates aether density at a point of contact, <code>Ae_local</code>, and the electromagnetic coupling <code>k_EM</code> converts that into injected power, <code>P_in</code>. From there it's ordinary thermodynamics: temperature rises at a rate set by the substance's mass and specific heat capacity, exactly as if the energy had come from a stove rather than a caster. This is usually the first equation any aether student is taught, precisely because it has no failure mode worth naming — a low-<code>Fid</code> attempt just heats the water more slowly.</p>
<p><strong>From ripple to result.</strong> It's worth tracing Eq. 4.0a back through §1.1–§1.3 once, in full, since every other technique in this document compresses the same chain of reasoning into a single closed-form line the way this one does. A caster inscribes a glyph or cadence that constitutes <code>J_cast(x', t')</code>, localized at the point of contact. Eq. 1.2 propagates this through the essentially flat, unperturbed geometry around an ordinary kettle — no metric distortion is involved, so the propagator <code>G</code> reduces here to its simplest, unperturbed form — producing a local perturbation <code>dAe(x, t) = Ae_local</code>, concentrated exactly where the caster intended. Eq. 1.3's gauge channel then converts that local perturbation into a distortion of the electromagnetic field-strength tensor, <code>delta(F_EM) = k_EM * Ae_local</code>, scaled by the fidelity of the sourcing current per Eq. 3.2. What Eq. 4.0a's <code>P_in = k_EM * Fid * Ae_local^2</code> actually represents is the power delivered by that distorted field once it couples to the water's own electromagnetic structure at the molecular level — the squared <code>Ae_local</code> reflects that the power delivered by a field is proportional to the square of the field's own strength, exactly as it would be for a coil or a flame. Everything after that line is ordinary thermodynamics, precisely because the ripple's job ends the moment it hands off a real, physical field distortion to physics that already knows what to do with one. This is the pattern every equation in the rest of this Part follows, whether or not it is spelled out again explicitly: source a ripple, propagate it, couple it into a channel, then let the receiving field behave exactly as it always would once genuinely disturbed.</p>
<p><strong>Eq. 4.0b — Minor Levitation ("Lifting a Feather")</strong></p>
<pre><code>F_net = m_obj * g_local * (1 - k_grav * Fid)
</code></pre>
<p><code>k_grav</code>, like the other three <code>k_f</code> terms in Eq. 3.1c, treats gravity as a simple force-coupling — enough to push, pull, or, as here, partially cancel a local pull. It cannot bend the metric itself; that requires <code>Xi(Ae, g)</code> (§3.3, §4.3). This is why lifting a pebble and generating the Bound Singularity's well (§4.3) both trace back to gravity but sit at opposite ends of the Power Hierarchy (§3.3) — one is a single closed-form term, the other is a partial solution to an entirely different piece of the Grand Equation.</p>
<p><strong>Eq. 4.0c — Minor Cohesion Boost ("Hardening a Surface")</strong></p>
<pre><code>E_bind_eff = E_bind * (1 + k_strong * Fid)
</code></pre>
<p>A temporary, proportional boost to a material's ordinary binding energy — enough to resist a scratch or a minor impact better than it otherwise would. This is a single-term nudge to an existing property, not a rewrite of the material itself; true transmutation requires a fully diagonalized <code>M_op</code> (§3.3, §4.8), which is Master tier, not Novice.</p>
<p><strong>Eq. 4.0e — Ripple Sense ("Feeling a Working")</strong></p>
<pre><code>S_detect(x, t) = k_EM * dAe_nearby(x, t)          -- read-only; no delta(F_EM) is sourced
</code></pre>
<p>The proven <code>k_EM</code> channel is not a one-way valve. The same coupling that lets a Novice push a distortion into the electromagnetic field also lets them notice one arriving from someone else's nearby casting — often well before it registers to an ordinary bystander as heat, light, or a felt static charge. This is a read, never a source: <code>S_detect</code> never itself becomes a <code>delta(F_EM)</code> in Eq. 1.3's sense, so neither Eq. 3.3's resolution threshold nor Eq. 1.3's fizzle/backlash distinction has anything to bite on here. A Novice can hold Ripple Sense continuously at zero risk — the cost is entirely informational rather than mechanical: this equation alone tells a caster <em>that</em> aether is moving nearby, not <em>whose</em> it is, what it's for, or whether it's friendly. Distinguishing those is a discipline built on top of this equation, not a further term inside it.</p>
<p>Adept- and Master-tier applied techniques are written up in <code>codex/techniques-adept.md</code> (§4.6) and <code>codex/techniques-master.md</code> (§4.8); Journeyman, Artisan, and Warden in their own respective files (§4.5, §4.7, §4.9) — see <code>codex/overview.md</code> for the full map. Every equation above is a single closed-form <code>k_f</code> term (or, for Eq. 4.0e, a passive read of one); the next stage up is holding more than one such term without a cross-term (Journeyman, §4.5), then combining them (Adept, §4.6); past that, the quark-sector <code>M_op</code> machinery from Eq. 3.1d opens partially (Artisan, §4.7) and then completely (Master, §4.8).</p>
<p><em>Note: Eq. 4.0d (Decay Nudge), which completes the four-force set of Novice worked examples, is defined in the Spell Directory (<code>codex/spell-directory.md</code>, §4.4), where it was introduced.</em></p></div></section>
<section class="book" id="techniques-journeyman"><header class="book-head"><span class="book-tag">§4.5</span><h1>Journeyman Techniques</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. Novice worked examples (§4.0) are housed in <code>codex/techniques-novice.md</code>; the Spell Directory's Journeyman entries (J-01–J-07, §4.4) are formalized by this section's equation.</em></p>
<hr>
<h3>4.5 Journeyman Techniques</h3>
<p>A Novice solves exactly one <code>k_f</code> term of Eq. 3.1c in closed form. A Journeyman solves two or more of the same terms — each still closed-form, each still a Novice-tier equation in its own right — without the cross-term <code>Chi(f1, f2)</code> (§3.3, §4.6) that would let one sourced ripple satisfy both channels of Eq. 1.3 at once. That absence is not a gap waiting to be filled by effort; it is the tier's defining structural fact. Lacking <code>Chi</code>, a Journeyman cannot blend two effects — only alternate between them, completely resolving one before the other begins. Eq. 4.13 formalizes exactly this: the total output of a Journeyman working two techniques is not a sum of simultaneous contributions but a sum of non-overlapping ones.</p>
<p><strong>Eq. 4.13 — Sequential Invocation Overhead</strong></p>
<pre><code>X_seq(t) = X_1(x,t) * Win_1(t) + X_2(x,t) * Win_2(t)
Win_1(t) . Win_2(t) = 0   for all t
tau_switch = t_start(Win_2) - t_end(Win_1)
</code></pre>
<p><code>X_1</code> and <code>X_2</code> are any two solved Novice-tier expressions from §4.0 or the Spell Directory (§4.4) — Eq. 4.0a through 4.0d or any entry built on them. <code>Win_1(t)</code> and <code>Win_2(t)</code> are activation-window indicator functions: each is 1 while its technique is actively producing output and 0 otherwise. The product constraint <code>Win_1(t) . Win_2(t) = 0</code> is the entire content of "closed form without a cross-term" written as an equation — at no instant is a Journeyman drawing output from both channels at once, because no <code>Chi(f1,f2)</code> exists yet to let a single ripple satisfy Eq. 1.3 twice simultaneously. Every entry in the Spell Directory's Journeyman section (J-01 through J-07) is a named illustration of <code>X_seq(t)</code>: Ember Handoff (J-01) is Eq. 4.0a's window closing before N-GR-03's opens; Two-Handed Smith (J-05) is Eq. 4.0a and Eq. 4.0c alternating for as long as the hammering lasts.</p>
<p><code>tau_switch</code> is the dead time between windows — the interval a Journeyman spends re-inscribing a glyph or re-settling a cadence (§3.6) between one closed-form casting and the next. It is real cost, not bookkeeping: a caster is producing neither <code>X_1</code> nor <code>X_2</code> while <code>tau_switch</code> elapses, and a task that assumes continuous output (a Storm-Step-style discharge-into-leap, say) simply cannot be performed at Journeyman tier no matter how short <code>tau_switch</code> gets, because Eq. 4.13 has no term for simultaneous output at all. Drilled practice — the kind Bladeline Feint (J-07) or Watch-Fire Relay (J-06) exist to train — shrinks <code>tau_switch</code> considerably, and a seasoned Journeyman's switch can become nearly imperceptible to an observer. But "nearly imperceptible" is not zero, and it cannot structurally become zero without <code>Chi(f1,f2)</code>: the instant <code>tau_switch -&gt; 0</code> with the windows still disjoint is not a faster Journeyman, it is the Adept transition itself, since a genuine zero-gap alternation and a true simultaneous blend become indistinguishable only once <code>Chi</code> exists to make the blend real rather than merely fast. This is why Adept fidelity enters the Adept Combination Pattern (Eq. 4.15, §4.6; catalogued in §4.4) squared rather than linearly — the two effects are no longer protected from each other's wobble by taking turns.</p></div></section>
<section class="book" id="techniques-adept"><header class="book-head"><span class="book-tag">§4.6</span><h1>Adept Techniques</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. The six named Adept combinations (AD-01–AD-06) already catalogued in the Spell Directory (§4.4) are formalized by this section's two equations. Journeyman's Sequential Invocation Overhead (Eq. 4.13) is housed in <code>codex/techniques-journeyman.md</code>.</em></p>
<hr>
<h3>4.6 Adept Techniques</h3>
<p>A Journeyman holds two or more solved <code>k_f</code> terms (Eq. 1.3) but no cross-term between them: each casting sources a single <code>dAe(x,t)</code>, propagates it through <code>G(x,x';t,t';g)</code>, and couples it to exactly one gauge sector at a time. Moving between sectors mid-working costs <code>tau_switch</code> (Eq. 4.13) — dead time in which the field is sourced but coupled to nothing. The Adept tier is defined by removing that overhead for a specific pair of forces, not by holding more <code>k_f</code> terms in general.</p>
<p><strong>Eq. 4.14 — Cross-Coupling Function</strong></p>
<pre><code>Chi(f1, f2) = Overlap[ delta(F_f1), delta(F_f2) ; dAe ]      0 &lt;= Chi &lt;= 1
</code></pre>
<p><code>Chi(f1,f2)</code> measures how coherently a single sourced ripple <code>dAe</code> can be shaped to satisfy two gauge-sector coupling channels at once, rather than sequentially. <code>Overlap[...]</code> is evaluated against the same ripple driving both <code>delta(F_f1)</code> and <code>delta(F_f2)</code> simultaneously — it is not a measure of two separate ripples occurring close together in time. <code>Chi = 0</code> describes exactly the Journeyman's condition: the two channels are reachable, but only by discarding one coupling to stand up the other, hence <code>tau_switch</code>. <code>Chi = 1</code> describes a ripple shaped so completely that both channels are satisfied with no interference loss between them, a limit no known technique reaches.</p>
<p>Solving <code>Chi</code> for one specific unordered pair is the achievement that promotes a caster from Journeyman to Adept <em>for that pair only</em>. This comprehension is exactly as granular as the Journeyman case: a caster can hold <code>Chi(EM,Strong)</code> (Flash-Forge, AD-01) as a real, nonzero function while <code>Chi(EM,Gravity)</code> (Storm-Step, AD-02) remains unsolved and equal to zero for them. With respect to that second pair they are still, formally, Journeyman — tier is a per-pair predicate, not a global rank. This is why a single caster's sheet can legitimately list several Adept techniques and several unsolved pairs side by side.</p>
<p><strong>Eq. 4.15 — Adept Combined Output</strong></p>
<pre><code>X_combo = k_f1 * k_f2 * Fid^2 * Chi(f1, f2)
</code></pre>
<p>This is the Spell Directory's Adept Combination Pattern (§4.4), now carrying a formal number so it can be cross-referenced against Eq. 4.14 rather than asserted on its own. Given solved <code>k_f1</code>, <code>k_f2</code>, and a nonzero <code>Chi(f1,f2)</code>, output scales with the product of both force couplings, gated by fidelity squared.</p>
<p>The squaring of <code>Fid</code> is not a stylistic echo of the product <code>k_f1 * k_f2</code> — it falls directly out of what <code>Chi</code> measures. <code>Chi</code> is only defined against a <em>single</em> ripple satisfying two channels at once; there is no second, independent ripple to fall back on if the first is imperfect. A wobble in that one ripple's shape degrades the overlap term in Eq. 4.14 for both channels simultaneously, because both channels are reading the same <code>dAe</code>. Contrast the Journeyman case: a poorly-sourced ripple on one <code>k_f</code> leaves the other <code>k_f</code> — sourced by a separate, later ripple — untouched, so a weak casting on one channel does not propagate loss into the other. The Adept's shared-ripple architecture has no such firewall. Fidelity therefore enters the combined output once for each channel it degrades, and since it degrades both channels through the same underlying flaw, the two factors are not independent draws — they are the same <code>Fid</code> value applied twice. Linear <code>Fid</code> would understate how much a marginal caster loses by attempting the blend; <code>Fid^2</code> is the honest accounting of a single point of failure taxed twice.</p>
<p>One consequence worth stating plainly: <code>Fid^2</code> falls faster than <code>Fid</code> for any <code>Fid &lt; 1</code>, so the practical gap between a mediocre Adept and a skilled one is wider, on the same technique, than the corresponding gap would be for a Journeyman running either force alone. Adept tier trades away switching overhead for a steeper fidelity penalty — it is a different failure mode, not a strictly easier one.</p>
<hr>
<p><strong>Closing note.</strong> Four fundamental forces admit exactly six unordered pairs, and all six are already named and catalogued in the Spell Directory (§4.4): AD-01 through AD-06. Eq. 4.14 and Eq. 4.15 formalize the mechanism behind all six; no seventh pair exists to discover. An Adept's further growth along this axis is therefore bounded: depth on pairs already held — raising <code>Fid</code> and refining <code>Chi(f1,f2)</code> toward its upper bound — or breadth across whichever of the six pairs remain unsolved for them. Growth beyond that ceiling belongs to a different channel entirely, reserved for Artisan and Master tier.</p></div></section>
<section class="book" id="techniques-artisan"><header class="book-head"><span class="book-tag">§4.7</span><h1>Artisan Techniques</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. The seven named Artisan specialties (AR-01–AR-07) already catalogued in the Spell Directory (§4.4) are formalized by this section's two equations, which extend Eq. 3.1e (<code>codex/power-hierarchy.md</code>).</em></p>
<hr>
<h3>4.7 Artisan Techniques</h3>
<p>Every Artisan entry in §4.4 has, until now, been described narratively — a named material and a narrow use, with the formal weight carried entirely by Eq. 3.1e's partial diagonalization. That equation establishes <em>which</em> eigenvectors an Artisan has solved; it does not by itself say what casting one actually produces, or what happens when a caster reaches past it. The two equations below close that gap, giving AR-01 through AR-07 the same kind of shared backbone that Eq. 4.0a already gives every Novice entry.</p>
<p><strong>Eq. 4.16 — Eigenvector Draw ("Signature Working")</strong></p>
<pre><code>Effect_i = lam_i * Fid * dAe_local,      e_i in S   (S per Eq. 3.1e)
</code></pre>
<p>This is the quark-sector channel's version of Eq. 4.0a. Where a Novice's <code>k_EM</code> is a single fixed coupling shared by every caster who touches the electromagnetic channel, <code>lam_i</code> is not fixed at all — it is the specific eigenvalue an individual Artisan has personally solved for a specific eigenvector <code>e_i</code>, and it exists in their working equations only because <code>e_i</code> already sits inside their proven <code>S</code>. A caster with salt in <code>S</code> has a <code>lam_i</code> for salt's lattice and nothing else; a caster with iron in <code>S</code> has an entirely different <code>lam_i</code>, tied to an entirely different <code>e_i</code>. The equation's shape is otherwise identical to Eq. 4.0a in every way that matters: <code>Fid</code> still scales the outcome linearly, <code>dAe_local</code> is still the sourced ripple doing the actual work, and a flawless casting against a low <code>Fid</code> still produces a correct but weak effect rather than an incorrect one. AR-01 through AR-07 are seven independent instances of this one equation, each keyed to its own <code>lam_i</code> and <code>e_i</code>. Nothing about Eq. 4.16 changes when an eighth material joins the catalog — it is the eigenvector entering <code>S</code> that does the work of unlocking a technique, not any new mathematics.</p>
<p><strong>Eq. 4.17 — Off-Basis Extrapolation</strong></p>
<pre><code>E_back_mat = Int_V[ | lam_guess - lam_true |^2 ] dV,      e_guess not in S
</code></pre>
<p>This is the failure mode Eq. 4.16 cannot produce by construction, because Eq. 4.16 only ever fires for <code>e_i in S</code>. Eq. 4.17 fires the moment a caster targets a material whose eigenvector was never solved and proceeds anyway on the strength of a resemblance — bronze reasoned from iron, porcelain reasoned from glass, tallow reasoned from rot. <code>lam_guess</code> is the eigenvalue the caster assumes by that analogy; <code>lam_true</code> is whatever the real eigenvalue would be, which was never measured because <code>e_guess</code> was never in <code>S</code> to begin with, and which the caster has no way to know in advance. The ripple goes out shaped for <code>lam_guess</code>; the material answers according to <code>lam_true</code>; the mismatch between them does not dissipate quietly. It integrates over the working volume as absorbed stress, exactly as Eq. 4.7 describes for an unresolved metric mismatch at Sovereign tier — this is the same backlash mechanism, not an analogous one, expressed through the quark-sector channel instead of the metric-sector channel. That equivalence is the point: §1.3's claim that this reflection-not-dissipation behavior is a universal property of unresolved channel mismatch, rather than something peculiar to the Overlay Fold, is proven precisely by the fact that Eq. 4.7 and Eq. 4.17 are the identical integral applied to two different channels. An Artisan who has never so much as glimpsed <code>Xi(Ae, g)</code> can still absorb backlash shaped exactly like a failed fold — smaller in most cases, since a single mismatched lattice rarely stores as much stress as a mismatched region of spacetime, but never zero, and never survivable to extrapolate from twice.</p>
<p>The practical lesson §3.3 already states in prose — that reaching outside a signature material is Master-tier work attempted without Master-tier comprehension — now has a cost attached to it in the same units used everywhere else in this Codex. A guild that trains Artisans trains Eq. 4.16 by widening <code>S</code> one eigenvector at a time, and trains against Eq. 4.17 by drilling the discipline of recognizing, before casting, whether a target material's <code>e_i</code> was ever actually solved.</p></div></section>
<section class="book" id="techniques-master"><header class="book-head"><span class="book-tag">§4.8</span><h1>Master Techniques</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. Artisan's partial-diagonalization techniques (§4.7, Eq. 4.16–4.17) are housed in <code>codex/techniques-artisan.md</code>; this section is the natural completion of that work once <code>S</code> closes over the full eigenbasis.</em></p>
<hr>
<h3>4.8 Master Techniques</h3>
<p>Every technique below is downstream of one fact, and one fact only: a Master has closed <code>S</code>. Where Eq. 3.1e restricts an Artisan to a finite, proper subset of <code>M_op</code>'s eigenvectors — a signature material, and nothing outside it — Master tier is defined in the Power Hierarchy (§3.3) as possession of the <em>full</em> eigenbasis. Nothing about the underlying mechanics changes between the two tiers; what changes is that <code>S</code> stops being a boundary. A Master has not learned a new kind of magic. A Master has finished solving the one <code>M_op</code> every caster has been working inside since Eq. 3.1d.</p>
<p><strong>Eq. 4.18 — Full Transmutation</strong></p>
<pre><code>M_op_full = Sum_{all i}[ lam_i * |e_i&gt;&lt;e_i| ],      S = complete eigenbasis
q_new = U_transmute(M_op_full) * q_old
</code></pre>
<p>An Artisan's <code>M_op_partial</code> (Eq. 3.1e) addresses whatever eigenvectors that Artisan's signature material happens to fall under, and only those — an Artisan of Iron can true a blade because iron's lattice is solved, and cannot touch bronze for the identical reason. <code>M_op_full</code> removes that restriction by exhaustion rather than by any new operator: every <code>lam_i</code> is known, so <code>S</code> is no longer a proper subset of anything, it <em>is</em> the eigenbasis. <code>U_transmute</code> is the unitary that acts on that completed basis, reassigning which combination of solved eigenvectors a given quantity of matter expresses — it moves <code>q_old</code> to <code>q_new</code> the way <code>U_op</code> (Eq. 4.1) moves a caster between two points, except the "points" here are two material identities rather than two locations. This is the mechanical content of "true transmutation": not a nudge to one property of a known material, but a rewrite of which material the field is, using an operator that Eq. 4.0c's authors never had the eigenbasis to write. Wood becomes stone, lead becomes something nearer gold, decayed tissue becomes sound tissue — not by analogy, but because <code>q_new</code> is a different solution of the same operator <code>q_old</code> was.</p>
<p><strong>Eq. 4.19 — Universal Binding &amp; Decay Control</strong></p>
<pre><code>E_bind_eff(x) = E_bind(x) * (1 + s * c_M * Fid),        any x  (S complete)
Gamma_eff(x)   = Gamma_0(x) * (1 + s * c_M * Fid)
s = +1 (boost / hasten)  or  s = -1 (weaken / arrest),  chosen at inscription
</code></pre>
<p>This is Eq. 4.0c and Eq. 4.0d, generalized in the one direction Novice tier could never take them. Eq. 4.0c boosts <code>E_bind</code> for a single material at a single point; Eq. 4.0d nudges <code>Gamma_0</code> for whatever trace unstable material happens to be present. Both are narrow because <code>k_strong</code> and <code>k_weak</code> are single-channel couplings applied to whatever is already at hand. Eq. 4.19 instead runs on <code>c_M</code>, the matter-coupling constant Eq. 1.3 folds directly into <code>M_op</code>'s own definition — and with <code>S</code> complete, <code>c_M</code> is no longer confined to a signature subset. The variable <code>x</code> ranges over any material a Master's eigenbasis covers, which is to say all of it.</p>
<p>The consequence worth stating plainly: Eq. 4.19 is a single equation, and <code>E_bind_eff</code> and <code>Gamma_eff</code> are its two faces. Cast with <code>s = +1</code> at living tissue's <code>E_bind(x)</code>, it is accelerated healing — wounds closing at a pace no Novice cohesion boost could sustain across a whole body rather than one seam. The same equation pointed at <code>Gamma_eff(x)</code> is controlled aging or decay — a Master can hasten decomposition (<code>s = +1</code>) as precisely as another Master arrests it (<code>s = -1</code>), because both are the same term with the direction <code>s</code> and <code>x</code>'s target chosen differently. The direction parameter is the same operator-level choice a Novice already makes between Eq. 4.0c and Brittle Ease (N-ST-02), or between Eq. 4.0a and Cold Ember (N-EM-02) — never a sign on <code>Fid</code> itself, which Eq. 3.2 bounds to <code>0 &lt;= Fid &lt;= 1</code>. What Novice tier taught as two unrelated techniques narrow enough to need separate names — Eq. 4.0c's cohesion boost, Eq. 4.0d's decay nudge — Master tier reveals as one equation that was always going to unify once <code>c_M</code> stopped being fenced off by an incomplete <code>S</code>. Binding-energy control and decay control were never two magics. They were one equation, waiting on a complete eigenbasis to be written down.</p></div></section>
<section class="book" id="techniques-warden"><header class="book-head"><span class="book-tag">§4.9</span><h1>Warden Techniques</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. This is the first metric-sector (<code>delta(g)</code>) applied technique below Sovereign (§4.1–§4.3, <code>codex/techniques-sovereign.md</code>) and Legend (§4.10, <code>codex/techniques-legend.md</code>), and the first place §1.4's propagator self-dependence bites at ordinary-technique scale rather than only in theory.</em></p>
<hr>
<h3>4.9 Warden Techniques</h3>
<p>A Warden works the metric channel one order past where a Novice can safely stand. Where Novice technique moves <code>Ae_local</code> at an arbitrary point without ever touching <code>g</code>, a Warden has solved the leading terms of Eq. 3.1f's perturbation series — <code>Xi_0</code> and <code>Xi_1</code> — and can therefore nudge spacetime's own curvature by a small, known amount. The catch is built into the word "perturbative": the series was expanded around flat, uncurved spacetime and validated only near that expansion point. Nothing licenses using it anywhere else. A Warden's entire practical range is therefore defined not by how strong <code>eps</code> (departure from flat space) they <em>can</em> push, but by how far a specific configuration has already been <em>proven safe</em>.</p>
<p><strong>Eq. 4.20 — Perturbative Curvature Whisper</strong></p>
<pre><code>delta(g)_warden = eps * Xi_1 * Bump(r, R_proven)
</code></pre>
<p><code>R_proven</code> is not a radius chosen for convenience — it is a specific, previously-validated geometry: a familiar room, a mapped stretch of road, a fold-site the Warden (or their teacher) has tested before. <code>Bump(r, R_proven)</code> reuses Eq. 4.8's localization shape to confine <code>eps * Xi_1</code> to that neighborhood and let it fall to zero outside it. This is why Warden effects read as small and domestic rather than grand: a doorway that briefly weighs less to cross, a step that briefly doesn't quite touch the floor. There is no version of this technique that produces a general-purpose geometry effect — the moment the target leaves <code>R_proven</code>, the underlying series has left the region it was ever shown to track.</p>
<p><strong>Eq. 4.21 — Perturbative Extrapolation Backlash</strong></p>
<pre><code>E_back_pert = Int_V[ | Xi(Ae,g) - (Xi_0 + eps*Xi_1) |^2 ] dV,      for  eps &gt; eps_valid(R_proven)
</code></pre>
<p><code>eps_valid(R_proven)</code> is the largest departure-from-flat-space that the Warden's specific proven configuration has actually tested — not a theoretical bound, a demonstrated one. Push <code>eps</code> past it and the truncated series <code>Xi_0 + eps*Xi_1</code> quietly stops tracking the true, closed-form <code>Xi(Ae,g)</code> that only a Sovereign has solved (§1.4, §3.3). The gap between what the Warden's math predicts and what the aether field actually does does not vanish; per §1.3's claim that this mechanism is universal across channels, it reflects back as absorbed curvature stress — the identical shape already seen in Eq. 4.7's Overlay Fold mismatch and in the sibling Artisan backlash equation, just written in the metric channel's own terms. A Warden who extends a proven doorway-weight trick to an unmapped stairwell, or widens <code>eps</code> past what a tested fold-site has shown, is not attempting a bigger version of the same trick — they are extrapolating an unvalidated curve and eating whatever the true <code>Xi(Ae,g)</code> turns out to be at that point.</p>
<p>In practice this makes Warden discipline almost entirely about <code>R_proven</code> bookkeeping: knowing exactly which geometries have been tested, to what <code>eps_valid</code>, and refusing every request — including one's own — to reuse the result somewhere merely <em>similar</em>. It is also why so little Warden technique is ever formally shared: a proof of safety is tied to one specific geometry, not portable to the next.</p></div></section>
<section class="book" id="techniques-sovereign"><header class="book-head"><span class="book-tag">§4.1–4.3</span><h1>Sovereign Techniques</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. The Part 4 preamble and Novice worked examples (§4.0) are housed in <code>codex/techniques-novice.md</code>. Eq. 3.1g is explicit that Sovereign and Legend "are the same mathematics at different scales... not different equations" — this file defines that mathematics once, at Sovereign's bounded scale; <code>codex/techniques-legend.md</code> (§4.10) extends the same constructions to Legend's effectively-permanent scale without re-deriving them.</em></p>
<hr>
<h3>4.1 The Overlay Fold</h3>
<p>The Overlay Fold relocates a caster from point A to point B without displacing mass. Rather than accelerating a body through space, it asserts a conformal identification between the two coordinates — establishing that, for the duration of the effect, A and B are the same point in the aether field — after which the caster's position resolves to the far side. At Sovereign scope, "for the duration of the effect" means a bounded hold: minutes to hours, per Eq. 3.1g's <code>R_dom</code>/<code>t_dom</code>, released once the caster arrives. A fold held open across years rather than hours is the same mathematics pushed to Legend scale (§4.10) — a different discipline of upkeep, not a different derivation.</p>
<p><strong>Eq. 4.1 — Overlay Identification</strong></p>
<pre><code>Xi_overlay(A, B) = Ae*(A) * U_op(A, B) * Ae(B) - Delta( g(A) - Om2(x) * g(B) )
</code></pre>
<p><strong>Eq. 4.2 — Null-Displacement Constraint</strong> (guarantees mass-neutrality)</p>
<pre><code>Loop_traj[ (T_ae - T_mat) ] d(traj) = 0
</code></pre>
<div class="table-scroll"><table>
<thead>
<tr>
<th>Symbol</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>U_op(A, B)</code></td>
<td>Unitary phase-lock operator identifying point A with point B</td>
</tr>
<tr>
<td><code>Delta(g(A) - Om2(x)*g(B))</code></td>
<td>Forces the two local metrics to match, up to a conformal scale factor</td>
</tr>
<tr>
<td><code>Om2(x)</code></td>
<td>Conformal factor absorbing scale differences between A and B</td>
</tr>
<tr>
<td><code>T_ae</code>, <code>T_mat</code></td>
<td>Stress-energy tensors of the aether field and of the caster's body</td>
</tr>
</tbody>
</table></div>
<p>Three practical constraints follow directly from this mathematics rather than being imposed as separate rules. The destination's local metric must already be known to the caster, since <code>Om2(x)</code> in Eq. 4.1 cannot be computed for an unmeasured location. No momentum can be carried through the fold, since the null-displacement constraint in Eq. 4.2 requires the aether and matter stress-energy tensors to cancel exactly along the transition path. And the difficulty of a given fold scales with the magnitude of the conformal mismatch between A and B, so a jump between similar environments is markedly easier than one between, for instance, sea level and a mountain summit.</p>
<p>Per §3.5–§3.6, <code>U_op</code> itself is subject to both the Fidelity Principle and Unassisted Invocation: a sloppily inscribed fold uses the same equation but a weaker effective operator, and a sufficiently practiced caster can hold the fold open with a visualized <code>U_op</code> alone, with no visible casting tell.</p>
<p>In §1.3's terms, the Overlay Fold routes entirely through the metric channel: Eq. 4.1's <code>Delta(g(A) - Om2(x)*g(B))</code> term is a <code>delta(g)</code> distortion by another name, which is exactly why holding a fold open engages the self-referential propagator behavior described in §1.4 rather than the simpler, static channel behavior a Novice's <code>k_f</code> techniques enjoy. This is the mechanical reason a fold cannot simply be "aimed and released" the way Eq. 4.0a can: the moment <code>U_op(A, B)</code> begins identifying the two coordinates, the caster's own ripple is propagating through a geometry it is simultaneously reshaping, and everything that follows in §4.2 — the superposed state, the possibility of a fizzle, bleed, or backlash collapse — is what that self-referential propagation looks like while it is still in flight.</p>
<h3>4.2 The Collapse Condition</h3>
<p>While the identification operator <code>U_op</code> is active, the caster does not occupy A or B individually. They exist in a superposed state between the two.</p>
<p><strong>Eq. 4.3 — Superposed State Vector</strong></p>
<pre><code>|Phi(t)&gt; = a(t)|A&gt; + b(t)|B&gt;
|a|^2 + |b|^2 = 1
a(0) = 1,  b(0) = 0
</code></pre>
<p><strong>Eq. 4.4 — Fold Evolution</strong> (how holding the fold shifts probability from A toward B)</p>
<pre><code>i*hbar * d/dt [a; b] = [ [0, U_op(A,B)], [U_op(A,B)*, 0] ] * [a; b]
</code></pre>
<p>A lower-fidelity <code>U_op</code> (§3.5) produces slower, weaker oscillation here — a sloppily inscribed fold is not just riskier but literally slower to resolve, independent of the caster's theoretical grasp of the technique.</p>
<p><strong>Eq. 4.5 — Resolution Functional</strong> (probability of clean arrival at the moment of release)</p>
<pre><code>P_arrive(t_rel) = | &lt;B | Phi(t_rel)&gt; |^2 * exp( -G_dec * t_rel )
</code></pre>
<p><strong>Eq. 4.6 — Decoherence Rate</strong></p>
<pre><code>G_dec = eta * ( mismatch(Om2) )^2 / K(B) + s_int
</code></pre>
<div class="table-scroll"><table>
<thead>
<tr>
<th>Symbol</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>eta</code></td>
<td>Proportionality constant setting how strongly conformal mismatch drives decoherence</td>
</tr>
<tr>
<td><code>mismatch(Om2)</code></td>
<td>Mismatch between the caster's assumed and the true conformal factor of B</td>
</tr>
<tr>
<td><code>K(B)</code></td>
<td>Caster's knowledge coefficient for B — prior visits, sensory data, measurement quality</td>
</tr>
<tr>
<td><code>s_int</code></td>
<td>External disruption injected mid-fold</td>
</tr>
</tbody>
</table></div>
<p>Three outcomes are possible depending on when and how the caster releases the fold. A <strong>fizzle</strong> occurs when release comes too early, before <code>b</code> has grown appreciably; the state collapses back to A harmlessly — nothing is absorbed and nothing reflects, the quiet failure of §1.3 and Eq. 3.3, reached here by releasing before <code>b</code> has grown rather than by low <code>Fid</code>; the only cost is the wasted casting. A <strong>bleed</strong>, or echo, occurs when release happens mid-oscillation, with <code>a</code> and <code>b</code> both significant; neither location fully resolves, and both sites display brief duplicate images of the caster and nearby objects until decoherence forces a resolution on its own. The most severe outcome, a <strong>backlash collapse</strong>, occurs when <code>G_dec</code> spikes sharply during the hold — from interference, or from a poorly measured destination — forcing an ungraceful resolution. The unresolved metric mismatch is then absorbed directly into the caster as curvature stress:</p>
<p><strong>Eq. 4.7 — Backlash Energy</strong></p>
<pre><code>E_back = Int_V[ | g(A) - Om2(x) * g(B) |^2 ] dV
</code></pre>
<p>The magnitude of this injury scales with how inaccurately the caster understood the destination going in, tying the consequence directly to <code>K(B)</code> in Eq. 4.6 rather than to chance. Note that this failure mode is a comprehension failure (an unproven or misjudged <code>mismatch(Om2)</code>), distinct from the quiet, non-destructive fizzle that results from a purely low-fidelity casting of an otherwise well-understood fold (§3.5, Eq. 3.3).</p>
<p>This is the general fizzle/backlash distinction of §1.3 in its original, specific form: Eq. 4.6's decoherence rate is what happens to Eq. 1.2's propagating ripple when the destination geometry is mismeasured, and Eq. 4.7's backlash energy is exactly the reflected coupling mismatch §1.3 describes, computed for this one technique before the general mechanism existed to name it. Eq. 4.17 and Eq. 4.21, in the Artisan and Warden technique files respectively, show the same mechanism again in the quark and perturbative-metric channels — this was never a rule unique to the Overlay Fold.</p>
<h3>4.3 The Bound Singularity</h3>
<p>The Bound Singularity generates a genuine, localized region of extreme spacetime curvature — a caster-made gravity well, precise enough at sufficient mastery to cross the threshold into a true event horizon — while actively suppressing its influence on everything outside a chosen boundary. It is built from three separately solved components that must be tuned together: a well source, a counter-curvature containment shell, and a time-dilation boundary that gives the shell a genuine causal edge rather than just a canceled field on paper. This sits at Sovereign tier (§3.3): sourcing real curvature from the aether field, rather than from ordinary mass-energy, requires <code>Xi(Ae, g)</code> — the same term that governs every other geometry-level effect in this system. At Sovereign scope the well is held and then released; a well maintained as a standing landmark across generations is the same construction at Legend scale (§4.10, Eq. 4.23).</p>
<p>This technique is the clearest possible illustration of §1.4's propagator self-dependence, because it doesn't merely encounter that self-dependence as an obstacle — it is built by deliberately exploiting it three times over, at three different radii, at once. The well source (Eq. 4.8) sources a <code>delta(g)</code> that reshapes the local propagator inside <code>R_core</code>; the counter-curvature shell (Eq. 4.9) sources a second <code>delta(g)</code>, timed and shaped to exactly cancel the first everywhere outside <code>R_core</code>; and the lapse tuning (Eq. 4.10) shapes proper time itself within the shell so that whatever self-reference remains between the two doesn't merely look canceled on paper but is causally sealed against escaping at all. Each of these three castings is, in Eq. 1.4's terms, modifying the very medium the other two are propagating through, in real time — which is exactly why they cannot be solved or inscribed independently and then simply layered together. A caster who has nailed the well and the shell separately, but has never practiced holding both simultaneously, is attempting a live recombination in the sense of §3.6, with everything that implies about the risk of doing so before it has been proven as a unit.</p>
<p><strong>Eq. 4.8 — Localized Well Source</strong></p>
<pre><code>Curv(g)(r) = Xi(Ae, g) * Bump(r, R_core)
</code></pre>
<p><code>Curv(g)</code> is the curvature built from the metric <code>g</code> (the same role the Einstein tensor plays in ordinary general relativity). <code>Bump(r, R_core)</code> is a smooth localization function equal to roughly 1 inside the core radius <code>R_core</code> and falling to 0 outside it, which is what keeps the well from sourcing curvature everywhere at once. Because the source is <code>Xi(Ae, g)</code> rather than ordinary matter, no real mass is ever required to build the well — consistent with the rest of this system never treating mass as a necessary ingredient of an effect.</p>
<p><strong>Eq. 4.9 — Counter-Curvature Shell (the anti-gravity field)</strong></p>
<pre><code>Curv(g)(r) = -Xi(Ae, g) * Shell(r, R_core, R_shell)      for R_core &lt;= r &lt;= R_shell
</code></pre>
<p><code>Shell(r, R_core, R_shell)</code> is nonzero only in the annulus between the core and the outer containment radius <code>R_shell</code>, and is engineered to carry curvature-charge equal and opposite to the well's. By an argument analogous to Birkhoff's theorem — a spherically symmetric exterior vacuum depends only on the total enclosed curvature-charge — nulling that total collapses the exterior field to flat space, to leading order. This is the "anti-gravity field": not a force pushing outward, but a matched counter-curvature that leaves nothing for the far field to respond to.</p>
<p><strong>Eq. 4.10 — Containment Lapse &amp; Horizon Tuning</strong></p>
<pre><code>lapse(r) = sqrt( 1 - 2*k_newton*M_ae(r) / r )      for R_core &lt;= r &lt;= R_shell
lapse(R_shell) -&gt; 0   when   2*k_newton*M_ae(R_shell) = R_shell
</code></pre>
<p><code>M_ae(r)</code> is the enclosed aether-mass-equivalent within radius <code>r</code> (the same role the mass function plays inside a Schwarzschild interior solution). <code>k_newton</code> is a fixed background constant — how strongly mass-energy curves spacetime at all, playing the role Newton's constant plays in ordinary gravity — distinct both from <code>Xi(Ae, g)</code>, the active technique the caster wields to source that curvature from aether in the first place, and from <code>k_grav</code>, the solvable gauge coupling of Eq. 3.1c that Novice techniques like Eq. 4.0b draw on. No caster solves or scales <code>k_newton</code>; it is a property of spacetime, not a channel. Tuning <code>R_shell</code> and <code>M_ae(r)</code> so the horizon condition is satisfied exactly at the shell boundary does more than cancel a number: it makes proper time within the shell approach a full stop as <code>r -&gt; R_shell</code> from inside, so nothing inside crosses out in any finite amount of external time. This is what makes the containment causal, not merely a canceled field on paper.</p>
<p><strong>Eq. 4.11 — Residual Outreach</strong></p>
<pre><code>Curv_ext(r) = (1 - Fid_shell) * Xi(Ae, g)|_{R_core} / r^3      for r &gt; R_shell
</code></pre>
<p><code>Fid_shell</code> is the fidelity coefficient (§3.5) specifically for the shell term, Eq. 4.9 — tracked separately from the fidelity of the well source or the lapse tuning, since each is inscribed and practiced on its own. With perfect shell fidelity, external curvature is exactly zero: full containment. Imperfect fidelity leaks a residual field, but only as a higher multipole — falling off as <code>r^-3</code> rather than the ordinary <code>r^-2</code> monopole a real, uncontained mass would produce. A sloppy containment doesn't reveal the well's true strength; it reveals a faint tidal echo of it.</p>
<p><strong>Eq. 4.12 — Unified Bound Singularity Form</strong></p>
<pre><code>Curv(g)(r) = Xi(Ae,g) * [ Bump(r,R_core) - Shell(r,R_core,R_shell) ]
             + (1 - Fid_shell) * Xi(Ae,g)|_{R_core} * r^-3 * Step(r - R_shell)

subject to:  lapse(r) = sqrt(1 - 2*k_newton*M_ae(r)/r)
             lapse(R_shell) -&gt; 0   when   2*k_newton*M_ae(R_shell) = R_shell
</code></pre>
<p>This is Eq. 4.8, Eq. 4.9, and Eq. 4.11 folded into a single piecewise definition, using <code>Bump</code>, <code>Shell</code>, and <code>Step</code> as switches that select the active term by radius: near <code>R_core</code> it reduces to the raw well; in the annulus out to <code>R_shell</code> it reduces to the counter-curvature shell; beyond <code>R_shell</code> it reduces to the residual leak. Eq. 4.10 is kept as an explicit constraint rather than merged into the main line, since the lapse function governs the rate of proper time — a different mathematical object from curvature — and folding it in would misrepresent time dilation as just another curvature term rather than the condition that makes the shell causally real.</p>
<p><strong>Failure modes.</strong> Two distinct disasters are possible, and they are not the same disaster. A <strong>shell rupture</strong> occurs when <code>Fid_shell</code> drops below <code>Fid_min</code> mid-technique (§3.5): the counter-curvature cancellation fails outright, and the well's full field snaps outward with no warning beyond whatever residual leak (Eq. 4.11) was already showing. <strong>Horizon migration</strong> is subtler: Eq. 4.9's cancellation can hold perfectly — zero measurable external curvature — while Eq. 4.10's horizon condition is still off, meaning the interior was never actually causally sealed. A containment that looks flawless by every instrument available may not be flawless over long enough timescales; a caster who has only mastered the shell and not the lapse tuning has built something that looks safe and isn't. This is a direct consequence of Eq. 1.4: the lapse function depends on the same reshaped geometry the well and shell are simultaneously producing, so a caster who has only validated Eq. 4.9's cancellation in isolation — rather than the full, mutually-reshaping system of all three castings together — has solved a version of the containment that assumed a propagator the actual, combined casting never provides.</p>
<p>Because <code>R_core</code>, <code>R_shell</code>, and <code>M_ae</code> are independent dials within the same technique, a caster who has crossed <code>prac_min</code> (§3.6) on all three can adjust them live — shrinking the shell to swallow an incoming threat, then re-expanding and resealing it, without ever fully dropping containment in between. Attempting the same adjustment through pen-and-glyph inscription is far slower, since each change requires re-inscribing the relevant term from scratch.</p>
<p>At Sovereign scope, "horizon migration" and the residual-leak monitoring above are checked once, at casting time, and again at release. Maintaining that same check across a standing well held for a generation — rather than an afternoon — is Legend tier's specific addition; see Eq. 4.23 in <code>codex/techniques-legend.md</code>.</p></div></section>
<section class="book" id="techniques-legend"><header class="book-head"><span class="book-tag">§4.10</span><h1>Legend Techniques</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. Split out from Sovereign tier per Eq. 3.1g's own framing ("the same mathematics at different scales, not different equations") — the base constructions (Overlay Fold, Bound Singularity) are defined once, in <code>codex/techniques-sovereign.md</code> (§4.1–§4.3, Eq. 4.1–4.12), and are not re-derived here.</em></p>
<hr>
<h3>4.10 Legend-Scale Techniques</h3>
<p>Legend tier solves nothing that Sovereign tier has not already solved. Per Eq. 3.1g, the two are the same mathematics differing only in <code>R_dom</code> and <code>t_dom</code>; every field term, every fold identification, every shell construction in §4.1–§4.3 carries forward unchanged. What changes is that the objects those equations describe stop holding still. A Sovereign's Overlay Fold or Bound Singularity is validated once, against a destination or a local vacuum that is, for all practical purposes, a fixed snapshot across an afternoon's <code>t_dom</code>. Push <code>t_dom</code> out to <code>t_dom_legend</code> — years, a lifetime, a standing generation — and the snapshot assumption fails: buildings rise and fall at the far end of a fold, riverbeds migrate, a mountain's mass redistributes by fractions no Sovereign-scale casting ever needed to track. Legend tier is the discipline of managing that drift. It is an upkeep problem, not a new derivation.</p>
<p><strong>Eq. 4.22 — Standing Fold Persistence</strong></p>
<pre><code>Xi_overlay_legend(A,B) = Xi_overlay(A,B)   [Eq. 4.1],   subject to R_dom, t_dom -&gt; t_dom_legend   (Eq. 3.1g)
t_drift = interval between re-validations of Om2(x) at B required to keep mismatch(Om2) below G_dec's safe threshold (Eq. 4.6)
</code></pre>
<p>The identification term itself is untouched — a Standing Fold is Eq. 4.1, held. What Legend adds is <code>t_drift</code>: the clock on how long the true conformal factor <code>Om2(x)</code> at B can be trusted before the caster's assumed value has wandered far enough that <code>mismatch(Om2)</code> in Eq. 4.6 starts driving <code>G_dec</code> toward failure. A Sovereign never measures <code>t_drift</code> because their hold ends before it matters. A Legend, or more commonly the order left to maintain the fold after the founding caster is gone, treats <code>t_drift</code> as the site's central operating parameter — the re-survey schedule the whole institution is built around.</p>
<p><strong>Eq. 4.23 — Standing Singularity &amp; Recertification Interval</strong></p>
<pre><code>Curv(g)_legend(r) = Curv(g)(r)   [Eq. 4.12],   subject to t_dom -&gt; t_dom_legend   (Eq. 3.1g)
t_recert = max interval between Fid_shell re-inscriptions such that Curv_ext(r) (Eq. 4.11) stays below the ambient background noise floor for the singularity's full t_dom_legend
</code></pre>
<p>Likewise, a Held Star or any other landmark-scale singularity is the identical well-shell-lapse construction of Eq. 4.12, not a new geometry. <code>Fid_shell</code> is never inscribed once and left; over <code>t_dom_legend</code> it decays, and the residual leak of Eq. 4.11 — falling off as <code>r^-3</code> but never zero — creeps upward until it would register at long range as an uncontained mass. <code>t_recert</code> bounds how long the shell can go between re-inscription before that happens.</p>
<p>Both equations share the same shape for a reason: Legend tier introduces exactly one new operative quantity per construction — <code>t_drift</code> for folds, <code>t_recert</code> for singularities — and both are maintenance intervals, not field terms. Nothing in §4.1–§4.3's mathematics is superseded. A Legend is, mechanically, a Sovereign whose institution has learned to keep re-solving the same equation before drift ever crosses the threshold that would make it fail.</p></div></section>
<section class="book" id="techniques-ascension"><header class="book-head"><span class="book-tag">§4.11</span><h1>The Ascent Beyond Legend</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. The four Ascent paths themselves — Tetrarch, Demiurge, Cosmographer, Communion — are defined in §3.3, <code>codex/power-hierarchy.md</code>. This section formalizes how "closeness" to each is measured and audited, per §3.4's own observation that closeness is measured in solved sub-terms and is auditable in principle.</em></p>
<hr>
<h3>4.11 The Ascent Beyond Legend — Applied Fragments</h3>
<p>§3.3 names four directions and proves, via §3.4, that none of them terminates. That is not the end of the mathematics — it is the reason the mathematics matters more here than anywhere else in the Codex. A path that cannot be finished still admits a <em>rate</em>, and a caster's claim to be walking one is worthless unless it can be checked against solved lower-tier machinery rather than taken on their word. The four fragments below do exactly that: each takes a target already named in §3.3 and reduces "how close" to a number built only from terms a lower tier has already proven. None of the four closes the distance. All four make the distance auditable.</p>
<p><strong>Eq. 4.24 — Tetrarch Coherence Fraction</strong></p>
<pre><code>Coh_tetrarch = average of Chi(f1,f2) over all 6 unordered pairs of {EM, weak, strong, gravity}
Coh_tetrarch -&gt; 1 as k_unified is approached (never reached)
</code></pre>
<p><code>Chi(f1,f2)</code> is Adept tier's solved cross-coupling function (Eq. 4.14) — one per force-pair, six unordered pairs total among {EM, weak, strong, gravity}. A caster pursuing the Tetrarch Path can, in principle, solve all six pairwise couplings individually, driving <code>Coh_tetrarch</code> toward 1 through work that is itself entirely ordinary Adept-tier mathematics, just exhaustively completed. But <code>Coh_tetrarch = 1</code> is necessary, not sufficient: full pairwise coherence describes six forces that agree with each other everywhere they've been made to meet, not the single coupling <code>k_unified</code> that would make them one term instead of six agreeing ones. No closed form for <code>k_unified</code> is known even in principle, so a caster standing at <code>Coh_tetrarch</code> arbitrarily close to 1 has proven something real and formidable — and is not thereby one proof closer to the unification itself, only to the best possible imitation of its surface behavior.</p>
<p><strong>Eq. 4.25 — Demiurge Bounded Generative Family</strong></p>
<pre><code>Gen_partial(dM) = { predicted e_new : e_new derived from S by a proven extrapolation rule r }
N_family = |Gen_partial(dM)|
</code></pre>
<p><code>S</code> is Artisan/Master's solved eigenvector subset of <code>M_op</code> (Eq. 3.1e). A Demiurge aspirant who cannot derive <code>Gen(dM)</code> — the generating structure for <em>any</em> stable matter configuration — can still prove a narrower rule <code>r</code>: not "any alloy," but "every alloy along this one proven mixing ratio," extrapolated outward from <code>S</code> rather than catalogued point by point. <code>N_family</code>, the count of predictions from <code>r</code> that have been individually derived and verified, is the auditable metric: it can grow without bound within its bounded family, and a large <code>N_family</code> is a genuine, checkable accomplishment. It says nothing about any configuration outside the family <code>r</code> was proven for. A Demiurge with <code>N_family</code> in the thousands for one alloy-rule is not a fraction of the way to <code>Gen(dM)</code>; they are the complete master of one proven rule among an unknown, possibly unbounded, number of others.</p>
<p><strong>Eq. 4.26 — Cosmographer Domain Ratio</strong></p>
<pre><code>rho_cosmo = R_dom_achieved / R_dom_legend_typical      (analogously definable for t_dom)
</code></pre>
<p><code>R_dom</code> and <code>t_dom</code> are the same dials Sovereign and Legend already turn (Eq. 3.1g). <code>rho_cosmo</code> simply asks how many "typical Legend domains" a caster's own closed-form <code>Xi(Ae, g)</code> currently spans, giving a Cosmographer aspirant a number instead of a boast. Per §1.4, this ratio never reaches infinity — that would require <code>Xi(Ae, g)</code> to escape the finite-<code>dM</code> dependence §3.4 forbids for any term of the Grand Equation. What makes <code>rho_cosmo</code> a cruel metric rather than a merely difficult one is that its increments are not evenly priced: because the metric-sector propagator is reshaped by every prior increment solved, moving <code>rho_cosmo</code> from 4 to 5 costs strictly more proof than moving it from 1 to 2 did. A Cosmographer's progress curve bends the wrong way for comfort — real, and increasingly expensive to keep buying.</p>
<p><strong>Eq. 4.27 — Communion Pooled Boundary Ratio</strong></p>
<pre><code>N_comm = | dM_total | / | dM_legend_typical |
</code></pre>
<p><code>dM_total</code> is the union of comprehension domains already named in §3.3's account of the Communion Path. <code>N_comm</code> expresses that union in units of "one typical Legend's worth of proven comprehension," and it is the one fragment in this section that can exceed 1: a large enough Communion of Novices and Sovereigns can out-mass a single Legend's <code>dM</code> in raw quantity, well before any of them approaches Legend's <em>quality</em> of comprehension individually. This is precisely the distinction §3.3 draws when it observes that a Communion of a thousand Novices is a very large Novice, not a Legend — <code>N_comm</code> measures the size of the pool, never the depth any one proof inside it reaches. <code>dM_total</code> remains strictly bounded by the union of what its members actually, individually proved; it is a ledger of pooled work, never a shortcut to comprehension none of them solved.</p>
<p>Each of these four fractions is a career's honest measure, not a formality. A caster who drives <code>Coh_tetrarch</code>, <code>N_family</code> (relative to a family worth pursuing), <code>rho_cosmo</code>, or <code>N_comm</code> asymptotically toward its respective limit has done something no ordinary Legend does — spent a lifetime, or organized many lifetimes, against a target the mathematics itself guarantees they cannot reach. No figure in this setting's recorded history has done so for more than one of the four paths at once; the four fragments do not share proof, and progress on one buys nothing on another.</p></div></section>
<section class="book" id="spell-directory"><header class="book-head"><span class="book-tag">§4.4</span><h1>The Spell Directory</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. The base equations these entries draw on are housed across the technique files: Eq. 4.0a–4.0c, 4.0e in <code>codex/techniques-novice.md</code>; Eq. 4.13 in <code>codex/techniques-journeyman.md</code>; Eq. 4.14–4.15 in <code>codex/techniques-adept.md</code>; Eq. 4.16–4.17 in <code>codex/techniques-artisan.md</code>; Eq. 4.18–4.19 in <code>codex/techniques-master.md</code>; Eq. 4.20–4.21 in <code>codex/techniques-warden.md</code>; Eq. 4.22–4.23 in <code>codex/techniques-legend.md</code>; Eq. 4.24–4.27 in <code>codex/techniques-ascension.md</code>.</em></p>
<hr>
<h3>4.4 The Spell Directory</h3>
<p>§4.0's worked examples (EM, gravity, strong, plus the passive EM read of Eq. 4.0e) were chosen to teach the pattern, not to be exhaustive. This section catalogs named techniques across the Power Hierarchy (§3.3), Novice through the Ascent Beyond Legend — every rank except Sovereign, whose two canonical workings are written up in full in <code>codex/techniques-sovereign.md</code> (§4.1–§4.3) rather than catalogued here — as a reference a novel can pull named techniques from without re-deriving mechanics each time. Entries use directory codes (<code>N-</code>, <code>J-</code>, <code>AD-</code>, <code>AR-</code>, <code>M-</code>, <code>W-</code>, <code>LG-</code>, <code>AS-</code>) rather than Equation Index numbers; they draw on the equations already indexed in §6 and don't need separate global numbering to stay traceable. Adding more later only requires following the pattern already set for that tier.</p>
<p>Read through §1.3, this directory is a map of which channel, or channel-pair, each entry routes through, and nothing more exotic than that. Every Novice and Journeyman entry is a single <code>delta(F_f)</code> distortion, or two used in sequence — the sole exception being N-EM-05, a passive read on the <code>k_EM</code> channel that sources no distortion at all (Eq. 4.0e); every Adept entry is a single ripple coupling into two gauge channels at once through the joint function <code>Chi(f1, f2)</code>, formally defined in Eq. 4.14, which is why Adept techniques are the first in this directory whose fidelity requirement is squared rather than linear — a single sourced ripple has to stay coherent enough to satisfy two coupling channels simultaneously, not one after the other, and a wobble a Journeyman's sequential switching would simply absorb as one weak casting instead degrades both halves of an Adept's blend at once. Every Artisan entry is a <code>delta(M_op)</code> distortion restricted to whatever eigenvector that Artisan's signature material actually falls under (Eq. 3.1e, Eq. 4.16) — narrow by construction, for exactly the reason §3.3 already gives. Master entries route through the same <code>delta(M_op)</code> channel with a complete <code>S</code> behind them (Eq. 4.18–4.19). Warden and Legend entries route through <code>delta(g)</code>, narrow and perturbative for the former (Eq. 4.20), the same closed-form Overlay/Singularity mathematics held across a vastly larger domain for the latter (Eq. 4.22–4.23). Ascension entries are historical fragments toward the four paths of §3.3, quantified by Eq. 4.24–4.27.</p>
<p><strong>Eq. 4.0d — Decay Nudge ("Coaxing a Glow")</strong> <em>(completing the four-force set begun in §4.0)</em></p>
<pre><code>Gamma_eff = Gamma_0 * (1 + k_weak * Fid)
P_out = Gamma_eff * E_per_decay * N_unstable
</code></pre>
<p>The caster nudges the decay rate of trace unstable material already present in most ordinary matter, very slightly upward, for the duration of the casting. <code>P_out</code> is the resulting radiant power: each decay of the <code>N_unstable</code> unstable nuclei present releases an energy <code>E_per_decay</code>, so the nudged rate <code>Gamma_eff</code> sets the output directly. <code>k_weak</code> is, true to its real-world namesake, the smallest of the four couplings by a wide margin — so even a flawless Novice casting of this equation produces only a faint warmth or the barest visible glow. This is the standard explanation given for why weak-force casters are rare and easy to underestimate at Novice tier: the force is not weak in principle, only in this one narrow, unblended expression of it. It reads very differently once an Adept learns to couple it to something else (Adept tier, below).</p>
<h4>Novice (Common)</h4>
<p><em>Electromagnetic (<code>k_EM</code>)</em> — extends Eq. 4.0a.</p>
<p><strong>[N-EM-01] Spark Draw</strong></p>
<pre><code>V_out = k_EM * Fid * Ae_local
</code></pre>
<p>A small, controlled static discharge (<code>V_out</code>, the discharge potential produced) between the caster's fingers and a target — enough to light kindling, startle, or send a visible signal at range. The first technique most students cast that isn't Eq. 4.0a itself.</p>
<p><strong>[N-EM-02] Cold Ember</strong></p>
<pre><code>P_in = -k_EM * Fid * Ae_local^2
</code></pre>
<p>Eq. 4.0a run in reverse: heat is drawn out rather than pushed in. Used for chilling drinks, slowing spoilage over a single evening, or cooling a wagon axle that's started to seize — nothing that would count as preservation at any real timescale.</p>
<p><strong>[N-EM-03] Lumen Thread</strong></p>
<pre><code>L_out = k_EM * Fid * Ae_local(t)   -- held steady rather than discharged
</code></pre>
<p>A sustained, low, flameless glow (<code>L_out</code>, the luminous output) along a treated wick or thread rather than a single discharge. The caster's main skill here is holding <code>Ae_local</code> constant over time instead of releasing it all at once — an early, gentle introduction to sustained casting.</p>
<p><strong>[N-EM-04] Static Ward</strong>
A faint, continuous repulsive charge held at the skin or on clothing — deflects dust, light debris, and insects. Popular with travelers, archivists, and anyone else who spends their day around things they'd rather not carry home.</p>
<p><strong>[N-EM-05] Ripple Sense</strong> — Eq. 4.0e.</p>
<pre><code>S_detect(x, t) = k_EM * dAe_nearby(x, t)
</code></pre>
<p>A passive, continuous read on the same <code>k_EM</code> channel every other EM technique here actively sources into — the caster notices a nearby working before an ordinary bystander would feel its heat, light, or static. Costs nothing and carries no fizzle or backlash risk (Eq. 4.0e), since nothing is ever sourced; the limitation is purely informational, not mechanical.</p>
<p><em>Gravity (<code>k_grav</code>)</em> — extends Eq. 4.0b.</p>
<p><strong>[N-GR-01] Feather Fall</strong></p>
<pre><code>F_net = m_obj * g_local * (1 - k_grav * Fid),  Fid &lt; 1 by design
</code></pre>
<p>The same equation as Eq. 4.0b, deliberately undershot — a controlled slow descent rather than full cancellation. Taught before full levitation precisely because undershooting on purpose is safer to practice than aiming for zero and occasionally overshooting into a shove.</p>
<p><strong>[N-GR-02] Anchor Step</strong></p>
<pre><code>F_net = m_obj * g_local * (1 + k_grav * Fid)
</code></pre>
<p>The inverse of Eq. 4.0b: a temporary increase in effective weight at the caster's own feet, for better footing on ice, a listing deck, or a narrow ledge in wind.</p>
<p><strong>[N-GR-03] Light Load</strong>
Eq. 4.0b applied to a carried object rather than the caster — a porter's or packer's trick, and one of the first Novice techniques to see routine commercial use rather than staying purely in a training hall.</p>
<p><em>Strong (<code>k_strong</code>)</em> — extends Eq. 4.0c.</p>
<p><strong>[N-ST-01] Seal Bind</strong></p>
<pre><code>E_bind_eff(x) = E_bind(x) * (1 + k_strong * Fid),  applied only at contact point x
</code></pre>
<p>Eq. 4.0c narrowed to a single point of contact between two surfaces — rope ends, a cracked seam, torn fibers held together — rather than a whole object's bulk cohesion. Fails safely: a dropped <code>Fid</code> just loosens the join rather than fusing it wrong.</p>
<p><strong>[N-ST-02] Brittle Ease</strong></p>
<pre><code>E_bind_eff(x) = E_bind(x) * (1 - k_strong * Fid)
</code></pre>
<p>The deliberate inverse of Eq. 4.0c — a small, precise weakening at one point, for a clean split rather than a ragged one. Common among fletchers, coopers, and quarry hands.</p>
<p><em>Weak (<code>k_weak</code>)</em> — extends Eq. 4.0d.</p>
<p><strong>[N-WK-01] Quick Ripen</strong>
Eq. 4.0d's decay nudge applied to already-ripening produce, nudging a process already underway forward by a day or two rather than starting one from nothing. An orchard-keeper's convenience, not a transformation.</p>
<p><strong>[N-WK-02] Faint Ward-Light</strong>
Eq. 4.0d held at the lowest sustainable output — a dim, steady, personal glow rather than a burst of warmth. The standard "still breathing" marker-light for anyone working somewhere that a torch would be a liability: mines, powder stores, night watches.</p>
<h4>Journeyman (Common)</h4>
<p>A Journeyman holds two or more of the above in closed form without a cross-term connecting them (§3.3) — every entry below is two Novice techniques held without blending: executed in clean sequence, or held as a live either/or choice between them (as in J-03). That distinction is the entire point of the tier, so it's called out explicitly in each write-up rather than left implied. Eq. 4.13 (<code>codex/techniques-journeyman.md</code>) formalizes exactly this pattern: disjoint activation windows separated by a switching cost, <code>tau_switch</code>. Note that <code>X_1</code> and <code>X_2</code> in Eq. 4.13 may also be two closed-form techniques drawn from a single <code>k_f</code> term (as in J-02 and J-06) — the tier's comprehension requirement is two or more solved terms on the caster's sheet, but the disjoint-window pattern applies to any pair of un-cross-coupled castings, same-force or not.</p>
<p><strong>[J-01] Ember Handoff</strong> — Eq. 4.0a, then N-GR-03. Heat a coal, then briefly lighten it to toss it accurately. Two separate, complete castings back to back, not one continuous effect.</p>
<p><strong>[J-02] Ward and Weld</strong> — N-ST-01, then N-ST-02, on different materials in the same working session. A cooper's or fletcher's routine: bind one seam, split one length, never both at once.</p>
<p><strong>[J-03] Lantern-Keeper's Round</strong> — N-EM-03 or N-WK-02, chosen by available margin rather than blended between. A night-watch specialty precisely because the choice, not a combination, is the skill being exercised.</p>
<p><strong>[J-04] Porter's Relief</strong> — N-GR-03 on a companion's litter, N-EM-02 on a wagon axle that's started to seize, applied in turn over the course of a journey rather than together.</p>
<p><strong>[J-05] Two-Handed Smith</strong> — Eq. 4.0a to heat the workpiece, then Eq. 4.0c to set the join, in strict alternation for as long as the work lasts. A guild-standard pairing precisely because an Adept's Flash-Forge (below) replaces it with one technique instead of two.</p>
<p><strong>[J-06] Watch-Fire Relay</strong> — Eq. 4.0a to relight a signal fire, N-EM-01 for a brief, bright flash where a full fire would be too slow. A chain of watchers relaying a message this way is switching, station to station, never combining.</p>
<p><strong>[J-07] Bladeline Feint</strong> — N-GR-01, then N-EM-01, drilled by duelists to the smallest <code>tau_switch</code> (Eq. 4.13) a Journeyman can sustain: lighten the step mid-lunge, then snap a startling spark at the guard the instant the lightening window closes. The tightness of the gap is the entire training regimen — and precisely how close it can get to zero without ever reaching it is the standing proof the duelist is still Journeyman, not Adept.</p>
<h4>Adept (Uncommon)</h4>
<p><strong>Eq. 4.15 — Adept Combined Output</strong> <em>(defined in §4.6, <code>codex/techniques-adept.md</code>, where the full derivation lives; restated here for the pattern below)</em></p>
<pre><code>X_combo = k_f1 * k_f2 * Fid^2 * Chi(f1, f2)
</code></pre>
<p><code>Chi(f1, f2)</code> (Eq. 4.14) is the cross-coupling function joining two <code>k_f</code> terms — the one piece Journeyman tier explicitly lacks (§3.3). Solving it once for a given pair is what promotes a caster from switching between two effects to blending them into a single technique. Fidelity enters squared rather than linearly because both halves of the blend must be held to standard at once; a combination technique punishes sloppy execution harder than either parent effect would alone. There are exactly six unordered pairs among the four forces, and each of the six below is the signature technique built on one of them.</p>
<div class="table-scroll"><table>
<thead>
<tr>
<th>Symbol</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Chi(f1, f2)</code></td>
<td>Solved cross-coupling function joining forces <code>f1</code> and <code>f2</code>; absent at Journeyman tier, present at Adept (Eq. 4.14)</td>
</tr>
</tbody>
</table></div>
<p><strong>[AD-01] Flash-Forge</strong> <em>(EM + Strong)</em> — heating and cohesion-boosting blended into one continuous pass rather than Two-Handed Smith's two separate steps (J-05). The signature technique of any smith who's made Adept, and usually the reason they're described that way rather than as "a very fast Journeyman."</p>
<p><strong>[AD-02] Storm-Step</strong> <em>(EM + Gravity)</em> — a static discharge and a lightened stance blended into a single short, controlled leap kicked off by the discharge itself. Popular with couriers and scouts for the same reason Ember Handoff (J-01) isn't: no visible gap between the spark and the motion.</p>
<p><strong>[AD-03] Cinder-Fall</strong> <em>(EM + Weak)</em> — heat injection blended with a decay nudge to produce a sustained, low, self-feeding flame from poor fuel — damp wood, old peat. Unglamorous and widely taught to Adept-tier quartermasters precisely because it's useful rather than impressive.</p>
<p><strong>[AD-04] Sunder Weight</strong> <em>(Gravity + Strong)</em> — the inverse of Light Load blended with Brittle Ease: an object made heavier and more fragile in the same casting. A demolition specialist's standard tool.</p>
<p><strong>[AD-05] Quiet Mend</strong> <em>(Strong + Weak)</em> — a cohesion boost blended with Eq. 4.0d run in reverse, slowing rather than hastening decay, to stabilize an already-aging bind — old rope, brittle leather — rather than merely strengthening a fresh one. A preservationist's or archivist's technique, and one of the few Adept combinations built around slowing something down.</p>
<p><strong>[AD-06] Grave Lantern</strong> <em>(Gravity + Weak)</em> — Light Load blended with Faint Ward-Light so a marked object hovers just barely off true rest while glowing faintly. Ceremonial rather than practical; several regional death-rites use a version of this over a grave-marker or a burial buoy.</p>
<p>All six unordered force-pairs are exhausted by AD-01 through AD-06 above — there is no seventh pair among four forces. An Adept's remaining growth from here is depth (<code>Fid</code>, practice) on the pairs they hold, solving any of the six they do not yet hold (§4.6 — tier is a per-pair predicate), or reaching for a different channel entirely (Artisan's <code>delta(M_op)</code>); what it is never is a brand-new combination beyond the six.</p>
<h4>Artisan (Uncommon)</h4>
<p>Each entry names the specific material an Artisan has solved — the finite subset <code>S</code> in Eq. 3.1e — and the narrow, precise work that subset allows. Reaching for a different material with the same confidence is Master-tier work attempted without Master-tier comprehension (§3.3), and fails accordingly. Eq. 4.16 (<code>codex/techniques-artisan.md</code>) gives every entry below a shared formal backbone; Eq. 4.17 formalizes the backlash risk of reaching for a material outside <code>S</code>.</p>
<p><strong>[AR-01] Artisan of Salt</strong> — the solved eigenvector governs salt's crystal lattice: precise purification, preservation, or selective dissolution and reformation of salt-based compounds. Does not extend to sugar or quartz, whatever their surface similarity.</p>
<p><strong>[AR-02] Artisan of Iron</strong> — a solved eigenvector for iron's lattice lets a warped blade be trued or its temper shifted without a forge. Bronze and silver are unmodeled and are not touched.</p>
<p><strong>[AR-03] Artisan of Bone</strong> — a solved eigenvector for bone's mineral structure, used by menders and, less happily, morticians, to realign or preserve it precisely. One of the more common Artisan specialties in settlements without ready access to a trained surgeon — and, per §3.3, exactly as narrow as every other entry here.</p>
<p><strong>[AR-04] Artisan of Rot</strong> — not a strengthening eigenvector but a specific, solved decay pathway in organic matter: controlled composting, curing, tanning. A closely guarded trade secret among tanners and vintners rather than a battlefield technique.</p>
<p><strong>[AR-05] Artisan of Glass</strong> — a solved eigenvector for silica's amorphous structure allows cold reshaping without a furnace. Prized by lens-makers and glaziers, and nearly useless for anything crystalline, since glass's structure is specifically the thing that's been solved.</p>
<p><strong>[AR-06] Artisan of Ash</strong> — rare, and largely ceremonial: a solved eigenvector for post-combustion residue lets a caster bind ash into a temporary, brittle shape. Associated almost exclusively with funerary sculpture in the few traditions that still practice it.</p>
<p><strong>[AR-07] Artisan of Clay</strong> — a solved eigenvector for clay's mineral lattice lets a caster drive precise, localized vitrification — true firing without a kiln — via Eq. 4.16, shaping and hardening a vessel wall by wall rather than all at once in a single heat-soak. Porcelain and stoneware bodies are close cousins but unmodeled, and firing them on the strength of clay's <code>lam_i</code> risks Eq. 4.17's off-basis backlash rather than a merely uneven glaze.</p>
<h4>Master (Rare)</h4>
<p>A Master's <code>S</code> is the complete eigenbasis of <code>M_op</code> (Eq. 4.18), so entries below are not tied to one signature material the way Artisan's are. Eq. 4.19 generalizes Eq. 4.0c's cohesion boost and Eq. 4.0d's decay nudge to any target once <code>c_M</code> is no longer restricted to a partial <code>S</code>.</p>
<p><strong>[M-01] Full Mend</strong> — Eq. 4.19's binding-energy term applied broadly across living tissue rather than to one bound seam: <code>E_bind_eff(x)</code> raised (Eq. 4.19 with <code>s = +1</code>) over an entire injury site at once. Where an Artisan of Bone can only realign what their one solved eigenvector covers, a Master's complete <code>S</code> lets the same boost reach muscle, vessel, and bone together in a single casting.</p>
<p><strong>[M-02] Grave Turn</strong> — Eq. 4.19 turned toward reinforcement (<code>s = -1</code> on <code>Gamma_eff</code> to arrest decay) or hastened aging (<code>s = +1</code>) of ordinary matter, rather than the dramatic identity swaps of Eq. 4.18 that Masters are best known for. A quarry-hand's or embalmer's use of the same complete eigenbasis that, wielded through <code>U_transmute</code> instead, changes lead to gold — proof the tier's machinery is general-purpose, not spectacle-only.</p>
<h4>Warden (Very Rare)</h4>
<p>Warden techniques are rarely catalogued at all — most Wardens' proofs are tied so tightly to one practitioner's own tested geometry (<code>R_proven</code>, Eq. 4.20) that they stay closely-guarded personal results rather than shared or generalized. One representative entry follows.</p>
<p><strong>[W-01] Threshold Ease</strong> — Applies Eq. 4.20 to a single, specific, previously-mapped threshold (a doorway or gate), briefly reducing the effective weight of crossing it; <code>R_proven</code> is that one threshold and no other, and the effect ends abruptly at its bounds. Pushing <code>eps</code> past <code>eps_valid(R_proven)</code> risks Eq. 4.21's backlash rather than a merely weaker effect.</p>
<h4>Legend (A Handful Across Recorded History)</h4>
<p>Legend entries reuse Sovereign's own mathematics (§4.1–§4.3) unchanged, held across a domain large enough in <code>R_dom</code>/<code>t_dom</code> to function as a standing, generational feature. See Eq. 4.22–4.23 (<code>codex/techniques-legend.md</code>).</p>
<p><strong>[LG-01] The Standing Fold</strong> — An inhabited, permanent Overlay linking two settlements, built on the unmodified Eq. 4.1 identification and held open across <code>t_dom_legend</code>. A hereditary order resurveys B's true conformal factor on a <code>t_drift</code> cadence (Eq. 4.22) so <code>mismatch(Om2)</code> never creeps <code>G_dec</code> toward collapse; the order's real craft is scheduling, not spellwork.</p>
<p><strong>[LG-02] The Held Star</strong> — A Bound Singularity (Eq. 4.12) maintained for generations as a regional landmark and power source rather than released. Its shell is periodically re-inscribed on a <code>t_recert</code> interval (Eq. 4.23) so the residual field <code>Curv_ext(r)</code> never rises above background and betrays an uncontained mass at range.</p>
<h4>Beyond Legend (Historical Fragments)</h4>
<p>No character in recorded history has completed a Tetrarch, Demiurge, Cosmographer, or Communion working (§3.3, §3.4) — but partial, documented attempts exist, and Eq. 4.24–4.27 (<code>codex/techniques-ascension.md</code>) give each one a checkable closeness metric. The two entries below are historical rather than teachable in the ordinary sense.</p>
<p><strong>[AS-01] The Four-Fold Feint</strong> — A historical Tetrarch aspirant's signature working, chaining all six solved <code>Chi(f1,f2)</code> pairs in tight, unbroken sequence so that EM, weak, strong, and gravitational expression seemed to flow as one force rather than four. Records treat it as proof <code>Coh_tetrarch</code> (Eq. 4.24) sat near 1 in the caster's hands — and, in the same breath, as proof that <code>k_unified</code> was never actually reached, since the technique still required four couplings performed seamlessly rather than one coupling performed at all.</p>
<p><strong>[AS-02] The Bound Chorus</strong> — A historical Communion working in which several practitioners pooled their individually-proven <code>dM_total</code> into a single acting boundary for one collective casting, reaching an effect no single member's comprehension could have supported alone. Surviving accounts treat it as both the clearest proof <code>N_comm</code> (Eq. 4.27) can exceed 1 and a cautionary tale, since what was merged was the provers themselves, not merely their proofs.</p></div></section>
<section class="book" id="glossary"><header class="book-head"><span class="book-tag">§5–§6</span><h1>Glossary &amp; Equation Index</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map. All § and Eq. numbers are global across the Codex. New equations continue the running numbering in §6.</em></p>
<hr>
<h2>5. Symbol &amp; Term Glossary</h2>
<div class="table-scroll"><table>
<thead>
<tr>
<th>Symbol</th>
<th>Definition</th>
<th>Defined in</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Ae</code></td>
<td>The aether field</td>
<td>Eq. 3.1</td>
</tr>
<tr>
<td><code>A_op</code></td>
<td>The reality-selection amplitude the Grand Equation evaluates</td>
<td>Eq. 3.1</td>
</tr>
<tr>
<td><code>Loop_dM[...]</code></td>
<td>Path-integral selection restricted to the caster's comprehension domain <code>dM</code></td>
<td>Eq. 3.1</td>
</tr>
<tr>
<td><code>Dpath(Ae)</code></td>
<td>Integration measure over aether field configurations</td>
<td>Eq. 3.1</td>
</tr>
<tr>
<td><code>hbar</code></td>
<td>Action quantum setting the phase scale of the path integral</td>
<td>Eq. 3.1, Eq. 4.4</td>
</tr>
<tr>
<td><code>k_f</code></td>
<td>Coupling constant, force <em>f</em> ∈ {EM, weak, strong, gravity}</td>
<td>Eq. 3.1c</td>
</tr>
<tr>
<td><code>F_f</code></td>
<td>Field-strength tensor for force <em>f</em></td>
<td>Eq. 3.1c</td>
</tr>
<tr>
<td><code>q</code>, <code>q_bar</code></td>
<td>Quark field and its Dirac conjugate</td>
<td>Eq. 3.1d</td>
</tr>
<tr>
<td><code>C_sel</code></td>
<td>Coupling-type selector (scalar/vector/tensor) — legacy symbol; no longer appears in any equation</td>
<td>Foundational draft; retained conceptually within <code>M_op</code> (Eq. 3.1d/3.1e)</td>
</tr>
<tr>
<td><code>M_op</code></td>
<td>Mass operator (matrix form) acting on the quark field</td>
<td>Eq. 3.1d</td>
</tr>
<tr>
<td><code>c_M</code></td>
<td>Matter-coupling constant analogous to <code>k_f</code>, folded into <code>M_op</code>'s own definition rather than tracked separately</td>
<td>Eq. 1.3, Eq. 3.1d</td>
</tr>
<tr>
<td><code>M_op_partial</code>, <code>S</code></td>
<td>An Artisan's partially diagonalized mass operator, and the finite eigenvector subset it's built from</td>
<td>Eq. 3.1e</td>
</tr>
<tr>
<td><code>lam_i</code>, <code>e_i</code></td>
<td>Eigenvalue/eigenvector pair of <code>M_op</code>; <code>lam_i</code> is solved exactly for <code>e_i</code> when <code>e_i in S</code></td>
<td>Eq. 3.1e / 4.16</td>
</tr>
<tr>
<td><code>lam_guess</code>, <code>lam_true</code></td>
<td>Assumed vs. actual eigenvalue when a caster targets a material eigenvector outside <code>S</code></td>
<td>Eq. 4.17</td>
</tr>
<tr>
<td><code>Effect_i</code></td>
<td>Magnitude of the quark-sector effect produced by drawing on eigenvector <code>e_i</code></td>
<td>Eq. 4.16</td>
</tr>
<tr>
<td><code>dAe_local</code></td>
<td>The sourced ripple concentrated at the working site — the same quantity as <code>Ae_local</code>, written in §1.1's perturbation notation</td>
<td>Eq. 4.16</td>
</tr>
<tr>
<td><code>E_back_mat</code></td>
<td>Backlash energy absorbed when a caster targets an eigenvector outside <code>S</code> — the quark-sector form of <code>E_back</code></td>
<td>Eq. 4.17</td>
</tr>
<tr>
<td><code>s</code></td>
<td>Direction parameter for Universal Binding &amp; Decay Control: <code>+1</code> to boost/hasten, <code>-1</code> to weaken/arrest</td>
<td>Eq. 4.19</td>
</tr>
<tr>
<td><code>U_transmute(M_op_full)</code></td>
<td>Unitary operator reassigning a quantity of matter's expression across the complete eigenbasis of <code>M_op</code></td>
<td>Eq. 4.18</td>
</tr>
<tr>
<td><code>Xi_pert</code>, <code>eps</code></td>
<td>A Warden's perturbative expansion of <code>Xi(Ae, g)</code>, and its departure-from-flat-space parameter</td>
<td>Eq. 3.1f</td>
</tr>
<tr>
<td><code>R_proven</code></td>
<td>A specific, previously-validated geometry to which a Warden confines an effect via <code>Bump(r, R_proven)</code></td>
<td>Eq. 4.20</td>
</tr>
<tr>
<td><code>eps_valid(R_proven)</code></td>
<td>The largest departure-from-flat-space <code>eps</code> that a given <code>R_proven</code> configuration has actually been demonstrated to tolerate</td>
<td>Eq. 4.21</td>
</tr>
<tr>
<td><code>E_back_pert</code></td>
<td>Backlash energy absorbed when <code>eps</code> is pushed past <code>eps_valid(R_proven)</code> — the perturbative-metric form of <code>E_back</code></td>
<td>Eq. 4.21</td>
</tr>
<tr>
<td><code>R_dom</code>, <code>t_dom</code></td>
<td>Spatial radius and duration over which a solved <code>Xi(Ae, g)</code> remains valid — small for Sovereign, effectively permanent for Legend</td>
<td>Eq. 3.1g</td>
</tr>
<tr>
<td><code>t_dom_legend</code></td>
<td>The <code>t_dom</code> value at Legend scale — a standing duration (years to a generation) rather than a Sovereign's bounded hold</td>
<td>Eq. 4.22 / 4.23 (scaling per Eq. 3.1g)</td>
</tr>
<tr>
<td><code>t_drift</code></td>
<td>Interval between re-validations of a destination's true conformal factor <code>Om2(x)</code> needed to keep <code>mismatch(Om2)</code> below <code>G_dec</code>'s safe threshold</td>
<td>Eq. 4.22</td>
</tr>
<tr>
<td><code>t_recert</code></td>
<td>Max interval between <code>Fid_shell</code> re-inscriptions such that residual leak <code>Curv_ext(r)</code> stays below the ambient noise floor across <code>t_dom_legend</code></td>
<td>Eq. 4.23</td>
</tr>
<tr>
<td><code>k_unified</code></td>
<td>Unsolved single coupling that would replace all four <code>k_f</code> terms at once (Tetrarch Path)</td>
<td>§3.3</td>
</tr>
<tr>
<td><code>Coh_tetrarch</code></td>
<td>Average of the six solved <code>Chi(f1,f2)</code> pairwise values; tends to 1 as <code>k_unified</code> is approached (never reached)</td>
<td>Eq. 4.24</td>
</tr>
<tr>
<td><code>Gen(dM)</code></td>
<td>Unsolved generating structure for <code>M_op</code>, predicting rather than cataloguing eigenvectors (Demiurge Path)</td>
<td>§3.3</td>
</tr>
<tr>
<td><code>Gen_partial(dM)</code>, <code>N_family</code></td>
<td>A proven, bounded extrapolation rule predicting new <code>M_op</code> eigenvectors from <code>S</code>, and the count of its verified predictions</td>
<td>Eq. 4.25</td>
</tr>
<tr>
<td><code>rho_cosmo</code>, <code>R_dom_legend_typical</code></td>
<td>Ratio of a caster's achieved domain to a typical Legend's domain, and the reference domain size it's measured against (Cosmographer Path)</td>
<td>Eq. 4.26</td>
</tr>
<tr>
<td><code>dM_total</code></td>
<td>Union of several casters' individually-proven comprehension domains (Communion Path)</td>
<td>§3.3</td>
</tr>
<tr>
<td><code>N_comm</code>, <code>dM_legend_typical</code></td>
<td>Ratio of a Communion's pooled <code>dM_total</code> to a typical Legend's <code>dM</code>, and that reference quantity</td>
<td>Eq. 4.27</td>
</tr>
<tr>
<td><code>Xi(Ae, g)</code></td>
<td>Aether–spacetime coupling term</td>
<td>Eq. 3.1b</td>
</tr>
<tr>
<td><code>g</code></td>
<td>Spacetime metric</td>
<td>Eq. 3.1a, Eq. 4.1</td>
</tr>
<tr>
<td><code>dM</code></td>
<td>Boundary of the caster's comprehension domain</td>
<td>Eq. 3.1</td>
</tr>
<tr>
<td><code>X_ideal</code>, <code>X_eff</code></td>
<td>Theoretical output of a fully solved term, and the effective output actually produced — <code>X_ideal</code> scaled by <code>Fid</code></td>
<td>Eq. 3.2</td>
</tr>
<tr>
<td><code>Fid</code></td>
<td>Fidelity coefficient — overlap between ideal and actual invocation</td>
<td>Eq. 3.2</td>
</tr>
<tr>
<td><code>phi_ideal</code>, <code>phi_actual</code></td>
<td>Ideal formal structure of a term vs. the caster's real-time invocation of it</td>
<td>Eq. 3.2</td>
</tr>
<tr>
<td><code>t_ins</code></td>
<td>Time invested in inscribing/invoking a term</td>
<td>Eq. 3.2</td>
</tr>
<tr>
<td><code>Fid_min</code></td>
<td>Minimum fidelity below which an invocation fails to manifest</td>
<td>Eq. 3.3</td>
</tr>
<tr>
<td><code>prac(x)</code></td>
<td>Practice depth for a specific term <code>x</code></td>
<td>Eq. 3.4</td>
</tr>
<tr>
<td><code>prac_min</code></td>
<td>Mastery threshold required for unassisted invocation</td>
<td>Eq. 3.4</td>
</tr>
<tr>
<td><code>anchor</code></td>
<td>1 if a physical medium is used, 0 for pure mental visualization</td>
<td>Eq. 3.4</td>
</tr>
<tr>
<td><code>Step(...)</code></td>
<td>Heaviside step function</td>
<td>Eq. 3.4</td>
</tr>
<tr>
<td><code>Sim[...]</code></td>
<td>Prefix operator: evaluates an invocation's readout without committing it to reality</td>
<td>Eq. 3.5</td>
</tr>
<tr>
<td><code>X_eff_proj</code></td>
<td>Projected effective output under <code>Sim[...]</code> — identical math to <code>X_eff</code>, never released</td>
<td>Eq. 3.5</td>
</tr>
<tr>
<td><code>E_back_proj</code></td>
<td>Projected backlash energy under <code>Sim[...]</code> — identical math to <code>E_back</code>, never released</td>
<td>Eq. 3.5</td>
</tr>
<tr>
<td><code>U_op(A, B)</code></td>
<td>Unitary identification operator between two points</td>
<td>Eq. 4.1</td>
</tr>
<tr>
<td><code>Om2(x)</code></td>
<td>Conformal scale factor reconciling two locations' metrics</td>
<td>Eq. 4.1</td>
</tr>
<tr>
<td><code>T_ae</code>, <code>T_mat</code></td>
<td>Stress-energy tensors, aether field vs. physical matter</td>
<td>Eq. 4.2</td>
</tr>
<tr>
<td><code>a(t)</code>, <code>b(t)</code></td>
<td>Amplitudes: "still at A" / "arrived at B"</td>
<td>Eq. 4.3</td>
</tr>
<tr>
<td><code>t_rel</code></td>
<td>Elapsed hold time at the moment the caster releases the fold — the counterpart to <code>t_ins</code></td>
<td>Eq. 4.5</td>
</tr>
<tr>
<td><code>G_dec</code></td>
<td>Decoherence rate governing collapse safety</td>
<td>Eq. 4.6</td>
</tr>
<tr>
<td><code>eta</code></td>
<td>Proportionality constant setting how strongly conformal mismatch drives decoherence</td>
<td>Eq. 4.6</td>
</tr>
<tr>
<td><code>K(x)</code></td>
<td>Knowledge coefficient for a given location</td>
<td>Eq. 4.6</td>
</tr>
<tr>
<td><code>s_int</code></td>
<td>External interference term</td>
<td>Eq. 4.6</td>
</tr>
<tr>
<td><code>E_back</code></td>
<td>Curvature-stress energy absorbed on failed collapse</td>
<td>Eq. 4.7</td>
</tr>
<tr>
<td><code>Curv(g)</code></td>
<td>Curvature built from the metric (Einstein-tensor analogue)</td>
<td>Eq. 4.8</td>
</tr>
<tr>
<td><code>Bump(r, R)</code></td>
<td>Smooth localization function, ~1 inside radius R, ~0 outside</td>
<td>Eq. 4.8</td>
</tr>
<tr>
<td><code>R_core</code></td>
<td>Radius of the well's core (true singularity/horizon region)</td>
<td>Eq. 4.8</td>
</tr>
<tr>
<td><code>Shell(r, R1, R2)</code></td>
<td>Smooth annular support function, nonzero only between R1 and R2</td>
<td>Eq. 4.9</td>
</tr>
<tr>
<td><code>R_shell</code></td>
<td>Outer containment radius — the intended edge of the well's influence</td>
<td>Eq. 4.9</td>
</tr>
<tr>
<td><code>k_newton</code></td>
<td>Fixed background constant governing how strongly mass-energy curves spacetime (a Newton's-constant analogue) — distinct from the solvable gauge coupling <code>k_grav</code> (Eq. 3.1c); no caster solves or scales it</td>
<td>Eq. 4.10</td>
</tr>
<tr>
<td><code>M_ae(r)</code></td>
<td>Enclosed aether-mass-equivalent within radius r</td>
<td>Eq. 4.10</td>
</tr>
<tr>
<td><code>lapse(r)</code></td>
<td>Proper-time rate at radius r relative to the exterior</td>
<td>Eq. 4.10</td>
</tr>
<tr>
<td><code>Fid_shell</code></td>
<td>Fidelity coefficient specific to the counter-curvature shell (Eq. 4.9)</td>
<td>Eq. 4.11</td>
</tr>
<tr>
<td><code>Curv_ext(r)</code></td>
<td>Residual external curvature from an imperfectly contained well</td>
<td>Eq. 4.11</td>
</tr>
<tr>
<td><code>Ae_local</code></td>
<td>Locally concentrated aether density at a point of contact</td>
<td>Eq. 4.0a</td>
</tr>
<tr>
<td><code>P_in</code></td>
<td>Power injected into a target substance</td>
<td>Eq. 4.0a</td>
</tr>
<tr>
<td><code>m_obj</code>, <code>g_local</code></td>
<td>Mass of the object being lifted, and the local gravitational acceleration acting on it</td>
<td>Eq. 4.0b</td>
</tr>
<tr>
<td><code>F_net</code></td>
<td>Net downward force remaining after partial gravitational cancellation</td>
<td>Eq. 4.0b</td>
</tr>
<tr>
<td><code>E_bind</code>, <code>E_bind_eff</code></td>
<td>A material's ordinary binding energy, and its temporarily boosted value</td>
<td>Eq. 4.0c</td>
</tr>
<tr>
<td><code>Gamma_0</code>, <code>Gamma_eff</code></td>
<td>Baseline and weak-force-nudged decay rate of trace unstable material</td>
<td>Eq. 4.0d</td>
</tr>
<tr>
<td><code>P_out</code>, <code>E_per_decay</code>, <code>N_unstable</code></td>
<td>Radiant power produced by a nudged decay rate; energy released per decay event; count of unstable nuclei present</td>
<td>Eq. 4.0d</td>
</tr>
<tr>
<td><code>S_detect</code>, <code>dAe_nearby</code></td>
<td>Passive detection readout and the nearby ripple it reads, using the <code>k_EM</code> channel in reverse</td>
<td>Eq. 4.0e</td>
</tr>
<tr>
<td><code>Win_1(t)</code>, <code>Win_2(t)</code></td>
<td>Activation-window indicator functions (1 while a given solved <code>k_f</code> term is actively producing output, 0 otherwise); mutually exclusive at Journeyman tier since no <code>Chi(f1,f2)</code> exists to let one ripple satisfy both channels of Eq. 1.3 at once</td>
<td>Eq. 4.13</td>
</tr>
<tr>
<td><code>tau_switch</code></td>
<td>Dead time between two sequential Journeyman castings, spent re-inscribing or re-visualizing (§3.6); shrinks with drilled practice but cannot structurally reach zero without <code>Chi</code></td>
<td>Eq. 4.13</td>
</tr>
<tr>
<td><code>Chi(f1, f2)</code></td>
<td>Solved cross-coupling function joining two forces; absent at Journeyman tier, present at Adept</td>
<td>Eq. 4.14</td>
</tr>
</tbody>
</table></div>
<p><em>Symbols governing how a caster's invocation reaches the Grand Equation's terms — <code>Ae_0</code>, <code>dAe</code>, <code>J_cast</code>, <code>G(x, x'; t, t'; g)</code> — are defined in §1.1–§1.4 (<code>codex/foundations.md</code>).</em></p>
<hr>
<h2>6. Equation Index</h2>
<div class="table-scroll"><table>
<thead>
<tr>
<th>Eq.</th>
<th>Name</th>
<th>Section</th>
<th>Tier</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>3.1</td>
<td>Grand Unified Aether Equation</td>
<td>§3.1</td>
<td>Foundational</td>
<td>Master path-integral governing all aether effects</td>
</tr>
<tr>
<td>3.1a</td>
<td>Aether Action</td>
<td>§3.1</td>
<td>Foundational</td>
<td>The action functional integrated inside the path integral</td>
</tr>
<tr>
<td>3.1b</td>
<td>Total Lagrangian Density</td>
<td>§3.1</td>
<td>Foundational</td>
<td>Sum of the gauge, quark, and aether-geometry contributions</td>
</tr>
<tr>
<td>3.1c</td>
<td>Gauge Term</td>
<td>§3.1</td>
<td>Foundational</td>
<td>The four fundamental forces' contribution to the density</td>
</tr>
<tr>
<td>3.1d</td>
<td>Quark Term</td>
<td>§3.1</td>
<td>Foundational</td>
<td>Matter's contribution to the density</td>
</tr>
<tr>
<td>3.1e</td>
<td>Partial Diagonalization</td>
<td>§3.3</td>
<td>Artisan</td>
<td>A finite, proven subset of <code>M_op</code>'s eigenvectors</td>
</tr>
<tr>
<td>3.1f</td>
<td>Perturbative Aether-Geometry Coupling</td>
<td>§3.3</td>
<td>Warden</td>
<td>Leading-order expansion of <code>Xi(Ae, g)</code> around flat space</td>
</tr>
<tr>
<td>3.1g</td>
<td>Domain Persistence</td>
<td>§3.3</td>
<td>Sovereign/Legend</td>
<td>Spatial and temporal reach of a solved <code>Xi(Ae, g)</code></td>
</tr>
<tr>
<td>3.2</td>
<td>Fidelity-Weighted Output</td>
<td>§3.5</td>
<td>Foundational</td>
<td>Scales any term's effective output by execution precision</td>
</tr>
<tr>
<td>3.3</td>
<td>Minimum Resolution Threshold</td>
<td>§3.5</td>
<td>Foundational</td>
<td>Below-threshold invocations fail quietly rather than backlashing</td>
</tr>
<tr>
<td>3.4</td>
<td>Unassisted Fidelity Ceiling</td>
<td>§3.6</td>
<td>Foundational</td>
<td>Governs casting a solved term with no physical medium</td>
</tr>
<tr>
<td>3.5</td>
<td>Simulated Invocation</td>
<td>§3.7</td>
<td>Foundational</td>
<td>Evaluates an invocation's readout without committing it to reality</td>
</tr>
<tr>
<td>4.0a</td>
<td>Thermal Excitation</td>
<td>§4.0</td>
<td>Novice</td>
<td>Injects power into a substance via EM coupling ("boiling water")</td>
</tr>
<tr>
<td>4.0b</td>
<td>Minor Levitation</td>
<td>§4.0</td>
<td>Novice</td>
<td>Partially cancels local weight via gravitational coupling</td>
</tr>
<tr>
<td>4.0c</td>
<td>Minor Cohesion Boost</td>
<td>§4.0</td>
<td>Novice</td>
<td>Temporarily boosts a material's binding energy</td>
</tr>
<tr>
<td>4.0d</td>
<td>Decay Nudge</td>
<td>§4.4</td>
<td>Novice</td>
<td>Slightly accelerates weak-force decay in trace unstable material</td>
</tr>
<tr>
<td>4.0e</td>
<td>Ripple Sense</td>
<td>§4.0</td>
<td>Novice</td>
<td>Passive detection use of the <code>k_EM</code> channel; a read rather than a source</td>
</tr>
<tr>
<td>4.1</td>
<td>Overlay Identification</td>
<td>§4.1</td>
<td>Sovereign/Legend</td>
<td>Establishes conformal identification between two coordinates</td>
</tr>
<tr>
<td>4.2</td>
<td>Null-Displacement Constraint</td>
<td>§4.1</td>
<td>Sovereign/Legend</td>
<td>Guarantees the Overlay Fold is mass-neutral</td>
</tr>
<tr>
<td>4.3</td>
<td>Superposed State Vector</td>
<td>§4.2</td>
<td>Sovereign/Legend</td>
<td>Describes the caster's state while a fold is held open</td>
</tr>
<tr>
<td>4.4</td>
<td>Fold Evolution</td>
<td>§4.2</td>
<td>Sovereign/Legend</td>
<td>Governs how holding the fold shifts probability from A to B</td>
</tr>
<tr>
<td>4.5</td>
<td>Resolution Functional</td>
<td>§4.2</td>
<td>Sovereign/Legend</td>
<td>Probability of clean arrival at release</td>
</tr>
<tr>
<td>4.6</td>
<td>Decoherence Rate</td>
<td>§4.2</td>
<td>Sovereign/Legend</td>
<td>Determines collapse safety from knowledge and interference</td>
</tr>
<tr>
<td>4.7</td>
<td>Backlash Energy</td>
<td>§4.2</td>
<td>Sovereign/Legend</td>
<td>Curvature stress absorbed by the caster on failed collapse</td>
</tr>
<tr>
<td>4.8</td>
<td>Localized Well Source</td>
<td>§4.3</td>
<td>Sovereign/Legend</td>
<td>Sources real curvature from aether alone, within a core radius</td>
</tr>
<tr>
<td>4.9</td>
<td>Counter-Curvature Shell</td>
<td>§4.3</td>
<td>Sovereign/Legend</td>
<td>Anti-gravity annulus that cancels the well's exterior field</td>
</tr>
<tr>
<td>4.10</td>
<td>Containment Lapse &amp; Horizon Tuning</td>
<td>§4.3</td>
<td>Sovereign/Legend</td>
<td>Engineers a genuine, causally sealing horizon at the shell boundary</td>
</tr>
<tr>
<td>4.11</td>
<td>Residual Outreach</td>
<td>§4.3</td>
<td>Sovereign/Legend</td>
<td>Leaked field from imperfect shell fidelity, as a higher multipole</td>
</tr>
<tr>
<td>4.12</td>
<td>Unified Bound Singularity Form</td>
<td>§4.3</td>
<td>Sovereign/Legend</td>
<td>Condenses Eq. 4.8, 4.9, and 4.11 into one piecewise definition</td>
</tr>
<tr>
<td>4.13</td>
<td>Sequential Invocation Overhead</td>
<td>§4.5</td>
<td>Journeyman</td>
<td>Formalizes the disjoint activation windows and switching cost (<code>tau_switch</code>) between two un-cross-coupled <code>k_f</code> terms</td>
</tr>
<tr>
<td>4.14</td>
<td>Cross-Coupling Function</td>
<td>§4.6</td>
<td>Adept</td>
<td>Formal overlap measure defining <code>Chi(f1,f2)</code>; <code>Chi = 0</code> is exactly the Journeyman condition</td>
</tr>
<tr>
<td>4.15</td>
<td>Adept Combined Output</td>
<td>§4.6</td>
<td>Adept</td>
<td>Promotes the Spell Directory's informal Adept Combination Pattern to the numbered index; <code>Fid</code> enters squared because <code>Chi</code> measures one ripple against two channels at once</td>
</tr>
<tr>
<td>4.16</td>
<td>Eigenvector Draw</td>
<td>§4.7</td>
<td>Artisan</td>
<td>Quark-sector analogue of Eq. 4.0a; the shared formal backbone behind AR-01–AR-07</td>
</tr>
<tr>
<td>4.17</td>
<td>Off-Basis Extrapolation</td>
<td>§4.7</td>
<td>Artisan</td>
<td>Quark-sector analogue of Eq. 4.7's backlash integral; confirms §1.3's claim that the backlash mechanism is universal</td>
</tr>
<tr>
<td>4.18</td>
<td>Full Transmutation</td>
<td>§4.8</td>
<td>Master</td>
<td>Rewrites a quantity of matter's identity via a unitary operator over the complete <code>M_op</code> eigenbasis</td>
</tr>
<tr>
<td>4.19</td>
<td>Universal Binding &amp; Decay Control</td>
<td>§4.8</td>
<td>Master</td>
<td>Generalizes Eq. 4.0c/4.0d's single-material boost/nudge to any material, once <code>c_M</code> is unrestricted by a partial <code>S</code></td>
</tr>
<tr>
<td>4.20</td>
<td>Perturbative Curvature Whisper</td>
<td>§4.9</td>
<td>Warden</td>
<td>Confines a solved <code>eps*Xi_1</code> term to a validated neighborhood <code>R_proven</code>; the entire practical range of Warden-tier metric effects</td>
</tr>
<tr>
<td>4.21</td>
<td>Perturbative Extrapolation Backlash</td>
<td>§4.9</td>
<td>Warden</td>
<td>Backlash from pushing <code>eps</code> past <code>eps_valid(R_proven)</code> — the same universal mechanism as Eq. 4.7 and Eq. 4.17</td>
</tr>
<tr>
<td>4.22</td>
<td>Standing Fold Persistence</td>
<td>§4.10</td>
<td>Legend</td>
<td>Reuses Eq. 4.1 unchanged under Eq. 3.1g's scaling; introduces <code>t_drift</code> as the operative Legend-tier constraint</td>
</tr>
<tr>
<td>4.23</td>
<td>Standing Singularity &amp; Recertification Interval</td>
<td>§4.10</td>
<td>Legend</td>
<td>Reuses Eq. 4.12 unchanged under Eq. 3.1g's scaling; introduces <code>t_recert</code> bounding Eq. 4.11's leak over <code>t_dom_legend</code></td>
</tr>
<tr>
<td>4.24</td>
<td>Tetrarch Coherence Fraction</td>
<td>§4.11</td>
<td>Beyond Legend</td>
<td>Averages all six solved <code>Chi</code> pairs as a checkable proxy for closeness to <code>k_unified</code></td>
</tr>
<tr>
<td>4.25</td>
<td>Demiurge Bounded Generative Family</td>
<td>§4.11</td>
<td>Beyond Legend</td>
<td>Counts verified predictions from one proven extrapolation rule, short of full <code>Gen(dM)</code></td>
</tr>
<tr>
<td>4.26</td>
<td>Cosmographer Domain Ratio</td>
<td>§4.11</td>
<td>Beyond Legend</td>
<td>Ratio of achieved to Legend-typical domain size; each increment costs more than the last (§1.4)</td>
</tr>
<tr>
<td>4.27</td>
<td>Communion Pooled Boundary Ratio</td>
<td>§4.11</td>
<td>Beyond Legend</td>
<td>Ratio of a Communion's pooled <code>dM_total</code> to a typical Legend's <code>dM</code></td>
</tr>
</tbody>
</table></div>
<p><em>The foundational mechanism equations (Eq. 1.1–1.4, §1.1–§1.4) sit ahead of the Grand Equation rather than inside it and are indexed by their subsection in <code>codex/foundations.md</code>.</em></p>
<p>Every rank of the Power Hierarchy (§3.3), Novice through Legend, now has at least one applied technique file and at least one formalized equation; the four Ascent Beyond Legend paths (§3.3) each have a closeness/progress equation in <code>codex/techniques-ascension.md</code> (§4.11). See <code>codex/overview.md</code> for the complete file map.</p></div></section>
<section class="book" id="changelog"><header class="book-head"><span class="book-tag">§7</span><h1>Changelog</h1></header><div class="book-body"><p><em>Part of the Aether Codex reference set — see <code>codex/overview.md</code> for the file map.</em></p>
<hr>
<h2>7. Changelog</h2>
<p><em>New techniques, refinements, and derivations are appended to the relevant Codex file with a version bump and a one-line summary here, then given their own subsection under the relevant Part. New equations continue the running numbering in §6 (<code>codex/glossary.md</code>).</em></p>
<p><strong>v2.4 — Cross-Reference Audit &amp; Consistency Pass</strong>
- Full cross-reference audit of all 16 files (equation/section citations, glossary coverage, Spell Directory codes, structural claims); no equations renumbered, no §/Eq. global numbering changed
- Fixed §-vs-Eq. citation swaps: "Eq. 3.4's Unsolved Ceiling" → "§3.4's" (§3.3), "Eq. 3.4 forbids" → "§3.4 forbids" (§4.11), the Sim[...] believed-vs-proven warning re-attributed §3.5 → §3.7 (§3.3), <code>Xi(Ae, g)</code> development pointer corrected to (§3.3, §4.3, §4.9) in §3.1, and §4.5's closing citation corrected from "Eq. 3.1c's combination pattern" to the Adept Combination Pattern (Eq. 4.15, §4.6); §4.11's closeness-auditability framing re-attributed §3.3 → §3.4 (here and in the v2.3 entry below)
- Updated stale ranges left by v2.3's own additions: J-01–J-06 → J-01–J-07 and AR-01–AR-06 → AR-01–AR-07 wherever they described the current directory (§4.5, §4.7, and the v2.3 entry below); §4.4's intro now counts §4.0's four worked examples and carves out N-EM-05 from the "every entry sources a distortion" claim
- Renamed the Eq. 4.10/4.12 background constant <code>k_grav</code> → <code>k_newton</code> to end the collision with the solvable gauge coupling <code>k_grav</code> (Eq. 3.1c, Eq. 4.0b); glossary updated, and §4.0's "same <code>k_grav</code>" throughline reworded to "gravity, at opposite ends of the hierarchy"
- Added an explicit direction parameter <code>s = +/-1</code> to Eq. 4.19, replacing prose that reversed the sign of <code>Fid</code> (bounded to [0,1] by Eq. 3.2); M-01/M-02 updated to match, and M-02 re-anchored from Eq. 4.18 to Eq. 4.19 (its described effects are property nudges, not identity rewrites)
- Re-paired J-05 (Two-Handed Smith) as Eq. 4.0a + Eq. 4.0c so AD-01 (Flash-Forge, EM+Strong) genuinely supersedes it; §4.5's echo updated; §4.4's Journeyman preamble now covers either/or entries (J-03) and same-force pairs (J-02, J-06); §4.5's <code>tau_switch</code> training examples now cite J-07 rather than J-03
- §3.3 tidy-up: subclass claim now names the Sovereign→Legend step as the exception that admits no partial rung; "three gauge-and-matter tiers" corrected to five; the Unsolved Ceiling moved out of the tier table into a footnote (it is a limit, not a tier — keeping §3.3's "not a ninth tier" arithmetic honest); Warden's <code>Xi_1</code> no longer hedged as "often" (Eq. 4.20 is identically zero without it), matching the tier definition "first-order"
- §4.2's fold fizzle no longer costs "minor fatigue" — aligned with §1.3/§3.5/§3.6's zero-cost quiet failure; §4.9's header now cites Legend's actual home (§4.10); §4.0's closing tier ladder now includes Journeyman and Artisan; §4.4's Eq. 4.15 block is now explicitly a restatement of §4.6's definition; §4.4 now names its one uncatalogued rank (Sovereign) and points to §4.1–§4.3
- Glossary: added missing rows (<code>A_op</code>, <code>Loop_dM[...]</code>, <code>Dpath(Ae)</code>, <code>hbar</code>, <code>X_ideal</code>/<code>X_eff</code>, <code>t_rel</code>, <code>eta</code>, <code>m_obj</code>/<code>g_local</code>/<code>F_net</code>, <code>P_out</code>/<code>E_per_decay</code>/<code>N_unstable</code>, <code>Effect_i</code>, <code>dAe_local</code>, <code>E_back_mat</code>, <code>E_back_pert</code>, <code>s</code>); fixed <code>t_dom_legend</code>'s defined-in pointer (Eq. 4.22/4.23, not Eq. 3.1g); marked <code>C_sel</code> as a legacy symbol appearing in no equation; <code>eta</code> also added to Eq. 4.6's inline symbol table; <code>V_out</code>/<code>L_out</code>/Eq. 4.0d's output symbols now named inline in §4.4
- Corrected ledger arithmetic in earlier entries: v2.1's Novice count 15 → 11; v2.3's new-directory-entry count 12 → 10</p>
<p><strong>v2.3 — Full Hierarchy Coverage</strong>
- Closed every remaining gap in the Power Hierarchy's applied-technique coverage: every rank from Novice through Legend now has a dedicated technique file and at least one formalized equation, and the four Ascent Beyond Legend paths each have a checkable closeness metric
- Added <code>codex/techniques-journeyman.md</code> (§4.5, Eq. 4.13 — Sequential Invocation Overhead): formalizes the disjoint activation windows and switching cost (<code>tau_switch</code>) between two solved <code>k_f</code> terms held without a cross-coupling, giving the existing J-01–J-07 directory entries a shared mathematical backbone
- Added <code>codex/techniques-adept.md</code> (§4.6, Eq. 4.14–4.15): formally defines <code>Chi(f1,f2)</code>, previously a named-but-undefined placeholder, as a real overlap measure (Eq. 4.14), and promotes the Spell Directory's informal Adept Combination Pattern to a numbered equation (Eq. 4.15)
- Added <code>codex/techniques-artisan.md</code> (§4.7, Eq. 4.16–4.17): a quark-sector analogue of Eq. 4.0a (Eigenvector Draw) giving AR-01–AR-07 a shared formal backbone, plus a quark-sector analogue of Eq. 4.7's backlash integral (Off-Basis Extrapolation) confirming §1.3's claim that the fizzle/backlash mechanism is universal across all three coupling channels
- Added <code>codex/techniques-master.md</code> (§4.8, Eq. 4.18–4.19): Full Transmutation (a unitary operator over the complete <code>M_op</code> eigenbasis) and Universal Binding &amp; Decay Control (generalizing Eq. 4.0c/4.0d to any material once <code>c_M</code> is unrestricted by a partial <code>S</code>)
- Added <code>codex/techniques-warden.md</code> (§4.9, Eq. 4.20–4.21): the first metric-sector (<code>delta(g)</code>) applied technique below Sovereign — a perturbative curvature effect confined to a single validated geometry (<code>R_proven</code>), plus the backlash mode for extrapolating past it
- Split the former combined Sovereign/Legend technique file: <code>codex/techniques-sovereign.md</code> now covers Sovereign scope only (§4.1–§4.3, Eq. 4.1–4.12, unchanged); new <code>codex/techniques-legend.md</code> (§4.10, Eq. 4.22–4.23) extends the same mathematics — explicitly not re-derived — to Legend's standing, generational scale, introducing <code>t_drift</code> and <code>t_recert</code> as the operative upkeep constraints at that scale
- Added <code>codex/techniques-ascension.md</code> (§4.11, Eq. 4.24–4.27): one closeness/progress equation per Ascent Beyond Legend path (Tetrarch, Demiurge, Cosmographer, Communion), honoring §3.4's own framing that closeness is auditable even though completion never is
- Added one new Novice equation, Eq. 4.0e (Ripple Sense): a passive, risk-free detection use of the <code>k_EM</code> channel in reverse, rounding out Novice tier with a technique that reads rather than sources
- Added 10 new Spell Directory entries across the newly-formalized ranks: N-EM-05, J-07, AR-07, M-01, M-02, W-01, LG-01, LG-02, AS-01, AS-02, plus the retitled AD- pattern block (now Eq. 4.15) — see §4.4 for the full list; new directory code prefixes <code>M-</code>, <code>W-</code>, <code>LG-</code>, <code>AS-</code> introduced alongside the existing <code>N-</code>, <code>J-</code>, <code>AD-</code>, <code>AR-</code>
- Added corresponding glossary (§5) entries for every new symbol, filled a pre-existing gap (<code>c_M</code> was used in §1.3 but never glossed), and added all 16 new rows to the Equation Index (§6)
- Updated <code>codex/overview.md</code>'s file map, reading order, and extension conventions to reflect the now-complete hierarchy</p>
<p><strong>v2.2 — Split into Reference Files</strong>
- Split the single <code>v1.md</code> document into nine files under <code>codex/</code>: <code>overview.md</code> (file map, reading order, extension conventions), <code>foundations.md</code> (§1–§2), <code>grand-equation.md</code> (§3.1–§3.2, §3.4–§3.7), <code>power-hierarchy.md</code> (§3.3), <code>techniques-novice.md</code> (§4 preamble, §4.0), <code>techniques-sovereign.md</code> (§4.1–§4.3), <code>spell-directory.md</code> (§4.4), <code>glossary.md</code> (§5–§6), <code>changelog.md</code> (§7)
- All § and Eq. numbering is global and unchanged; each file carries a short header noting what it houses and where its neighbors live
- No equations, symbols, or technical content changed — structural reorganization only
- <code>v1.md</code> deleted after verification; the split files are now the canonical Codex</p>
<p><strong>v2.1 — The Spell Directory</strong>
- Added Eq. 4.0d (Decay Nudge), completing the four-force set of Novice worked examples begun in §4.0
- Added §4.4, The Spell Directory: a coded catalog (<code>N-</code>, <code>J-</code>, <code>AD-</code>, <code>AR-</code>) of Common and Uncommon techniques — 11 Novice entries across all four forces, 6 Journeyman entries demonstrating unblended alternation, 6 Adept entries (one per unordered force pair, introducing the shared <code>Chi(f1, f2)</code> cross-coupling pattern), and 6 Artisan signature-material entries
- Directory entries are deliberately not added to the Equation Index individually — they draw on already-indexed base equations rather than each requiring new global numbering, keeping the catalog easy to extend
- Added corresponding glossary (§5) entries for <code>Gamma_0</code>/<code>Gamma_eff</code> and <code>Chi(f1, f2)</code></p>
<p><strong>v2.0 — Subclasses &amp; The Ascent Beyond Legend</strong>
- Expanded the Power Hierarchy (§3.3) with three intermediate subclasses — Journeyman (between Novice/Adept), Artisan (between Adept/Master), Warden (between Master/Sovereign) — each defined by a genuine but incomplete solution to the next tier's term, not a new term of its own
- Split the former combined "Sovereign / Legend" row into two sequential tiers, distinguished by how far a solved <code>Xi(Ae, g)</code> reaches rather than by different mathematics (Eq. 3.1g)
- Added Eq. 3.1e (Partial Diagonalization), Eq. 3.1f (Perturbative Aether-Geometry Coupling), and Eq. 3.1g (Domain Persistence), each extending an existing Eq. 3.1 sub-term rather than introducing a new one
- Added "The Ascent Beyond Legend" (§3.3): four divergent, historically-attested paths toward apotheosis — Tetrarch (gauge unification), Demiurge (matter-generation), Cosmographer (unbounded geometry), Communion (pooled comprehension) — each pushing one piece of <code>L_total</code> or <code>dM</code> to its limit while remaining provably incomplete per §3.4
- Added corresponding glossary (§5) and Equation Index (§6) entries</p>
<p><strong>v1.9 — Simulated Invocation</strong>
- Added §3.7 and Eq. 3.5 (Simulated Invocation): a <code>Sim[...]</code> prefix that evaluates any equation's fidelity readout — projected output, projected backlash energy — without passing the result into Eq. 3.1's <code>Loop_dM[...]</code> selection, so nothing is actually manifested
- Established that <code>Sim[...]</code> reps count fully toward <code>prac(x)</code> (§3.6), making fidelity practice free of real-world risk regardless of a technique's tier
- Established the deliberate limit: <code>Sim[...]</code> scores execution against the caster's <em>believed</em> <code>phi_ideal</code>, so it cannot validate an unproven or misjudged claim — comprehension-driven backlash risk (§2, §3.6) is untouched by this mechanic
- Cross-linked §2, §3.5, and §3.6 to the new section; added glossary entries for <code>Sim[...]</code>, <code>X_eff_proj</code>, <code>E_back_proj</code> and an Equation Index row for Eq. 3.5</p>
<p><strong>v1.8 — Novice Techniques &amp; Course Structure</strong>
- Added §4.0, the first Novice-tier worked examples: Eq. 4.0a (Thermal Excitation — "boiling water"), Eq. 4.0b (Minor Levitation), Eq. 4.0c (Minor Cohesion Boost), each a single closed-form <code>k_f</code> term
- Clarified the distinction between <code>k_grav</code> (a simple force-coupling, exercised directly for the first time in Eq. 4.0b) and <code>Xi(Ae, g)</code> (true metric curvature, §4.3) — same underlying force, opposite ends of the Power Hierarchy
- Added a Tier column to the Equation Index (§6) so the document can start functioning as a course syllabus; flagged that Adept and Master tiers have no applied techniques yet
- Linked the Novice row of the Power Hierarchy (§3.3) to its new worked examples</p>
<p><strong>v1.7 — Study Guide Restructure</strong>
- Removed the Worldbuilding Hooks &amp; Open Threads section entirely; this document is now scoped as a study guide and glossary for the mechanics of the magic system, not a source of narrative/story hooks
- Renumbered the Equation Index to §6 and the Changelog to §7; updated the subtitle and all internal cross-references accordingly
- No equations, symbols, or technical content changed</p>
<p><strong>v1.6 — Grand Equation Tidy-Up</strong>
- Decomposed Eq. 3.1 into a top-level path integral plus four named sub-equations (Eq. 3.1a–3.1d: Aether Action, Total Lagrangian Density, Gauge Term, Quark Term), replacing the single deeply nested one-line form
- Updated the Term Reference (§3.2) and Glossary (§5) to point each symbol at its precise sub-equation rather than the whole of Eq. 3.1
- Added the corresponding rows to the Equation Index (§6)
- Readability pass only — no physical content changed from earlier versions</p>
<p><strong>v1.5 — Condensed Form</strong>
- Added Eq. 4.12, folding the well source, counter-curvature shell, and residual outreach (Eq. 4.8, 4.9, 4.11) into a single piecewise expression using <code>Bump</code>, <code>Shell</code>, and <code>Step</code> as radius-selecting switches
- Kept the horizon/lapse condition (Eq. 4.10) as an explicit companion constraint rather than merging it into the main line, since it governs proper time rather than curvature</p>
<p><strong>v1.4 — The Bound Singularity</strong>
- Added a Sovereign/Legend-tier technique (§4.3) for generating a localized, aether-sourced gravity well with an engineered containment boundary
- Introduced Eq. 4.8 (well source), Eq. 4.9 (counter-curvature shell / anti-gravity field), Eq. 4.10 (containment lapse and horizon tuning — the time-dilation component), and Eq. 4.11 (residual outreach from imperfect shell fidelity)
- Distinguished two independent failure modes: shell rupture (a Fidelity Principle failure) vs. horizon migration (a subtler failure that can pass every static measurement while remaining causally unsealed)
- Added three worldbuilding hooks reflecting the new technique (later removed, see v1.7)</p>
<p><strong>v1.3 — Notation Overhaul &amp; Unassisted Invocation</strong>
- Replaced every symbol in the document with a plain-ASCII equivalent for ease of typing in the manuscript. Legacy mapping, for cross-referencing older drafts:</p>
<div class="table-scroll"><table>
<thead>
<tr>
<th>Old</th>
<th>New</th>
<th>Old</th>
<th>New</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ψ / Ψ†</td>
<td><code>Ae</code> / <code>Ae*</code></td>
<td>Γ_decohere</td>
<td><code>G_dec</code></td>
</tr>
<tr>
<td>κ_f</td>
<td><code>k_f</code></td>
<td>σ_interference</td>
<td><code>s_int</code></td>
</tr>
<tr>
<td>F_f^μν</td>
<td><code>F_f</code></td>
<td>η</td>
<td><code>eta</code></td>
</tr>
<tr>
<td>M̂</td>
<td><code>M_op</code></td>
<td>𝔉 / 𝔉_min</td>
<td><code>Fid</code> / <code>Fid_min</code></td>
</tr>
<tr>
<td>Ξ(Ψ,g_μν)</td>
<td><code>Xi(Ae, g)</code></td>
<td>φ_ideal / φ_actual</td>
<td><code>phi_ideal</code> / <code>phi_actual</code></td>
</tr>
<tr>
<td>∂ℳ</td>
<td><code>dM</code></td>
<td>τ / τ_ins / τ_rel</td>
<td><code>t</code> / <code>t_ins</code> / <code>t_rel</code></td>
</tr>
<tr>
<td>Û(x_A→x_B)</td>
<td><code>U_op(A, B)</code></td>
<td>α(τ), β(τ)</td>
<td><code>a(t)</code>, <code>b(t)</code></td>
</tr>
<tr>
<td>Ω²(x)</td>
<td><code>Om2(x)</code></td>
<td>⟨a|b⟩</td>
<td><code>&lt;a|b&gt;</code> (unchanged — already typeable)</td>
</tr>
<tr>
<td>δ(...)</td>
<td><code>Delta(...)</code></td>
<td>∮, 𝒟Ψ, ∫</td>
<td><code>Loop[...]</code>, <code>Dpath(Ae)</code>, <code>Int[...]</code></td>
</tr>
<tr>
<td>x_A, x_B</td>
<td><code>A</code>, <code>B</code></td>
<td>γ (transition path)</td>
<td><code>traj</code></td>
</tr>
</tbody>
</table></div>
<ul>
<li>Added Unassisted Invocation (§3.6): a per-term mastery threshold, <code>prac_min</code>, past which a solved equation can be cast through visualization alone, with no physical medium — including live, in-<code>dM</code> recomposition of already-solved terms. Introduced Eq. 3.4.</li>
<li>Added one worldbuilding hook reflecting the new mechanic (later removed, see v1.7).</li>
</ul>
<p><strong>v1.2 — The Fidelity Principle</strong>
- Retired any implication that aether is a finite, consumable, or storable resource; established it as an ambient, inexhaustible field (§3.5)
- Introduced execution fidelity as a second, independent axis alongside comprehension: Eq. 3.2 (Fidelity-Weighted Output), Eq. 3.3 (Minimum Resolution Threshold)
- Cross-linked the Fidelity Principle into the Overlay Fold and Collapse Condition (§4.1, §4.2) to distinguish fidelity failures (quiet fizzle) from comprehension failures (backlash, Eq. 4.7)
- Added two worldbuilding hooks reflecting the new craftsmanship axis (later removed, see v1.7)</p>
<p><strong>v1.1 — Voice &amp; Reference Pass</strong>
- Rewrote document prose for a consistent explanatory register
- Introduced sequential equation numbering (Eq. 3.1–4.7) and the Equation Index (§6)
- Added §-style cross-references throughout; no equations altered in substance from v1.0</p>
<p><strong>v1.0 — Initial Compilation</strong>
- Grand Unified Aether Equation established (§3)
- Power hierarchy tiers defined (§3.3)
- Overlay Fold technique derived — mass-neutral relocation via metric identification (§4.1)
- Collapse Condition derived — resolution mechanic and three failure modes (§4.2)
- Master symbol glossary compiled (§5)</p></div></section>
<p class="footer-note">The Aether Codex · v2.4 · cross-reference audited</p>
</main>
</div>
<script>
(function(){
  var btn=document.getElementById('menuBtn'), rail=document.getElementById('rail');
  if(btn){btn.addEventListener('click',function(){rail.classList.toggle('open');});
    rail.addEventListener('click',function(e){if(e.target.closest('a'))rail.classList.remove('open');});}
  var links={}, as=rail.querySelectorAll('a[data-target]');
  as.forEach(function(a){links[a.getAttribute('data-target')]=a;});
  var current=null;
  function setActive(id){
    if(current===id)return; current=id;
    as.forEach(function(a){a.classList.remove('active');});
    if(links[id])links[id].classList.add('active');
  }
  var books=document.querySelectorAll('section.book');
  var obs=new IntersectionObserver(function(entries){
    entries.forEach(function(en){ if(en.isIntersecting) setActive(en.target.id); });
  },{rootMargin:'-20% 0px -70% 0px'});
  books.forEach(function(b){obs.observe(b);});
})();
</script>
