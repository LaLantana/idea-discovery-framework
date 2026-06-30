# Idea Discovery Framework — Design Notes

This file is for the human maintainer (you) of the idea-discovery skill. It captures design decisions, known principles, and maintenance reminders that don't belong inside the skill's operational files but matter for keeping the framework coherent over time.

Claude does not read this file when running the skill — it lives in the workspace (not in the installed skill) and exists for your reference. The current framework version is **2.0** (see the changelogs at the end).

## Single source of truth: The kill model

The "The kill model" section of `rubric.md` is the consolidated reference for every kill point in the framework — the two veto families (commercial and structural), the function-named gates, veto routing, the matrix kill, and conviction-gated confirmation. If a new kill point is introduced anywhere — in `SKILL.md`, in a section template, or elsewhere in `rubric.md` — it must also be reflected there. If "The kill model" is updated, the corresponding source text must stay consistent.

The user's ability to answer "where can the process stop?" by reading one section depends on this discipline.

## Distribution of kill logic

Kill logic is intentionally distributed across two files, not consolidated:
- **Process flow** (where the analysis can stop — the early-exits and the function-named gates) lives in `SKILL.md` because it governs process flow.
- **The measurement and routing** (what a veto is, the four-dimension score, veto routing, the matrix kill) live in `rubric.md` because they are scoring and measurement rules.

The "The kill model" section of `rubric.md` consolidates the *reference*, not the logic itself. This distribution is correct; do not merge the logic into a single file.

## Gate firing-conditions are canonical in `SKILL.md` (single-source)

Each gate's **firing conditions** — what definitively triggers the Structural gate (legal / data / capability), the Business-model gate (its two causes), the GTM gate, and the early-exits — are stated **once, canonically, in `SKILL.md`'s "The kill model"**. Section templates *apply* their gate and keep their section-specific analytical guidance (e.g., template 07's payback-window benchmarks and Step-2 adjustment menu, template 02's threshold sanity-check, the 2/3-cliff scoring reminders), but they **reference** `SKILL.md` for the condition definitions rather than restating them. `rubric.md` keeps the canonical **measurement and routing** (the two veto families, the routing table, the matrix kill) and points to `SKILL.md` for the conditions.

This refines "Distribution of kill logic" above: process-flow conditions live in `SKILL.md`; measurement/routing lives in `rubric.md`; neither is restated in the templates. Before this cleanup the conditions were triplicated (`SKILL.md` summary + `rubric.md` summary + a full restatement in each owning template), which was the framework's highest drift risk (a change had to be made in three places). If a future change reintroduces a full condition restatement into a template or the rubric, push back — extend the canonical statement in `SKILL.md` instead.

## Two-layer structure of the skill

The skill has two layers that should not be confused:
- **`rubric.md`** defines *how* scores are assigned and what they mean (measurement).
- **Section templates (01–09)** define *what analytical work* Claude does in each framework section (process).

The rubric is read in parts by the templates — each template activates the dimension anchors relevant to its section. Section 09 reads the rubric in full to assemble overall scores and apply the matrix.

When adding new content, ask: is this a measurement rule (rubric) or analytical work (template)? Conflating the two creates the kind of redundancy and contradiction that's hard to debug later.

## Conviction labels are evidence quality, not confidence

Conviction labels (H/M/L) describe the quality of evidence backing a judgment, not how confident the user or Claude feels about it. This distinction is established in the Conviction and scoring section of `rubric.md` but worth restating here because it's the most common drift point in confidence scales.

If you ever find yourself or Claude treating M as "moderate confidence," push back. M is "analogous evidence exists." L is "no external validation." H is "tested against the world."

## Agent-fit is descriptive, not decisional

Agent-fit was tempting to use as a tiebreaker or as a soft scoring input. It is neither. It produces an honest form-factor recommendation that informs execution planning *after* a proceed decision, and contributes portfolio-level visibility into the kinds of ideas being generated. It does not move ideas between matrix quadrants, override kill recommendations, or break ties between similarly-positioned ideas.

If a future change starts using agent-fit to influence decisions, that change is reintroducing the bias the rubric is designed to prevent. Push back.

## Geographic lens is configurable per idea

The framework was originally designed with Colombia as a default lens, then generalized to accept any target market specified in the idea brief. The Colombia-specific lens in earlier drafts has been replaced with a generalized "apply a local lens to whatever market(s) the brief specifies."

When updating the geographic lens, do not re-introduce hardcoded defaults. The lens is configurable for a reason.

## The framework is expected to evolve

The discovery framework is not frozen after first draft. It is meant to be tuned based on what real evaluations surface — patterns of failed-to-kill ideas, dimensions that produce inconsistent scores, anchors that need sharper wording, gaps in coverage that only become visible after running the framework on actual ideas.

