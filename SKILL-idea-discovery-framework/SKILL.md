---
name: idea-discovery
description: Use this skill when the user wants to evaluate a product idea for commercial viability and solo buildability. Triggers include any request to "run discovery on" an idea, "evaluate" an idea, work through an `00-brief.md` file, or fill in sections numbered 01–09 in a project folder. The skill produces a structured, multi-section analysis culminating in a kill/proceed decision. Do not use this skill for execution planning, roadmapping, or building products that have already been greenlit — only for the discovery phase itself.
---

# Idea Discovery Skill

## What this skill does

Runs a structured discovery process to evaluate whether a product idea is worth pursuing. Produces a 9-section analysis ending in a kill/proceed decision, with explicit reasoning the user can review and challenge.

### How to start

When invoked, the user provides a filled-in brief (pasted or attached in chat).

1. Read the brief fully.
2. Derive the folder name from the brief's "Idea name" field, converted to kebab-case (e.g., "Fandango Colombia" → `fandango-colombia`).
3. Confirm the derived folder name with the user in a single line. Example: "Creating folder `idea-discovery-workspace/projects/fandango-colombia/` and saving the brief as `00-brief.md` — proceed, or would you like a different folder name?" If the user proposes an alternative, use that.
4. Create the folder (if it doesn't already exist) and save the brief as `00-brief.md` inside it.
5. Confirm you understand:
   - The idea
   - The primary market and market expansion question
   - The solution hypothesis (or whether form factor is deferred to analysis)
   - Any idea-specific depth or focus overrides
   - The runway, if the brief gives one (capital available for this idea; sections 07/08 compare the initial investment and cumulative capital against it)
   - The run mode (checkpoint or autonomous — see "Run mode"; defaults to autonomous if the brief doesn't set it)
6. State the active project folder explicitly (e.g., "Active project folder: `idea-discovery-workspace/projects/fandango-colombia/`"). All section outputs (`01-problem-and-user.md` through `09-decision.md`) will be saved to this folder as the framework progresses.
7. Begin section 01.

## Form-factor handling (before section 1)

Read the solution hypothesis field in the brief.

- If the user named a specific form factor (e.g., "agent," "web app," "marketplace"): acknowledge it explicitly, flag that it will be actively challenged in section 3 (not accepted as given), and proceed. Do not require pre-justification.
- If the user wrote "evaluate form factor as part of analysis" or equivalent: confirm that section 3 will generate and evaluate candidate form factors from scratch.
- If the field is missing or unclear: ask the user before proceeding.

Form-factor evaluation is not a gate to starting analysis — it's a commitment to actively challenge the assumption in section 3, where the analytical context exists to do it well.

## Required documentation in every section file

Every populated section `.md` file in the project folder must contain four documented parts, in this order, regardless of section content or recommendation:

1. **Analysis** — the actual section content, following the section template's prompts.
2. **Recommendation** — proceed to next section, or kill (with type of kill if applicable, e.g., "kill — compliance gate").
3. **Rationale** — the reasoning that connects the analysis to the recommendation. Explicit, not implied.
4. **Challenge pass** — the structured falsification exercise (see "Challenge pass" section below), with its findings documented even if they led to no changes.

All four parts are mandatory. A section file is not complete until all four are present and visible in the file itself. The user must be able to open any section file at any time and see all four parts — they are not transient chat content, they are part of the artifact.

## Run mode

The framework is **autonomy-first**: it is built to run end-to-end without a human in the loop, and its mechanical rules (vetoes, the placement demotions, conviction-gated kill confirmation) are designed to hold autonomously. The brief's **run-mode field** selects the mode for each evaluation; if it isn't set, the run is autonomous.

- **Autonomous mode** (the default) runs all sections end-to-end without intermediate pauses, surfacing the complete populated project folder at the end. Kills auto-confirm at High/Medium conviction and escalate only on low-conviction (or the section-09 contradiction) — see "Kill confirmation" below.
- **Checkpoint mode** (set `run mode: checkpoint` in the brief) pauses after each section: write the section file (all four required parts), surface one checkpoint presenting the recommendation, rationale, and challenge-pass summary together, and wait for confirmation before the next section. If the user requests revisions, revise (preserving the four-part structure) and re-surface.

In every mode, each section file is written with all four required parts.

### Kill confirmation (conviction-gated)

A kill — at any gate or the matrix — **auto-confirms in autonomous mode unless the validation layer fires on it**: if a decision-critical claim driving the kill is Low conviction, the kill **escalates to the human** (validate-or-accept) before it stands; High/Medium-conviction kills proceed without a pause. In checkpoint mode, all kills pause. The section-09 high-commercial / weak-financial contradiction is a mandatory escalation even in autonomous mode (a genuine ambiguity, not a kill). Every kill still carries the challenge pass applied to the kill itself (see `rubric.md`, "The kill model").

## Standing habits (apply throughout every section)

**Generate alternatives.** For every recommendation, generate at least 3 alternatives before settling on one. Show the alternatives considered, not just the winner. If you only see one option, you haven't looked hard enough — keep going.

**Falsify first answers.** When your first answer to a question feels obvious, treat that as a signal to challenge it. Actively search for evidence the answer is wrong before accepting it. Ask: what would make this wrong? What assumption am I making? What would a skeptic say?

**Avoid US/global defaults.** The brief specifies the target market. Apply a local lens to that market: identify local incumbents, substitutes, payment infrastructure, trust signals, dominant channels, language/content gaps, regulatory bodies, cultural patterns around the specific painpoint. Cite local sources where possible.

**Name comparables specifically.** "Like Fandango" is not analysis. *Fandango operates in market X under conditions Y; in target market Z those conditions are A* is analysis.

**Conviction labels everywhere.** Apply H/M/L conviction labels to any judgment call, quantitative estimate, market assertion, or competitive claim — not just rubric scores.
- **High:** backed by external evidence (interviews, primary data, market research).
- **Medium:** backed by analogous evidence (similar products' performance, indirect signals).
- **Low:** your own reasoning, no external validation yet.

A Low conviction label is not a problem — it's an honest signal of where research is needed. Do not inflate conviction to seem more decisive.

**Validate before deciding (the validation layer).** Before any proceed or kill is finalized, identify the decision-critical low-conviction claims — the load-bearing ones that would flip the decision if wrong — and either validate them or explicitly record them as accepted risk. This applies symmetrically to proceeds and kills, and gates only the load-bearing items, not every low-conviction label. (Full rule in `rubric.md`.)

**Surface questions, don't speculate.** When you're unsure whether to go deeper on something, ask the user rather than burning context on speculative depth. Cheap to ask, expensive to over-research.

**Honor brief overrides.** When the brief specifies a depth or focus override for a section, acknowledge it at the top of that section's output (e.g., "Per the brief, going deeper on regulatory analysis for this idea") so the override is visibly respected.

## Depth calibration

Match analysis depth to the decision being made. Discovery is meant to filter ideas, not produce business plans. For each section, aim for: enough depth to make the kill/proceed decision with reasonable confidence, no more. If a section is producing more than ~600–800 words of substantive content (not counting templates or headers), check whether you're optimizing past the decision threshold — and either tighten or surface a question to the user.

Default depth heuristics (override conditions noted):
- Market analysis: 3–5 incumbents named and characterized. Expand if the market is highly fragmented with no clear leaders.
- Competitive analysis: 3–4 dimensions that matter most for differentiation. Avoid full feature matrices.
- Financial projections: order-of-magnitude correctness. Conservative/base/optimistic each get one paragraph plus a small table.
- Risk & compliance: identify gates and ballparks, not legal opinions.

The brief may override these defaults for a specific idea. Honor those overrides.

## Output format

Section files are markdown, and the reasoning stays in **prose** — the right default for these judgment-heavy sections. But where a section's output is *natively tabular or visual*, a table or a simple visual carries it better than prose and is welcome:

- **Section 08** — the multi-year, multi-scenario projection should be a **structured table** (years × scenarios, with the cumulative-capital row) plus a short prose summary (see template 08).
- **Section 09** — include a **score table** (dimension | score | conviction) and a **simple 2×2 matrix visual** with the idea's position marked (see template 09).
- Elsewhere a small table is fine where the data is genuinely tabular (e.g., section 02's incumbent comparison or bottom-up SOM).

This is permission, not a mandate — do not force a table into every section, and keep the analysis itself in prose. Heavier artifacts (a spreadsheet financial model, a slide deck) are out of scope for discovery; they belong to post-decision execution.

## Deep research escalation (standing protocol)

A few sections warrant deep research — structured multi-source investigation beyond ordinary web search. The *triggers* are section-specific and listed in each template's research subsection. The *escalation protocol* is the same everywhere and lives here so the templates don't restate it:

When deep research appears warranted, surface to the user — *"I think deep research is warranted here because [specific reason] — proceed?"* — and wait for explicit confirmation. Do not run deep research without it. If the user declines, proceed with regular web search and note the analytical-depth limitation in the section output.

## Section flow

Run sections in order. Each section is a separate file in the project folder, named to match the template in `templates/`.

1. `01-problem-and-user.md`
2. `02-market-and-competitive.md`
3. `03-form-factor-and-differentiation.md`
4. `04-risk-and-compliance.md`
5. `05-business-model.md`
6. `06-solo-buildability.md`
7. `07-investment-and-GTM.md`
8. `08-financial-projections.md`
9. `09-decision.md`

For each section:
1. Open the corresponding template in `templates/`.
2. Follow the section-specific prompts in that template.
3. Apply the standing habits above.
4. Write the populated section to the project folder with all four required parts documented (Analysis, Recommendation, Rationale, Challenge pass).
5. In checkpoint mode, surface to the user and wait for confirmation before moving on.

## Upstream/downstream dependencies (standing rule)

Each section template lists what later sections consume from it. The discipline is universal: if a downstream section cannot draw on an upstream section's outputs as expected — e.g., a target-user definition too vague for section 02 to size a SOM — that is a signal to revisit the upstream section before continuing, not to proceed with weaker downstream analysis. Templates list their specific consumption mappings; this standing rule is why those mappings matter.

## Challenge pass (run at the end of every section)

Before finalizing any section, run a structured devil's advocate pass. The challenge pass is direction-agnostic: it applies whether the section concludes with a proceed or a kill recommendation. Whatever the section concluded, the falsification questions try to break it.

Standard questions:
- What's the strongest argument this analysis is wrong?
- What did I assume that I should have investigated?
- What would a skeptical investor say after reading this?
- Is there a non-obvious option I dismissed too quickly?

Document the findings in the section file under the "Challenge pass" heading, even if they led to no changes. If changes were made based on the challenge pass, note what changed and why.

Section templates may include additional, section-specific falsification questions on top of these four. Apply both layers.

## The kill model (where the analysis can stop)

A kill is produced by a **veto** (a dealbreaker) or by the **matrix** (death by mediocrity). This section is the **canonical statement of each stop-point's firing conditions**; the veto *families*, the *routing*, and the matrix kill live in `rubric.md` ("The kill model"), which points back to the conditions here. Section templates *apply* these gates — and reference these conditions rather than restating them. The stop-points, in firing order, named by what they test (not numbered):

- **Problem gate (01)** and **Market gate (02)** — *early-exits.* A Problem severity or Market size score of **0–2** is a fatal commercial veto: recommend the kill and stop, rather than running the remaining sections. The Market-size veto fires only after the make-money-threshold sanity-check confirms the SOM fails under every reasonable assumption (template 02). (Defensibility is **not** an early-exit — it's finalized at section 09.)
- **Structural gate (04)** — fires on **any** of three structural dealbreakers, each a *conclusion from* section 04's research (a low-conviction finding routes through the validation layer before the kill stands):
  - **Legal / regulatory blocked** — required licensing is obtainable by *no one* building this (or not obtainable by the user with no partner able to supply it); **or** the activity is prohibited in the target market; **or** compliance requires a structure that cannot exist here (an entity type that can't be formed, partnerships unavailable to new entrants); **or** compliance cost is *obviously disproportionate* to any plausible business value — so high that no section-05 model could justify it, and visible without 05/08 needing to quantify value (if quantifying value is needed to make the call, this sub-condition does *not* fire — continue to section 05).
  - **Data access blocked** — the data / API / partnership the idea needs is obtainable by *no one* building this (not merely hard for this user; the "can *this* user obtain it" question is section 06's).
  - **Capability infeasible** — the idea's core function cannot be performed to an adequate standard by *anyone* with current technology.
- **Business-model gate (05)** — fires on either of two causes, which route differently: **(a) no model survives the legal envelope** (all candidate models are prohibited or require licensing the user can't obtain), or **(b) no model has viable economics** — the **Monetization 0–2** commercial veto (all viable candidates have negative unit margins at any plausible scale).
- **GTM gate (07)** — no go-to-market strategy produces CAC recoverable within the model's plausible payback window, **after the Step-2 adjustment attempt** (template 07 holds the payback-window benchmarks and the adjustment menu); skip section 08.
- **Section 09** — the **Defensibility late veto** (scored provisionally at 03, finalized at 09 once the 04/05 moats are known; a veto if still **0–2**) and the **matrix decision** (commercial average **< 6**, or a placement demotion — see `rubric.md`).

At any stop-point, Claude recommends the kill with explicit rationale **and the challenge pass applied to the kill itself** (what would make the kill wrong — missed workarounds, partnership structures, segment pivots). Commercial vetoes route to kill or a *pivot* (a re-brief); structural vetoes route to *partner / kill / park* (see `rubric.md`). The kill is **confirmed per the conviction-gated rule** (auto-confirmed at High/Medium conviction in autonomous mode, escalated if low-conviction; always paused in checkpoint mode — see "Kill confirmation" above).

Once confirmed, Claude writes `09-decision.md` documenting the stop-point, the rationale, the challenge pass applied to the kill, and which sections were not run. This applies in both modes. Killing an idea early is a valid and valuable outcome — discovery succeeds when it accurately filters ideas, whether the outcome is proceed or kill.

## Cross-idea calibration

Before finalizing section 9 (Decision), check whether the workspace's `projects/` folder holds prior evaluations (other than the current idea). If it does:
- Identify the 3 closest prior evaluations by domain or shape (their `09-decision.md` files hold the score records).
- Compare this idea's scores against them. Are scores internally consistent? Does this idea genuinely deserve a higher commercial score than [prior idea] given what was known then?
- If scores have drifted upward over time (everything starting to look like a 7), flag it explicitly.

If `projects/` holds no prior evaluations, skip this step — it activates as the portfolio grows.

## Scoring

See `rubric.md` for the full scoring system. Summary:
- **Commercial score** (the primary axis): four equally-weighted dimensions — problem severity (01), market size (02), defensibility (03, finalized at 09), monetization clarity (05) — combined as a simple average. No caps: a fatal 0–2 dimension is a *veto*, and two-or-more weak (3–4) dimensions demote placement. Data access is no longer a commercial dimension (it's a structural check in section 04).
- **Solo-buildability score** (the second axis): independently scored; defines build strategy, not kill criterion.
- **Agent-fit** (qualitative, descriptive only — not in the matrix): captured as a short note.

Plot commercial × solo-buildability on a 2×2. The matrix drives the decision. Agent-fit is descriptive only: it informs execution planning after a proceed decision and provides portfolio-level visibility — it does not move matrix positions, override kills, or break ties between ideas (per `rubric.md`).

## Framework version

Current framework version: **2.0** — the kill & score model redesign (vetoes vs. scores, four-dimension arithmetic average, function-named gates, conviction-gated kills, autonomy-first). Section 09 records this version in each evaluation's portfolio metadata, so evaluations stay comparable across framework changes.

## Output

The final artifact is the populated project folder, containing one `.md` file per section completed.

- For ideas that complete the full analysis: all nine section files are present, and `09-decision.md` serves as the executive summary — readable on its own, with the other sections as supporting detail.
- For ideas killed at a gate: the project folder contains the sections completed up to and including the kill point, plus `09-decision.md` documenting the kill recommendation, the rationale, the challenge pass output applied to the kill, and which sections were not run. `09-decision.md` is still the executive summary in this case — it just summarizes a kill instead of a proceed.

`09-decision.md` is always written, regardless of outcome. Killed ideas produce a kill decision file, not the absence of one.