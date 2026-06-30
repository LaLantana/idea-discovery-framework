# Template: 09 — Decision

## Purpose of this section in the framework

Section 09 is the framework's culminating section. It produces the final decision document — the section file that captures the outcome of the discovery work and tells the user what to do with the idea.

Unlike sections 01–08, section 09 does NOT produce new analysis. It synthesizes the analytical work from prior sections into:
- The 2×2 matrix decision (commercial × solo-buildability)
- The strategic interpretation of the matrix placement given the financial picture from section 08
- The final decision content for the user
- A portfolio-level record of the evaluation

The section file IS the decision document. The four required parts (Analysis, Recommendation, Rationale, Challenge pass) map onto the decision document's structure. Header material (idea name, date, market, run configuration) sits at the top of the section file; Portfolio metadata sits at the bottom.

**On killed ideas:** if a veto fired anywhere upstream — an **early-exit** at section 01 (Problem) or 02 (Market), or a **gate** at section 04 (Structural), 05 (Business-model), or 07 (GTM) — section 09 still runs. Its job in that case is to produce the kill decision document — documenting which veto fired, why, what was considered, and any partial findings worth preserving for portfolio learning. (The **Defensibility late veto** is evaluated *inside* section 09, at Task 1, since it's finalized here.) The structure for a killed idea is different from a pursued idea, but both are produced as section 09 output.

## Brief fields relevant to this section

Before starting the synthesis work, draw on these fields from `00-brief.md`:

- **Idea name and one-liner:** used in the section file's header.
- **Primary market:** referenced in the document header and may inform language in the rationale.
- **Make-money threshold:** already evaluated in section 08; referenced here for completeness in the decision document.
- **Learning value field:** relevant for surfacing the learning-project override in Task 4 if the matrix produces a kill in the low commercial / high solo-buildability quadrant.
- **Run configuration:** whether this section runs in autonomous mode (the default) or checkpoint mode. Note: even in autonomous mode, the high-commercial + weak-financial-picture contradiction in Task 5 pauses for user input (a mandatory escalation), and any kill resting on decision-critical low-conviction evidence escalates per the conviction-gated rule.
- **Depth overrides (if any):** acknowledge at the top of the section file. Common overrides: "produce a brief decision document only — I'll review the analysis sections separately," "produce the full document including detailed rationale," "skip the portfolio metadata — I'm not tracking portfolio yet."

If any of these fields are missing or unclear, surface the gap to the user before starting synthesis work.

## Research activated in this section

No new research. Section 09 synthesizes existing analysis from sections 01–08.

## Analytical work for this section

These tasks together produce the **Analysis** portion of the section file. The Recommendation, Rationale, and Challenge pass are produced after the analytical work, drawing on it.

Section 09's "analysis" is synthesis work — assembling prior sections' outputs into the matrix decision and decision document.

If a veto fired upstream (an early-exit at 01/02, or a gate at 04/05/07), section 09 follows a kill-specific path. Tasks 1–3 still run (they characterize what was learned before the kill); Tasks 4–5 are replaced by a single kill-decision task; Task 6 produces a kill-specific document structure. (A Defensibility late veto is decided within Task 1 below — it is not an upstream kill.)

### Task 1: Finalize Defensibility, then assemble the commercial score

**First, finalize the provisional Defensibility score (and apply the late veto).** Section 03 scored Defensibility *provisionally*, before downstream moats were known. Reconcile that provisional score against moats surfaced in section 04 (regulatory moats) and section 05 (data / network / business-model moats): if those raise the real defensibility, revise the score up and note why; if nothing changes it, the provisional score stands. **Then apply the Defensibility late veto:** if the *finalized* score is **0–2**, this is a fatal commercial veto — route it to a kill (or pivot) per `rubric.md` and follow the kill path (Task 6 alternate), exactly as an upstream veto would. Document the provisional→final reconciliation explicitly.

**Then assemble the commercial score from the four dimensions** (data access is no longer a commercial dimension — it's a structural veto in section 04):
- **Problem severity** (scored in section 01)
- **Market size** (scored in section 02)
- **Defensibility** (finalized just above, from section 03's provisional score)
- **Monetization clarity** (scored in section 05)

**Aggregation — a plain arithmetic average, no caps:** the four dimensions are equally weighted; the overall commercial score is the simple average (sum ÷ 4). There are **no cap rules** — they have been removed. Because a 0–2 on any dimension is a *veto* (handled at its section, or just above for Defensibility), every dimension feeding this average is already **≥ 3**; there is no fatal flaw left for an average to hide, which is the only thing caps existed to prevent.

**Apply the "weak on multiple fronts" placement demotion (mechanical):** if **two or more** of the four dimensions are **3–4**, place the idea as **low-commercial regardless of the average**. This demotes *placement*, not the score — the commercial score stays the honest average; record the demotion and which dimensions triggered it. (This is parallel to the conviction-at-threshold demotion in Task 4.)

Document:
- Each dimension's score with conviction label (and, for Defensibility, the provisional→final reconciliation).
- The arithmetic average.
- Whether the "weak on multiple fronts" demotion fired, and which dimensions triggered it.
- The final commercial score (0–10) with overall conviction.

**Overall conviction is the lowest conviction among the four dimensions** (the weakest evidence governs). If any dimension is L conviction, the overall score reflects that — note the L-conviction dimension(s) explicitly in the score record so the user can see which the caveat applies to. (This feeds both the 6/L→low matrix rule in Task 4 and the validation layer.)

### Task 2: Retrieve the solo-buildability score

Pull the Solo-buildability score from section 06 with its conviction label. No assembly needed — section 06 produced a single score on the 0–10 scale.

Document:
- The Solo-buildability score.
- The conviction label.
- Any user-noted profile adjustments that were applied at the section 06 checkpoint.

### Task 3: Retrieve the financial picture

Pull the synthesized financial picture from section 08:
- The threshold comparison (scenario, timing, magnitude, conviction, key drivers).
- The cumulative capital required.
- The conviction picture overall.
- The key risks.

If the GTM gate fired in section 07, section 08 was skipped. In that case, document the GTM gate finding and note that no financial projection exists for this idea.

If section 08 ran, document its synthesized financial picture in compressed form. The decision document references this; the full picture lives in section 08's file.

### Task 4: Apply the 2×2 matrix

Apply the matrix using commercial score (X-axis) and solo-buildability score (Y-axis). An idea only reaches the matrix if it has **survived every veto** — the early-exits (01/02), the Structural / Business-model / GTM gates (04/05/07), and the Defensibility late veto finalized in Task 1. Use the commercial **placement** from Task 1: if the "weak on multiple fronts" demotion fired, the idea is placed low-commercial regardless of its average.

**Threshold for each axis: 6/10** (per `rubric.md`'s matrix section).

**Matrix quadrants:**

- **High commercial (≥6) + high solo-buildability (≥6):** "Pursue immediately." The standard go path for a commercially viable, solo-executable idea. "Immediately" describes timing relative to other quadrants — this idea is ready to act on now; the user retains sequencing judgment.

- **High commercial (≥6) + low solo-buildability (≤5):** "Pursue with partnership strategy." The idea is worth pursuing but execution requires partnership(s) per section 06.

- **Low commercial (≤5) + high solo-buildability (≥6):** "Kill, with optional learning-project override." The idea is buildable but doesn't justify the build commercially. The default is kill. Before the kill is finalized, the user may exercise an optional learning-project override — see "The learning-project override" below.

- **Low commercial (≤5) + low solo-buildability (≤5):** "Kill." The idea is neither commercially viable nor easily executable. No options are surfaced — both axes are weak.

**Threshold ties:** if commercial score is exactly 6.0, the conviction label may break the tie. L conviction at 6.0 is treated as below the threshold (low commercial); M and H conviction at 6.0 are treated as at the threshold (high commercial). Same rule applies to solo-buildability. This rule comes from `rubric.md`'s matrix section (conviction at the threshold breaks ties downward).

**The learning-project override:**

When the matrix produces a kill in this quadrant, the user may exercise one optional override before the kill is finalized: **pursue as learning project.** This option is surfaced only when the brief's learning value field indicates a learning interest in the relevant skill area. When exercised, the user explicitly chooses to pursue the idea with no expectation of revenue. The framework's output in this case is *not* a green light for commercial pursuit — it is explicit acknowledgment that the user is investing time in skill-building, with no expectation of return.

If the override is not exercised (or not available because the brief indicates no relevant learning interest), the kill stands. The decision document may note related ideas worth evaluating as separate next briefs where the framework's analysis points at such adjacencies — different segment, different audience, different scope. These are portfolio notes for the user's consideration, not a framework path; pursuing any of them means starting a fresh evaluation with a modified brief.

The learning-project override applies only to this quadrant. The low commercial / low solo-buildability quadrant has no override (the idea isn't buildable, so skill-building isn't meaningful). Gate-driven kills also have no override (structural unviability has been established).

Document:
- The commercial score with conviction.
- The solo-buildability score with conviction.
- The matrix quadrant placement.
- Any tie-breaking applied.
- For low commercial / high solo-buildability quadrant: whether the learning-project override was surfaced (i.e., whether the brief indicated relevant learning interest) and the user's choice if it was.

**Output format — score table + matrix visual.** Present the scores as a **score table** (dimension | score | conviction, with the commercial average and the "weak on multiple fronts" demotion flag if it fired), and include a **simple 2×2 matrix visual** (markdown or ASCII) with the idea's position marked on the commercial × solo-buildability axes. Keep the reasoning in prose; the table and the visual make the verdict legible at a glance (per `SKILL.md`'s output-format note and `rubric.md`'s matrix section).

### Task 5: Apply the financial picture as strategic context

The matrix placement gives the headline decision. The financial picture from section 08 modifies the interpretation:

- **Strong financial picture** (meets threshold in expected case, robust scenario range, H/M conviction): the matrix placement is well-supported.
- **Marginal financial picture** (meets threshold only in optimistic case, narrow scenario range, L conviction): the matrix placement is supported but fragile. Pursue paths come with the caveat "this depends on optimistic execution."
- **Weak financial picture** (doesn't meet threshold, or meets only at threshold itself with breakage risks): the matrix placement may need revision. See "Handling high commercial + weak financial picture" below.
- **No financial picture** (the GTM gate fired): the idea is in the kill path regardless of matrix placement.

**Handling high commercial + weak financial picture:**

If the commercial score is ≥6 (high) but the financial picture is weak (doesn't meet threshold, or meets only marginally), the matrix and the financial picture are in tension. This is a real contradiction that should not be papered over.

When this contradiction surfaces:

1. **Surface the contradiction to the user explicitly,** even in autonomous mode. This is one of the cases where autonomous mode pauses for user input — the contradiction is too consequential to resolve without user judgment.

2. **Present three options to the user:**
   - **Trust the matrix placement (commercial score):** proceed with the pursue path, treating the weak financial picture as a known risk to monitor.
   - **Trust the financial picture:** treat the idea as low-commercial despite the score, moving it to the corresponding kill quadrant (low/high or low/low based on the solo-buildability score, with override availability per Task 4).
   - **Revisit the analysis:** the contradiction suggests something in sections 01–05's dimension scoring or section 08's projections may need re-examination. Pause the framework, identify the most likely source of error, and revisit that section.

3. **Document the user's choice** and the reasoning in the decision document's rationale section.

The matrix gives the quadrant; the financial picture gives the conviction in that placement. When they contradict, the user decides which to trust — but the contradiction itself must be surfaced, not smoothed over.

Document:
- How the financial picture supports or qualifies the matrix placement.
- Any contradictions surfaced and how they were resolved.
- The user's choice if the high commercial + weak financial contradiction fired.

### Task 6 (standard path): Compose the decision document

The section file IS the decision document. It must be readable as a standalone — the user should understand the decision, the reasoning, and the next steps without re-reading sections 01–08.

**The section file structure (which becomes the document structure):**

**Header (top of section file, before the four required parts):**
- Idea name and one-liner (from brief)
- Date of evaluation
- Primary market
- Run configuration (checkpoint/autonomous mode)
- Section completion status (which sections ran, any sections skipped due to gates)

**Analysis section (first of the four required parts):**
- The matrix application work from Tasks 1–5 — commercial score assembly, solo-buildability retrieval, financial picture retrieval, matrix placement, strategic context from financial picture.

**Recommendation section (second of the four required parts):**
- The matrix placement and headline recommendation (pursue immediately / pursue with partnership / pursue as learning project / kill).
- For the low commercial / high solo-buildability quadrant: whether the learning-project override was exercised by the user, or whether the kill stands.
- Whether the high commercial + weak financial contradiction was resolved (and how).
- **Action subsection:** the specific actions tied to the recommendation:
  - **If pursue immediately:** the recommended next steps (build the MVP, key risks to monitor, the make-money threshold check-in points).
  - **If pursue with partnership:** the partnership(s) needed, what to look for in candidates, timeline considerations from section 06's partnership requirements detail.
  - **If pursue as learning project (user-elected from the low commercial / high solo-buildability quadrant):** confirmation that the framework's output is *not* a green light for commercial pursuit, the specific skill areas being built, the time investment envelope the user is committing to, and the milestone at which the user re-evaluates whether continuing makes sense.
  - **If kill, matrix-driven, low commercial / high solo-buildability, no user override:** confirmation of the kill decision and rationale. Document that the learning-project override was either not surfaced (no relevant learning interest in brief) or was surfaced and declined. Where the framework's analysis points at adjacent ideas worth evaluating as separate next briefs, name those directions specifically (e.g., "consider evaluating the upmarket B2B segment as a separate idea — willingness-to-pay benchmarks are stronger there" or "consider evaluating a different geographic market where the regulatory picture is simpler"). These are portfolio notes for the user's consideration, not a framework path.
  - **If kill, matrix-driven, low commercial / low solo-buildability:** confirmation of the kill decision and rationale. No options surfaced — both axes are weak.

**Rationale section (third of the four required parts):**
- One-paragraph summary of why this decision was reached.
- Commercial score drivers (which dimensions were strong/weak, what drove the overall score).
- Solo-buildability drivers (what makes this buildable or not).
- Financial picture drivers (what determines the threshold story).
- Any contradictions or qualifications surfaced in Task 5.
- **Risks subsection:** the key risks identified in section 08 with monitorability classification (monitorable vs. structural), the L-conviction findings that the user should treat as open questions, any partnership-realism uncertainty if pursuing with partnership.

**Challenge pass section (fourth of the four required parts):**
- The standard four falsification questions plus section-specific questions (see Challenge pass subsection below).
- For kill recommendations, the challenge pass applies to the kill itself.

**Portfolio metadata (bottom of section file, after the four required parts):**
- The full score record (all dimension scores with conviction, the overall commercial score, the solo-buildability score).
- The matrix placement.
- The final decision (pursue immediately / pursue with partnership / pursue as learning project / kill).
- The date of evaluation.
- The framework version under which this evaluation was run (stated in `SKILL.md`).
- A reference to the workspace folder containing the full section files.

The decision document is what the user will reference downstream. Its job is to be honest, complete, and useful — not to be enthusiastic about pursue paths or critical about kill paths. The framework's job is to surface what's true; the document's job is to capture that.

### Task 6 (alternate — kill path): Compose the kill decision document

If a veto fired upstream (an early-exit at 01/02, or a gate at 04/05/07), or the Defensibility late veto fired in Task 1, the document structure is different. The section file structure:

**Header (same as standard):** idea name and one-liner, date, primary market, run configuration, section completion status (with explicit note of which sections were skipped due to which veto).

**Analysis section (first of the four required parts):**
- The kill-specific synthesis work — partial commercial scores for dimensions that were assigned before the kill, the veto that fired and the finding that triggered it, the synthesized picture from whichever section the kill was triggered in.

**Recommendation section (second of the four required parts):**
- The kill decision with which veto fired.
- The specific finding that triggered the veto.
- Confirmation that the kill was confirmed per the conviction-gated rule (auto-confirmed at High/Medium conviction in autonomous mode; escalated to the user if it rested on low-conviction evidence; paused in checkpoint mode).
- **Override availability follows buildability** (per `rubric.md`):
  - **Structural-veto kills** (section 04 — legal / data / capability): **no override.** The idea can't be built or operated, so skill-building isn't meaningful.
  - **Commercial-veto kills** (Problem 01, Market 02, Monetization 05, or the Defensibility late veto): the idea may be *buildable* but isn't *monetizable*. **Only if the brief's learning field is filled**, surface the **learning-project footnote** — the user may opt to run **section 06 only** to assess buildability, then decide whether to pursue purely as a skill-building project (no expectation of revenue). If the learning field is blank, the kill stands with no override.

**Rationale section (third of the four required parts):**
- The challenge pass output applied to the kill (from whichever section the kill was triggered in, since that's where the challenge pass for the kill was originally documented).
- The specific reasoning grounded in the veto's conditions.
- **What was learned subsection:** partial findings from sections that ran, score dimensions assigned before the kill (these may inform future evaluations of related ideas), the synthesized regulatory / business model / GTM picture from whichever section the kill was triggered in.

**Challenge pass section (fourth of the four required parts):**
- The standard four falsification questions plus section-specific questions, all applied to the kill itself.

**Portfolio metadata (same as standard):** full score record (including partial scores for dimensions that were assigned), the veto that fired, the kill decision, date, workspace reference.

The kill document preserves the learning from the evaluation even when the idea isn't pursued. Future related ideas can reference this document for context.

## Scoring activated in this section

Section 09 does not score new dimensions. It assembles the overall commercial score from sections 01–05's dimension scores per Task 1.

## Section-specific content for the four required parts

The four required parts (Analysis, Recommendation, Rationale, Challenge pass) are mandatory in the section file per `SKILL.md`. Below is what each part contains for section 09 specifically.

### Analysis

The matrix application work from Tasks 1–5 (standard path) or the kill-specific synthesis work (kill path).

For the standard path, subsections in order: Commercial score assembly, Solo-buildability retrieval, Financial picture retrieval, Matrix application, Strategic context from financial picture.

For the kill path, subsections in order: Pre-kill score assembly (for dimensions that were assigned), Gate finding and trigger, Kill rationale synthesis.

### Recommendation

The matrix placement and headline recommendation, plus the Action subsection covering specific actions tied to the recommendation.

For the low commercial / high solo-buildability quadrant, whether the learning-project override was surfaced and the user's choice are documented here.

For kill paths (matrix-driven or gate-driven), the kill confirmation.

### Rationale

The reasoning behind the decision, with the Risks subsection (monitorability classification, L-conviction findings, partnership uncertainty).

For kill paths, the challenge pass output applied to the kill and the What was learned subsection.

### Challenge pass

The standard four falsification questions from `SKILL.md` apply, plus the section-specific questions below.

For kill recommendations, the challenge pass is applied to the kill itself — the questions ask what would make the kill recommendation wrong, not just what would make the synthesis wrong.

## Challenge pass: section-specific falsification questions

In addition to the standard four questions from `SKILL.md`, apply these to the decision synthesis:

- **Score-honesty check:** is the commercial score a faithful arithmetic average of the four dimensions, with no fatal flaw hidden? Because 0–2 dimensions are vetoes (not averaged), every dimension here should be ≥ 3 — check that no genuine 0–2 was softened to a 3 to dodge a veto. Did the "weak on multiple fronts" demotion fire when two or more dimensions were 3–4? Was the Defensibility provisional→final reconciliation done honestly, not inflated by speculative downstream moats? Was the L-conviction caveat surfaced when any of the four dimensions is L conviction, and is overall conviction the lowest of the four — not labeled higher than honest?

- **Matrix-application-rigor check:** is the matrix placement honest about borderline cases? Threshold ties at 6.0 should apply the conviction rule per `rubric.md`'s matrix section — only L conviction at 6.0 breaks the tie downward. And if the "weak on multiple fronts" demotion fired in Task 1 (two or more dimensions at 3–4), the idea is placed low-commercial regardless of its average — check that demotion was applied, and not over-applied. Check that any borderline placement applied the rules correctly.

- **Financial-contradiction check:** does the financial picture contradict the matrix placement? A high commercial score with a weak financial picture is a contradiction that should be surfaced and resolved through user input, not smoothed over. If the contradiction was present but not surfaced, the synthesis is incomplete.

- **Learning-exception-rigor check:** if the learning-project override was surfaced and exercised, is it actually warranted by the brief's stated learning interest, or is it being used to rescue a marginal commercial idea? The override applies only when the brief indicates a learning interest in the relevant skill area, and the framework's output if exercised is explicit acknowledgment of skill-building, not commercial pursuit.

- **Document-honesty check:** does the decision document accurately represent the analysis, or has it been tilted toward the recommended path? Pursue documents should surface risks and L-conviction findings honestly, not bury them in the Risks subsection while the rest of the document reads enthusiastically. Kill documents should preserve what was learned, not just document the kill in a way that closes the case.

Document the findings under the Challenge pass heading even if no changes were made to the synthesis. If changes were made, note what changed and why.

## Depth calibration for this section

Variable weight depending on path. Standard document (pursue immediately / pursue with partnership / pursue as learning project) is moderately heavy — synthesis plus complete document structure. Kill document is lighter — synthesis is partial since gate-fired sections don't have full analysis.

Normal depth range: ~800–1,200 words for the section file. The total length depends on the path — pursue paths with full action sections will be longer; gate-driven kills with skipped sections will be shorter.

`SKILL.md`'s general ~600–800 word check-in threshold applies as a self-check signal. At that point, confirm the additional depth is contributing to the decision document's usefulness, not optimizing past what the user needs to act on the decision.

Signs the section is too thin:
- Matrix application reduced to "high/high, pursue" without strategic context from the financial picture.
- Financial picture not integrated into the recommendation.
- Risks subsection missing or reduced to a single sentence.
- Action subsection generic rather than specific to the recommendation type (e.g., "follow up on partnerships" instead of naming the partnership types from section 06).
- For low commercial / high solo-buildability quadrant: learning-project override not surfaced when the brief indicates a relevant learning interest, or surfaced without the implications spelled out.
- Portfolio metadata incomplete.

Signs the section is too thick:
- Re-deriving conclusions from sections 01–08 instead of summarizing them. The decision document references analysis; it doesn't re-do it.
- Restating dimension-by-dimension scoring at length instead of surfacing the drivers in one or two sentences.
- Over-engineering the action subsection into a project plan. The action subsection names next steps; it doesn't sequence them.
- Speculating about future framework evaluations or portfolio strategy rather than capturing this evaluation specifically.

If the brief specifies a depth override for this section, honor it and acknowledge it at the top of the section file.

## Downstream dependencies

Section 09 is the framework's terminal section. No downstream sections consume its output within the framework. The decision document is consumed by the user for action.

For portfolio-level use: the decision document's portfolio metadata section is what future evaluations reference when considering related ideas. The framework's portfolio metadata captures basic record-keeping fields (scores, matrix placement, decision, date, framework version, workspace reference).