Two kinds of change are legitimate:

- **Recalibration:** Updates to anchor descriptions, dimension definitions, kill thresholds, or matrix logic, motivated by patterns observed across multiple evaluations. Tracked in this file under the relevant entry.
- **Extension:** New dimensions, new section content, new sub-templates, motivated by gaps revealed during use. Tracked here when the change affects multiple files.

The discipline that distinguishes legitimate change from drift:
- Recalibration is documented before it is applied, with the motivating evidence named.
- Recalibration updates all dependent files in one pass, not piecemeal.
- Ad-hoc adjustments to anchors during a single evaluation are not recalibration — they are score manipulation.

Future-you should expect to update this framework. Resist treating it as static.

## Section files must contain four documented parts

Every populated section file must contain, in the file itself: (1) Analysis, (2) Recommendation, (3) Rationale, (4) Challenge pass. All four parts are mandatory in both checkpoint and autonomous run modes.

The reasoning behind exactly four parts:
- **Analysis** is the work product.
- **Recommendation** is the actionable output that connects to the next section or to a kill.
- **Rationale** is the explicit reasoning that connects analysis to recommendation. It is not implied by the analysis — it must be stated, so the user can review the chain of reasoning.
- **Challenge pass** is the documented falsification exercise applied to whatever the section concluded.

If a future change attempts to collapse these (e.g., "rationale is obvious from analysis, skip it") or expand them (e.g., "add a sources section"), think carefully. The four-part structure was chosen to make every section file self-contained and auditable. Adding more parts is fine if there's a clear reason; removing parts is not.

## Challenge pass applies to kills, not only to proceeds

The challenge pass is direction-agnostic. Whatever the section concluded — proceed or kill — the four falsification questions try to break that conclusion. A wrongly-killed idea is just as bad as a wrongly-proceeded one, possibly worse because you don't get to discover the mistake later.

Kill recommendations must include the challenge pass output applied to the kill itself, not just to the analysis that led to it (per `SKILL.md`'s "The kill model" section).

If a future change argues that "challenge pass on kills is unnecessary because the analysis already supports the kill," reject it. The whole point of the challenge pass is to test the conclusion, not to support it.

## Wrapper test downgrades agent-fit verdict directly

The wrapper test (from framework section 03 / template 03 when drafted) interacts with the agent-fit verdict as follows: a failed wrapper test (a general-purpose LLM can do this adequately for the user) downgrades the verdict by one level. Strong becomes Partial; Partial becomes Not agent-shaped.

This is intentional — it prevents the analysis from producing a verdict like "strong agent fit, but a thin wrapper." Strong agent fit means the product is differentiated from what general-purpose LLMs can do; if it isn't, the verdict is wrong.

The wrapper test also feeds into the Defensibility dimension of the commercial score, but the agent-fit interaction is independent. Both effects happen.

## Solo-buildability anchors reference the profile's build-speed baseline (single calibration point)

The solo-buildability anchors no longer hardcode build times. They reference **`user-profile.md`'s build-speed baseline** — the assumed time commitment (~20 hours/week), the baseline build window for a standard in-profile MVP, and how that window scales for the learning tiers. The baseline is the **single calibration point**: a different adopter recalibrates solo-buildability by editing that one block in `user-profile.md`, and the rubric anchors shift with it. (Before this calibration pass, the anchors hardcoded "4–8 weeks" *and* the profile described capability separately — a double-coupling that forced edits in two files to recalibrate.)

The same user-calibration caveat still applies to the matrix threshold's bias toward "kill more aggressively." That bias matches a user prioritizing commercial discipline; a user with different priorities (e.g., a learning-first stance) might tune the threshold differently.

These are not universal anchors. Document any recalibration here when it happens.

## The 2×2 matrix is two-axis only

The decision matrix is built from commercial score × solo-buildability score. It is not three-axis. Agent-fit was deliberately kept off the matrix during design — see "Agent-fit is descriptive, not decisional" above.

If a future change attempts to add a third dimension to the matrix (agent-fit, conviction, learning value, etc.), reject it. The matrix's clarity depends on being two-axis. Additional considerations are layered on top of the matrix output, not inside the matrix mechanism.

## The matrix threshold is 6/10, not 5/10

The high/low split on each matrix axis is at 6/10. A score of 6 or above is "high"; 5 or below is "low." This errs on the side of false negatives (killing ideas that might have worked) over false positives (pursuing ideas that won't), which matches the user's stated focus on commercial discipline.

If the threshold is ever changed, document the motivating evidence — what pattern of failed-to-kill or wrongly-killed ideas justified the change — and update the matrix section of `rubric.md` accordingly.

## Commercial score: four dimensions, equal-weighted arithmetic average, no caps

The overall commercial score is the simple arithmetic average of the **four** commercial dimension scores (sum ÷ 4): Problem severity (01), Market size (02), Defensibility (03 provisional → 09 finalized), and Monetization clarity (05). The dimensions are weighted equally. **There are no cap rules.**

This replaces the v1.0 "five dimensions, average-then-caps" model (reversed in the v2.0 kill/score redesign — see that changelog). The caps existed to stop a strong dimension from masking a *fatal* one; v2 removes that need by making a fatal dimension (0–2) a **veto** instead — a dealbreaker that kills the idea at its own section (or, for Defensibility, at 09), so it never enters the average. Because every dimension that reaches the average is therefore ≥ 3, there is no fatal flaw left for an average to hide, and the score becomes a clean, comparable number. A separate mechanical **"weak on multiple fronts" demotion** (two or more dimensions at 3–4 → low-commercial *placement*, score unchanged) handles the "mediocre across the board" case the old 3–4 caps used to catch. Data access was removed as a commercial dimension (now a structural veto in section 04). Equal weighting remains the deliberate default — do not introduce category-specific weighting without evidence from real evaluations (see the Future roadmap).

## Conviction at the threshold breaks ties downward

A score of 6 with Low conviction is treated as below the matrix threshold on its axis. This prevents conviction inflation through the matrix: a 6/L means "I think this just clears the bar, but I have no evidence," and treating it as "high" would inflate the matrix output beyond what the evidence supports.

This rule applies per axis independently. A 6/L on both commercial and solo-buildability is treated as low/low on both.

## Learning-project paths are buildability-gated (matrix override + commercial-veto footnote)

The learning-project path — pursue an idea purely for skill-building, with no expectation of revenue — takes two forms in v2, both gated on the brief's learning field being filled, and both available only where the idea is *buildable*:

1. **Matrix override** — in the low commercial / high solo-buildability quadrant, when the matrix produces a kill, the user may instead pursue as a learning project. (The quadrant guarantees buildability, and only one axis is failing.)
2. **Commercial-veto footnote** — on a commercial-veto kill (Problem 01, Market 02, Monetization 05, or the Defensibility late veto), the idea may be buildable but not monetizable. Because these kills fire before section 06 has run, the footnote lets the user opt to run *section 06 only* to assess buildability, then decide whether to pursue as skill-building.

The unifying principle: **override availability follows buildability.** Without the brief's learning field, the kill stands with no override either way.

Where it is NOT available: the low commercial / low solo-buildability quadrant (not buildable), and **structural-veto kills** (section 04 — legal / data / capability), where the idea can't be built or operated at all. If a future change tries to extend a learning path to those cases, reject it — they lack buildability.

## Recalibration must update templates, not just the rubric

When the rubric is recalibrated (the legitimate reasons and the recalibration discipline are in "The framework is expected to evolve" above), any section templates that reference the changed rubric content must be reviewed and updated for consistency.

Track which templates were updated and which were verified as unaffected. Mid-evaluation anchor adjustments are not recalibration — they are score manipulation. Legitimate recalibration goes through this file and updates all dependent files together.

## Prior evaluations are not re-scored

When the rubric is recalibrated, prior evaluations are not re-scored to match the new version. They remain calibration data for the rubric version under which they were assessed. Future evaluations use the updated rubric.

This rule protects the historical record of how the user's thinking evolved. Re-scoring would erase that data.

## Run mode default is autonomous (reversed from v1.0)

The framework is **autonomy-first**: the default run mode is autonomous (Claude runs all sections end-to-end and surfaces the complete project folder). **Checkpoint mode is opt-in via the brief's run-mode field.**

This *reverses* the v1.0 decision ("default is checkpoint until the framework is validated"). The reversal was deliberate (v2.0 redesign): a "checkpoint until validated" default has no mechanism to know when it is validated, and bakes a future cleanup step into `SKILL.md`. The clean design puts the control where it belongs — the per-evaluation run-mode field. During the current validation phase the maintainer simply sets `run mode: checkpoint` in each brief; once confident, they stop. Nothing in the skill needs to change when validation completes. The autonomy-first default is safe because the mechanical rules (vetoes, the placement demotions, conviction-gated kill confirmation) are designed to hold without a human, and the two mandatory escalations below still force input when it matters.

## Form-factor challenge happens in section 03, not at start

The form-factor bias check is *lightweight* at the start (acknowledge the user's named form factor, commit to challenging it in section 03), and *substantive* during section 03 (active evaluation of form-factor alternatives via the agent-fit assessment).

Earlier drafts tried to make the start-of-analysis check substantive (demanding pre-justification from the user). This was rejected because users cannot reasonably pre-justify a form factor without doing the research that section 03 is designed to do. The current split — lightweight gate at start, real challenge in section 03 — is the correct design.

## File locations

- **Skill folder:** `SKILL-idea-discovery-framework/` — the portable engine (`SKILL.md`, `rubric.md`, `user-profile.md`, `templates/01–09`, and a skill-level `README.md`). Uploaded to Claude via Customize → Skills.
- **Workspace:** `idea-discovery-workspace/` — the user's data: `projects/` (one folder per evaluation), `idea-brief-template.md`, `project-instructions.md`, a workspace-level `README.md`, and this `design-notes.md`.
- **Repo root:** the parent folder holding both, with a top-level `README.md`. Intended for sharing as a public GitHub repo.
- The workspace is not part of the skill. The skill is portable; the workspace is the user's personal data. `design-notes.md` is maintainer-only and is not read during a run, which is why it lives here in the workspace rather than in the installed skill.

## Distinction between SKILL.md run mode and section template requirements

Run mode (checkpoint vs. autonomous) governs *when Claude pauses for user input*. The four-part documentation requirement (see "Section files must contain four documented parts" above) governs *what every section file must contain*. These are independent:

- In checkpoint mode, Claude pauses after writing each section file.
- In autonomous mode, Claude writes all section files end-to-end without pausing.

Two situations force user input even in autonomous mode:

1. **Kill confirmation is conviction-gated** (reversed from v1.0's "every kill always requires confirmation"). In autonomous mode, a kill **auto-confirms** when it rests on solid (High/Medium-conviction) evidence and **escalates to the user** only when a decision-critical claim driving it is Low conviction (the validation layer); in checkpoint mode every kill pauses. This unifies kill confirmation with the validation layer — a kill escalates exactly when it rests on thin, decision-critical evidence — rather than pausing on every kill regardless of evidence. The framework can produce a kill at the early-exits (01/02), the function-named gates (04/05/07), or the matrix / Defensibility late veto (09); each is confirmed per this rule.

2. **High commercial + weak financial picture contradiction in section 09.** When the commercial score is high (≥6) but the financial picture from section 08 is weak (doesn't meet the make-money threshold, or meets only marginally), the matrix placement and the financial picture are in tension. This contradiction is too consequential for automatic resolution and pauses for user input. The user chooses among three options: trust the matrix placement, trust the financial picture, or revisit the analysis.

These are the only two situations that force input in autonomous mode (case 1 conditionally, on low conviction; case 2 always). Future changes that add new overrides should be added to this list and reflected in the corresponding template.

## Kill & score model v2.0 — changelog (2026-06-29)

The v2.0 redesign reworked the framework's **kill and score model**. The design document is `redesign-spec-kill-and-score-model.md` (at the repo root); the critical analysis that preceded it is `design-analysis.md`. Per the framework's own discipline, prior evaluations are not re-scored against v2.0. The organizing idea: separate **vetoes** (dealbreakers, fired the moment they are definitively known, routed by type) from **scores** (degrees that place an idea on the matrix) — which removed the conflation the old cap rules papered over.

### Scoring
- **Commercial score is now four dimensions, a plain arithmetic average, no caps.** Dimensions: Problem severity (01), Market size (02), Defensibility (03 provisional → 09 finalized), Monetization clarity (05). The cap rules are deleted; a fatal 0–2 dimension is now a *veto* (so the average only ever combines dimensions ≥ 3), and a mechanical **"weak on multiple fronts" demotion** (two-plus dimensions at 3–4 → low-commercial placement, score unchanged) replaces the old 3–4 caps. Reverses the v1.0 "five dimensions, average-then-caps" entry above. (No geometric mean — considered and dropped as unnecessary once the veto/score split removed the problem caps solved.)
- **Overall commercial conviction = the lowest of the four dimensions.**
- **Data access removed as a commercial dimension** and relocated to section 04 as a structural veto (the opportunity-level "can anyone obtain it"); the user-level "can THIS user" stays in section 06. Reverses the v1.0 "Data access stays in the commercial score" decision.

### Vetoes, gates, routing
- **Two veto families.** *Commercial vetoes* (a dimension at 0–2) route to kill or pivot (a re-brief) — never partner. *Structural vetoes* (legal / data / capability, all assessed in section 04) route uniformly partner / kill / park, with the partner route stated as conditional on the still-partial commercial picture.
- **Gates renamed by function** (no more Gate 1/2/3): Problem (01), Market (02), Structural (04), Business-model (05, two causes), GTM (07), plus the Defensibility late veto and the matrix decision (09).
- **Early-exit.** Problem (01) and Market (02) fire as early-exits — kill and stop, skipping later sections — following the full kill protocol (four parts, challenge pass on the kill, conviction-gated confirmation). Defensibility is deliberately *not* an early-exit: scored provisionally at 03 and finalized at 09 (a late veto), because moats can emerge in 04/05.
- **Section 04 keeps its name ("Risk and compliance")** but its scope expanded to hold the data-access and capability-feasibility structural checks on top of the full compliance research — which remains load-bearing (a veto is a conclusion *from* the research, never a substitute for it).
- **Business-model gate (05) split into two causes** that route differently: no-legal-model → restructure / licensed-partner else kill; Monetization 0–2 → clean kill or model pivot (never partner).

### Conviction & validation
- **Validation layer (new).** At any decision (proceed *or* kill), decision-critical low-conviction claims must be validated or explicitly accepted as recorded risk before the decision is final. Symmetric across proceeds and kills; gates only the load-bearing claims.
- **Kill confirmation is conviction-gated** (reverses v1.0's "every kill always requires confirmation"): autonomous kills auto-confirm at High/Medium conviction and escalate only on low conviction; checkpoint pauses all. The §09 high-commercial / weak-financial contradiction remains a mandatory escalation.

### Run mode
- **Default reversed to autonomous** (was checkpoint). Checkpoint is opt-in via the brief's run-mode field — see the standing entry "Run mode default is autonomous" for why the "checkpoint until validated" default was retired.

### Files changed (one pass)
`rubric.md` and `SKILL.md` (the core engine); templates 01–09; the brief template and both workspace/skill READMEs (run-mode + kill-confirmation language); and these design notes. Version bumped **1.0 → 2.0** in `SKILL.md` (section 09 records it in each evaluation's portfolio metadata). Verified by cross-file grep and two independent subagent audits against the 13 model invariants.

## Solo-buildability calibration — recalibration (2026-06-29)

A focused recalibration of the solo-buildability inputs (from `design-analysis.md` §4), applied after the v2.0 model redesign:

- **`user-profile.md` is now the single solo-buildability calibration point.** A new **build-speed baseline** block holds the assumed time commitment, the baseline build window, and how it scales for the learning tiers; `rubric.md`'s anchors reference it instead of hardcoding "4–8 weeks." One-file recalibration for a different adopter.
- **Time availability fixed at ~20 hours/week** as a stable profile assumption (rather than a per-evaluation brief field — that remains a deferred `design-analysis.md` #3 item). Section 06's time-to-MVP estimates are calibrated to this commitment. **Financial runway is *not* fixed here** — it stays per-idea in sections 07/08; folding it into the brief is the open half of design-analysis #3.
- **Perishable specifics stripped** from the profile (e.g., "deploying now with Claude Code," "the workflow is currently in the test phase," "Shopify customization") so the profile holds stable capability, not time-stamped claims that age within months.
- **Design/UX is never a solo-buildability constraint** — stated absolutely, including for design-led products where design is the commercial differentiator. (Design being a product's differentiator is a section-03 defensibility question, not a section-06 build bottleneck for this AI-native user.)

Version stays **2.0** — this is a calibration/portability refinement within the v2.0 model, not a change to the kill/score model itself.

## Kill-gate condition de-duplication — maintenance refactor (2026-06-29)

Implements roadmap **#4** (from `design-analysis.md` §2, the highest remaining drift risk). Before this pass, each gate's firing conditions lived in **three** places — a summary in `SKILL.md`, a summary in `rubric.md`, and a *full restatement in the owning template* (04/05/07 each re-derived their conditions in detail; 01/02 each restated the early-exit kill protocol). v2.0's gate expansion (Structural gate → legal/data/capability; Business-model gate → two causes) widened this triplication. A single condition change had to be hand-synced across three files — exactly the kind of drift the framework's sync discipline is meant to avoid.

The decision (approved before implementation) — **conditions-only canonicalization in `SKILL.md`**:

- **`SKILL.md`'s "The kill model"** is now the single canonical statement of each gate's firing conditions. Its per-gate bullets were expanded from one-liners into the full definitions (the Structural gate's three conditions with their "obtainable by no one" tests and the disproportionate-cost carve-out; the Business-model gate's two causes; the GTM gate's "no recoverable CAC after the Step-2 attempt"; the Problem/Market early-exits; the §09 Defensibility late veto + matrix kill).
- **Templates 04/05/07** keep all analytical work (the research/tasks that produce the inputs) and the *act* of applying the gate, but reference `SKILL.md` for the condition definitions instead of restating them. Section-specific analytical guidance stays in place: template 07's payback-window benchmarks and Step-2 adjustment menu, template 02's threshold sanity-check, the 2/3-cliff scoring reminders.
- **Templates 01/02** trim their early-exit kill-protocol restatement to a reference (the protocol is already canonical in `SKILL.md`), keeping the section-specific bits (01's pivot-routing example, 02's threshold sanity-check) and the scoring reminders.
- **Template 09** was verified to reference `rubric.md`/`SKILL.md` for the matrix threshold, conviction-tie, and veto reconciliation; it legitimately applies the matrix in-place (it is the "reads the rubric in full" section), so its mechanics stay.
- **`rubric.md`** keeps the canonical measurement and routing — the two veto families, the routing table, the matrix kill, and "What is *not* a kill criterion" (kept verbatim) — and its "The gates (named by function)" list now points to `SKILL.md` for the conditions rather than restating them.

**Routing was deliberately left as-is** (canonical in `rubric.md`, summarized-with-pointer in the templates): this pass targets *condition* duplication only, the clearly-agreed scope. Tightening the templates' routing summaries is a separate, smaller cleanup if it proves worth it.

No behavior change — the conditions are identical, only relocated — so the **version stays 2.0**. No prior evaluations to re-score (`projects/` is empty; the no-re-score rule applies regardless). Files changed in one pass: `SKILL.md`, `rubric.md`, templates 01/02/04/05/07/09, and this file. Verified by cross-file grep and a verification subagent audit against the kill-model invariants.

## Lean-start set completion — runway field, anchor exemplars, output formats (2026-06-29)

The remaining lean-start items from the Future roadmap — **#3** (runway half), **#11** (worked anchor exemplars), **#2** (output formats, trimmed) — implemented in one pass after the #4 de-duplication. All three are additive/refinement within v2.0 (no change to the kill/score model), so the **version stays 2.0**. No prior evaluations to re-score.

**#3 — Runway field in the brief (the open half of design-analysis #3).** Sections 06/07/08's capital estimates rested on a runway figure implicitly — and template 07 already referenced "the user's capital availability (*from the brief* …)" and evaluated GTM candidates against "runway" for a brief field that **did not exist** (a dangling reference). Added a **Runway** field to `idea-brief-template.md` (capital available for this idea before it must sustain itself), **optional with a fallback**: if blank, sections 07/08 still run, report the capital required, and note that no runway ceiling was given — preserving autonomy-first behavior. Template 07 now compares the initial-investment picture against the runway (closing the dangling reference), template 08 compares cumulative capital required against it, and template 06 flags if build capital alone would exceed it. `SKILL.md`'s "How to start" adds runway to the brief fields to confirm. (The time-commitment half of #3 was already handled — ~20 h/week fixed in `user-profile.md`, 2026-06-29 — so this completes #3.)

**#11 — Worked anchor exemplars.** The anti-inflation cross-idea calibration check only activates once a portfolio exists, so the first ideas set the baseline with no exemplars; the rubric gave anchor *descriptions* but no worked examples. Added one or two concrete scored exemplars beneath each commercial dimension's anchors (Problem severity, Market size, Monetization clarity, Defensibility) and the solo-buildability anchors in `rubric.md` (e.g., a worked "3/H Problem severity"). Exemplars live once, in `rubric.md`, beside the anchors they illustrate (templates reference those anchors, not copies). Purely additive — no scoring behavior change, and the exemplars are explicitly illustrative, not additional anchors.

**#2 (trimmed) — Output formats.** Prose is the right default for the reasoning-heavy sections, but a few have natively tabular/visual outputs forced into prose — worst case section 08's multi-year, multi-scenario projection. Per the Restraint check, three targeted changes, **not** a per-section table mandate: (a) `SKILL.md` gains a short "Output format" note — markdown prose by default, tables/visuals welcome where the data is natively tabular, reasoning stays in prose; (b) template 08 gets a structured projection table (years × scenarios, with the cumulative-capital row); (c) template 09 gets a score table (dimension | score | conviction) and a simple 2×2 matrix visual, and `rubric.md`'s "Visual reference" line is softened from "a literal visual is not required" to encourage the section-09 matrix visual.

With this pass the **lean-start set is complete** (#4, #3, #11, #2). Files changed: `idea-brief-template.md`, `rubric.md`, `SKILL.md`, templates 06/07/08/09, and this file. Verified by cross-file grep, a consistency read, and a verification subagent audit.

## Anchor-copy resync + #7 deferral (2026-06-29)

Evaluated roadmap **#7** (de-duplicate the dimension anchors that the scoring templates restate from `rubric.md`) and **deliberately deferred it** — recorded here so it isn't re-litigated. Unlike the #4 gate-condition de-dup, #7 is a genuine trade-off, not a clear win: the dimension anchors are the standard the scorer measures against at the core scoring moment of *every* evaluation, so keeping them *in-context in the owning template* is a reliability feature, not mere redundancy. The proposed hybrid (full anchors in the rubric, a gloss in each template) is a messy middle — a gloss is itself a smaller copy that can drift, so it pays the refactor cost without buying clean single-sourcing. The Restraint check in `design-analysis.md` flagged #7 as the one not to do reflexively. Revisit only if real evaluations show the copies drifting repeatedly across maintenance cycles — the standing trigger for graduating a deferred item.

**What was done instead (the proportionate fix).** The templates that copy the rubric's anchors — 01 (Problem severity), 02 (Market size), 03 (Defensibility), 05 (Monetization clarity) — were checked against the rubric and the drift that had already crept in was resynced:
- **Template 01** had condensed the Problem-severity *High* band and dropped real nuance — the "(weekly or more)" frequency cue, the "(costs significant time, money, or friction)" materiality cue, and the *"unprompted complaints alone are not enough"* caveat. Restored to match the rubric. (Template 02 had a trivial wording divergence, also aligned; 03 and 05 were already in sync.)
- Each anchor block in 01/02/03/05 now carries a one-line **canonical-source marker** pointing to `rubric.md` (where the bands and the worked examples live) and noting the copies must be kept in sync — so a maintainer sees the source of truth and the sync obligation right at the copy site.

The standing rule "Recalibration must update templates, not just the rubric" remains the mitigation for the retained duplication. No scoring-model change — **version stays 2.0**. Files: templates 01/02/03/05 and this file.

## Systematic review v1.0 — changelog (2026-06-25)

The first end-to-end systematic review took the framework from first draft to a coherent v1.0. It resolved every entry in the former "Known issues to revisit after first pass" list (now retired) plus several inconsistencies surfaced during the review. This is the record of what changed and why. Per the framework's own discipline, prior evaluations are not re-scored against v1.0.

### Scoring

- **Commercial-score combination settled: equal-weighted average, then caps.** `rubric.md` had said "not an average — holistic judgment," contradicting template 09 and these notes ("simple average, sum ÷ 5"). Resolved in favour of average-then-caps and `rubric.md` rewritten to match. (Later reversed in v2.0 — see the v2.0 changelog above and the current standing entry "Commercial score: four dimensions, equal-weighted arithmetic average, no caps.") Equal weighting confirmed as the deliberate default.
- **Data access stays in the commercial score as a market-structure question.** Anchors tightened to "is access structurally available in the market," and the user-specific "can THIS user obtain it" question is now explicitly handled in section 06 — cross-referenced in `rubric.md`, template 02, and template 06. Not split into two dimensions; not moved.

### Agent-fit

- **Analytical method moved to template 03; `rubric.md` keeps the scoring outputs.** The five evaluation lenses (with anti-examples), the verdict heuristic, and the default-skepticism instruction now live in template 03, where the evaluation runs. `rubric.md` retains the verdict definitions, the format/examples, the wrapper-test downgrade rule, and the usage rules — shrinking it toward the size of the other dimension definitions.
- **`SKILL.md` "tiebreaker" language corrected.** SKILL.md's Scoring summary had called agent-fit a "tiebreaker," contradicting `rubric.md` and the "Agent-fit is descriptive, not decisional" entry above. Corrected to descriptive-only.

### De-duplication into SKILL.md

- **Deep-research escalation is now a standing protocol in `SKILL.md`.** Templates name only their section-specific triggers and reference the protocol instead of each restating the "I think deep research is warranted… proceed?" escalation. Applied to every template that mentions deep research (01–08).
- **The "revisit upstream if a downstream section can't draw on outputs" rule is now a standing rule in `SKILL.md`.** The identical closing sentence was removed from every template's Downstream-dependencies section; templates keep only their consumption mappings.
- **Workaround-check variation is now documented as intentional.** Templates 04 and 05 introduce new alternatives; template 07 runs a thoroughness check on its Step 2 (which already generates alternatives). Each check now states its role inline so the difference reads as deliberate.

### Templates

- **Template 07's post-launch investment window is now model-aware** (~3 months consumer / ~6 months transactional / ~12 months B2B), replacing the fixed 6-month default, still overridable via the brief.
- **Templates 06 and 09 no longer cite `design-notes.md` as the source of operational rules.** The 6/10 threshold, the conviction-tie rule, and "solo-buildability never kills" were cited to design-notes — which Claude does not read during a run — and have been repointed to `rubric.md`, where they live. (Surfaced by moving design-notes into the workspace.)

### Structure, naming, paths

- **Skill renamed `idea-discovery`** (the SKILL.md frontmatter still said `product-discovery` while everything else said idea-discovery). Titles and the rubric title updated to match.
- **Section-03 rename and filename casing fixed** across `SKILL.md` and templates 01/02 ("Form factor & differentiation"; `07-investment-and-GTM.md`).
- **All folder paths normalized:** `discovery-workspace/` → `idea-discovery-workspace/`, `product-discovery/` → `SKILL-idea-discovery-framework/`, and the stale project path in `project-instructions.md`. The brief template gained an explicit **Idea name** field so SKILL.md's folder-derivation resolves.
- **`design-notes.md` moved into the workspace** (its current home), so the maintainer-only notes are not shipped with the installed skill.
- **`idea-brief-template.md` is canonical in the workspace only** (no skill-folder duplicate, to avoid drift); the READMEs point to it there.

### READMEs

- **Three purpose-built READMEs:** repo-root (what the repo is, the skill/workspace split, setup), skill-folder (install and maintain the skill), and workspace (run/revisit/maintain evaluations). The original single draft was a misplaced workspace guide; its content was relocated and corrected, and the other two were written fresh. design-notes (the "why") and the workspace README (the "how") are kept as distinct documents.

### Portfolio / calibration

- **Cross-idea calibration now reads the workspace `projects/` folder** (where evaluations are actually saved) instead of the never-populated `references/past-evaluations/`, which has been removed from the docs.
- **A framework-version field was added** — version **1.0** is stated in `SKILL.md` and recorded in section 09's portfolio metadata, so future evaluations stay comparable across framework changes.

## Future roadmap (post-v2.0)

Deliberately deferred from the v1.0 review and not taken up in the v2.0 kill/score redesign — to be taken up when there is evidence or need, not before:

- **Re-evaluation triggers** (scheduled cadence; market-condition changes; `user-profile.md` updates that move ideas near the solo-buildability threshold; framework-version divergence).
- **Status lifecycle** for evaluated ideas (active / paused / killed / completed / on-hold), to track changes after the decision.
- **Empirical cross-idea calibration** once a portfolio exists — checking whether H-conviction/high-commercial ideas actually outperform, whether the vetoes and the "weak on multiple fronts" demotion fire on the right ideas, and whether the 6/10 thresholds hold up over time.
- **Category-specific commercial weighting** (B2B vs. consumer, marketplace vs. direct) — only if real evaluations show equal weighting is systematically mis-scoring; would require a category-classification step before the commercial-score assembly.

### Open items from `design-analysis.md` (the 2026-06-25 design critique)

The critique proposed 12 prioritized recommendations plus a few looser observations; the v2.0 redesign and the 2026-06-29 calibration pass implemented several. The rest are the open backlog below — full reasoning and the Restraint check (which trims several) are in `design-analysis.md` at the repo root.

**Already implemented — do not redo:** #1 early-exit (v2.0); #6 single solo-buildability calibration point (the build-speed baseline, 2026-06-29); #3 time-commitment half (~20 h/week fixed in `user-profile.md`); #12 learning-value half (settled as the buildability-gated footnote); #4 kill-gate condition de-duplication (2026-06-29 maintenance refactor — see the changelog above); #3 runway half, #11 worked anchor exemplars, and #2 output formats (2026-06-29 lean-start completion — see the changelog above).

**Lean-start set — complete (2026-06-29).** All four recommended starting points are now implemented: **#4** (kill-gate condition de-duplication), **#3** (runway field), **#11** (worked anchor exemplars), and **#2** (output formats, trimmed). See the changelogs above. The strategic/larger items below remain deferred until there is evidence or need.

**Strategic / larger (defer until evidence or need):**
- **#5 — Fast-triage / pre-screen mode.** Only if the early-exit (#1) proves insufficient; it largely overlaps #1, so don't build both.
- **#7 — Reduce template↔rubric anchor duplication.** A genuine trade-off (drift-risk vs. proximity), not a clear win — decide deliberately. **Evaluated and deferred 2026-06-29** (in-context anchors aid scoring reliability at the scoring moment; the gloss approach is a messy middle; drifted copies were resynced and canonical-source markers added instead — see the changelog above). Revisit if repeated cross-cycle drift appears.
- **#8 — "Park with a re-evaluation trigger" outcome.** v2.0 added *park* routing for capability vetoes; a general timing-park plus the trigger machinery overlaps the "Re-evaluation triggers" and "Status lifecycle" items above.
- **#9 — Optional shareable exports.** A 1-page decision summary (especially for the partnership path) earns its place; an `.xlsx` financial model does not — resist until an idea has passed.
- **#10 — Agentic harness.** After manual validation, with enforced research-grounding, a structured score artifact, and controller + per-section sub-agents.
- **#12 (founder–market-fit half) — Decide whether unfair-advantage / distribution access deserves weight** (e.g., folded into Defensibility), without adding a third matrix axis.

**Further observations (not in the prioritized 12):**
- **Time-to-decision budget.** Give an evaluation a rough target time (≈X hours) to reinforce the lightweight-filter intent and fight scope creep. Cheap; the critique never prioritized it.
- **Idea-evolution mid-analysis.** A clean "the idea materially changed — re-anchor and note the pivot" mechanism for mid-run reshapes (a sharper wedge, a segment / form-factor shift in 03/07). v2.0's pivot-as-re-brief covers the *different-idea* case; this is the lighter in-place re-anchor it doesn't.

These are tracked here as roadmap items, not open defects.
