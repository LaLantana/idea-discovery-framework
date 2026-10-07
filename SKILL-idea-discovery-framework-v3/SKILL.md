---
name: idea-discovery
description: Run the Idea Discovery Framework ONLY when the user explicitly asks to run it, by naming the skill or the framework (e.g., "run idea discovery", "run the framework on this", "/idea-discovery") or by attaching a filled-in 00-entry.md and asking to run it. Do NOT use it for exploratory questions, brainstorming, opinions on an idea or problem, market questions, or discussion or maintenance of the framework itself, even when they are about ideas or problems; answer those normally. When run, it researches a potential problem, defines the problem worth solving, generates and screens ideas, and evaluates up to three of them, ending in a verdict per idea.
---

<!-- v3 dry-run build (2026-10-06), installed for the dry runs. Built from idea-discovery-workspace/_v3-drafts/; edit the drafts, not this copy. -->

# Idea Discovery Skill

## What this skill does

Runs a **pre-evaluation** of a potential problem: whether, and how, a business might solve it. The process follows the double diamond:

| # | Section | Position | Temperament |
|---|---|---|---|
| 00 | Entry (written by the founder) | Entry point | — |
| 01 | Discover | 1st diamond, diverge | Generates |
| 02 | Define | 1st diamond, converge | Judges (no scores) |
| 03 | Brief (written by 02) | Midpoint | — |
| 04 | Ideation | 2nd diamond, diverge | Generates |
| 05 | Screen | 2nd diamond, diverge (light evaluation) | Judges (no scores) |
| 06–12 | Evaluation, per idea | 2nd diamond, diverge (evaluation) | Judges (scores) |
| 13 | Decision | Exit point | Judges |
| 14 | Run summary (written last) | After the exit point | Summarises (no judgement) |

Throughout, a "problem" includes a **desire**: something people want and cannot easily get, not only a pain.

The framework stops at the exit point; 14 only records how the run got there. Building, testing and iterating (the 2nd diamond's converge) are out of scope, and so is primary research, which needs a human, time and money.

### How to start

**Only on explicit request.** Start a run only when the founder has explicitly asked to run the framework: by naming it, or by attaching a filled-in entry and asking to run it. If this skill was loaded for anything else (an exploratory question, a brainstorm, a question about an idea, a market or this framework), do not start a run, create folders or write files. Answer the question normally, and if a run would help, offer it in one line.

When invoked, the founder provides a filled-in entry (pasted or attached in chat).

1. Read the entry fully. If the founder supplied an idea or a solution instead of a problem, restate it as the problem (or desire) it would answer, say so in one line, and carry the idea into 01's "Entry, ripped" as an assumption to test and into 04 as a candidate.
2. Derive the folder name from the entry's "Working name" field in kebab-case (e.g., "Restaurant staff turnover" → `restaurant-staff-turnover`).
3. Confirm the folder name with the founder in a single line, e.g.: "Creating `idea-discovery-workspace/projects/restaurant-staff-turnover/` and saving the entry as `00-entry.md`. Proceed, or would you prefer a different name?" Use the founder's alternative if one is given.
4. Create the folder (if it doesn't already exist) and save the entry as `00-entry.md`.
5. Confirm, in a few lines, that you understand the problem, any leads (stated as leads, not constraints), and the run mode (autonomous unless the founder asks for checkpoint mode).
6. State the active project folder, then begin 01.

## Section flow

Run the sections in order. Each section is one file, named to match its template in `templates/` (00's template is `00-entry-template.md`; the founder's filled-in file is `00-entry.md`).

**Problem level** (`projects/<problem-name>/`):
- `00-entry.md`
- `01-discover.md`
- `02-define.md`
- `03-brief.md`
- `04-ideation.md`
- `05-screen.md`

**Per selected idea** (`projects/<problem-name>/ideas/<idea-name>/`, one subfolder per idea that 05 selects; the idea name comes from the idea's card in 04):
- `06-problem-market-and-competitive.md`
- `07-form-factor-and-differentiation.md`
- `08-risk-and-compliance.md`
- `09-business-model.md`
- `10-solo-buildability.md`
- `11-investment-and-GTM.md`
- `12-financial-projections.md`

**Problem level, last:** `13-decision.md`, then `14-summary.md`, each written once for the whole problem.

When 05 selects more than one idea, evaluate them **one at a time**, completing an idea's 06–12 (or its kill) before starting the next, in the order 05 lists them. A killed idea does not stop the run; the next idea starts.

"Proceed to 13" and "early exit to 13" always mean: on to the next selected idea's 06, or to 13 after the last idea.

For each section:
1. Open its template in `templates/`.
2. Follow the template's prompts.
3. Apply the standing habits below.
4. Write the section file with its required parts (see "Required documentation").
5. In checkpoint mode, surface to the founder and wait for confirmation before moving on.

## Generating and judging

The two temperaments never share a section. The one exception is the narrow candidate sets named under "No alternatives after the screen" (07's and 11's), which those sections generate and then judge.
- **01 and 04 generate.** They do not score, rank, recommend a winner or kill.
- **02 and 05 judge without scores.** 02 always chooses one problem, even on weak evidence; 05 selects the ideas worth a full evaluation (at most three, possibly none).
- **06–13 judge with scores,** one idea at a time.
- **14 summarises** the run and adds no judgement.

**Nothing is scored before 06.** The problem is not scored in the first diamond. Problem severity is scored per idea in 06, against that idea's own target user.

**No alternatives after the screen.** Alternatives are generated once: problem framings in 01, ideas in 04, narrowed by 05. The evaluation (06–13) judges the idea it was handed. It never generates a different idea, segment, market, form factor or revenue model, and it never re-opens 01–05. If the evaluation finds the idea wrong, that is a finding against this idea; the alternatives already exist in 04 and in 13's list of flagged ideas. The only things generated inside the evaluation are those its templates name: 07's candidate differentiation hypotheses (sharpening this idea's edge) and 11's candidate go-to-market strategies (how to reach this idea's customers).

**Flagged, not run.** 02 may flag other strong opportunity areas, and 05 may flag ideas beyond those it selects. Flagged items are listed in 13 and run only if the founder chooses. Nothing is sent back or run automatically.
- Running a flagged **idea** adds an `ideas/<idea-name>/` subfolder to the same problem folder. Its handoff, threshold included, is written first as `ideas/<idea-name>/05-handoff.md`, using 05's handoff method; this completes 05's work for that idea and changes nothing 05 decided. 13 and 14 are then reissued with the idea added (an "added idea" amendment).
- Running a flagged **opportunity area** starts a new problem folder (`projects/<problem-name>-<area-name>/`). It links to the original run's 00 and 01 instead of copying or redoing them. Its 02 records that the founder picked this area from the original 02's flagged list, notes the original 01's date, and writes the new HMW question, target user and 03. From 04 on, the run is normal. Start it like any run, with the folder-name confirmation and the run mode (How to start, steps 3–6), reading the original 00 in place of a new entry. Its 02 carries forward the original run's other flagged areas, and an amendment-log entry in the original 13 points to the new folder.

## Required documentation in every section file

Every section file contains four documented parts, in this order:

1. **Analysis:** the section content, following the template.
2. **Recommendation:** proceed; a kill of the idea (with the kill type, e.g., "kill — Structural gate"); or a section-specific outcome: at 05, "no idea selected"; at 08 and 09, a veto routed to a partner, or at 09 to a different legal structure for the same model ("proceed with a partner" or "proceed with [structure]"); at 08, "park"; at 09, "early exit to 13 (locked average)"; at 13, each idea's verdict.
3. **Rationale:** the reasoning that connects the analysis to the recommendation, stated explicitly.
4. **Challenge pass:** see "Challenge pass" below, with its findings documented even if they led to no change.

**Diverge sections (01, 04)** adapt the parts: the Recommendation is always "proceed", and the challenge pass takes the diverge form.

**Handoff and record documents (00, 03, 14)** are exempt. 00 is written by the founder; 03 is written by 02 as the midpoint brief; 14 summarises the run and decides nothing. Their templates define their contents.

All parts must be visible in the file itself. They are part of the artifact, not chat content.

## Run mode

The framework is **autonomy-first**. Runs are **autonomous by default**: all sections run end-to-end without intermediate pauses other than those in "Pauses during a run", and the complete project folder is surfaced at the end.

**Checkpoint mode** is an opt-in that the founder requests when starting the run (there is no field for it in 00). It pauses after each section: write the section file with its required parts, surface the recommendation, rationale and challenge-pass summary together, and wait for confirmation. If the founder asks for revisions, revise and re-surface, but change a score only on new evidence or a misapplied anchor; otherwise record the founder's reading as a recorded dissent and leave the score. A kill escalation in checkpoint mode is folded into the section's pause, with validate-or-accept as the options.

### Kill confirmation (conviction-gated)

A kill or a park of an idea, at any gate or at the commercial-score decision, **auto-confirms in autonomous mode unless the validation layer fires on it**: if a decision-critical claim driving the stop is Low conviction, the stop **escalates to the founder** (validate-or-accept) before it stands; High/Medium-conviction stops proceed without a pause. Before escalating, try to validate the claim with desk research, and escalate only if it is still Low. If the founder chooses to validate and that needs work outside the run (interviews, a test), record the stop as **provisional**, with the test attached, and finish the run; the test's result is new evidence for a re-run. In checkpoint mode, all kills and parks pause. A veto routed to a partner (or, at 09, to a different legal structure) does not pause: the evaluation continues, and its Low-conviction claims go through the validation layer in 13. The 13 high-commercial / weak-financial contradiction is a mandatory escalation even in autonomous mode (a genuine ambiguity, not a kill); it applies to crisp ≥6 placements *and* to borderline-band cases resolving toward pursue or validate-first. A **validate-first** band verdict is otherwise emitted as the final verdict in autonomous mode, with its full payload (see `rubric.md`, "Borderline band"). Every kill or park carries the challenge pass applied to the stop itself.

## Pauses during a run

A run asks the founder something only in these cases. Each is asked as a plain message.
- The folder-name confirmation at the start (How to start, step 3).
- **Deep research:** before using deep research (see "Research and deep research").
- **Checkpoint mode,** when the founder has requested it.
- **The escalations** in "Kill confirmation": a low-conviction kill or park, and the 13 contradiction.

Anything else that would otherwise be a question is recorded in the section instead: as an open assumption, a claim to verify, or a limitation in the Rationale.

## Agents

Agents do the divergent work and parallel research:
- **01:** one research agent per topic cluster, and a brainstorm of problem framings with distinct lenses.
- **04:** the idea brainstorm, with distinct lenses covering the variation types.
- **05 and 06–12:** research may be split across agents where it helps.

Agents return findings; the main run writes the section file, so each file keeps one voice and stays within its word cap. If the host cannot run agents, run the same work as sequential passes, one per cluster or lens; the output is the same.

## Standing habits (apply throughout every section)

**Generate alternatives where the template says so.** In 01 and 04, and in 02's and 05's choices, consider the real alternatives before settling, and show the ones considered, not just the winner. In 06–13, follow "No alternatives after the screen": no alternative ideas, segments, markets, form factors or models.

**Falsify first answers.** When an answer feels obvious, treat that as a signal to challenge it. Search for evidence that it is wrong before accepting it. Ask: what would make this wrong? What am I assuming? What would a skeptic say?

**Avoid US/global defaults.** Apply a local lens: local incumbents, substitutes, payment infrastructure, trust signals, dominant channels, language and content gaps, regulators, and cultural patterns around the problem. In 01–04 the lens follows every geography the evidence points at, not only a market lead. From 05 on it applies to each idea's market. Cite local sources where possible.

**Name comparables specifically.** "Like Fandango" is not analysis. *Fandango operates in market X under conditions Y; in target market Z those conditions are A* is analysis.

**Conviction labels everywhere.** Apply H/M/L conviction labels to any judgment call, quantitative estimate, market assertion or competitive claim, not just rubric scores.
- **High:** backed by external evidence (interviews, primary data, market research).
- **Medium:** backed by analogous evidence (similar products' performance, indirect signals).
- **Low:** own reasoning, no external validation yet.

Conviction tracks **evidence quality** (how directly and soundly the evidence measures the claim), **not source type**. This framework's research is almost always secondary, so "secondary" never by itself means Medium (the basis for M is *indirectness*). An authoritative secondary source (official statistics, a rigorous survey, real pricing or transaction data) can be High, and the mere existence of a primary study is not High until its quality is assessed. A Low label is not a problem; it is an honest signal of where research is needed. Do not inflate conviction to seem decisive.

**Validate before deciding (the validation layer).** Before any proceed or kill is finalized, identify the decision-critical low-conviction claims (the load-bearing ones that would flip the decision if wrong) and either validate them or record them explicitly as accepted risk. This applies symmetrically to proceeds and kills, and only to the load-bearing items. (Full rule in `rubric.md`.)

**Verify facts, pin them, and list them (the fact-verification habit).** Distinct from the validation layer: that one gates on *low conviction*; this one gates on *verifiability*, because the highest hallucination risk is on confident specifics. For every decision-relevant external fact or figure (named laws and regulations with numbers or dates, competitor metrics, platform or general-LLM capability claims, market sizes, CAC and pricing benchmarks):
- cite it **at the point of use** with a short marker (e.g., [3]) pointing to the section's source list, plus its conviction label;
- **pin load-bearing quantities once**: a problem-level key-figures set in 01–03, and a per-idea set from 05 on, listed in a short "Pinned figures" line at the end of the Analysis of each section that pins one. Reuse them; never silently re-derive a number that then drifts between sections;
- **add it to the section's "claims to verify" list.** The lists are consolidated in 13.

Verify what you can in-workflow and flag what you can't. (This habit is instruct-and-flag: there is no separate automated verifier yet.)

**Justify blanket conclusions.** No bare categorical judgment ("the market is saturated", "there's no white space", "the channels are taken", "no moat") without its reasoning and the specific, verified evidence stated inline. A categorical claim next to a finding it appears to contradict must be **reconciled**, not left as two loose assertions.

**Don't speculate, and don't ask.** When unsure whether to go deeper, stay within the section's word cap and record the open question in the section. The only mid-run questions are those in "Pauses during a run".

## Length: hard word caps

Discovery filters; it does not produce business plans.
- **Every section template (01–14) states a hard maximum** for its file, counted on the whole file excluding citation markers, the source list and any further exclusions the template names. References are required; they just don't count. The caps are provisional until reviewed after the first dry run.
- **Before the run finishes,** count the words in every section file and rewrite any file over its cap. This is 14's last step, and the counts are recorded there.
- **Depth guidance** (how many incumbents, which scenarios, how far to go on regulation) lives in each template.

## Output format

Section files are markdown, and the reasoning stays in **prose**. Where an output is natively tabular or visual, a table or simple visual carries it better and is welcome:
- **12:** the multi-year, multi-scenario projection as a **structured table** (years × scenarios, with the cumulative-capital row), plus a short prose summary.
- **13:** for each idea decided at 13 (pursue, validate-first, or a kill by the late veto or the commercial score), a **score table** (dimension | score | conviction), a **simple visual of the commercial position** (the commercial average on a 0–10 line, with the 6.0 threshold and the 5.5–6.5 band marked), and the short **build box** from 10; a shorter stop block for an idea stopped before 13; then a comparison table across the evaluated ideas.
- **14:** the key-figures table and the **decision trail** (one row per decision, in run order).
- Elsewhere, a small table is fine where the data is genuinely tabular.

This is permission, not a mandate. Heavier artifacts (a spreadsheet model, a slide deck) are out of scope.

## Research and deep research

**Ordinary web search never needs confirmation,** including searches run in parallel by agents. It is the default research method in every section.

**Deep research** means the dedicated research tool, or a structured multi-source investigation beyond ordinary web search. Its triggers are section-specific and listed in each template. When it appears warranted, pause and ask the founder in a plain message: *"I think deep research is warranted here because [specific reason]. Proceed?"* Wait for the answer. If the founder declines, continue with ordinary search and note the limitation in the section's Rationale.

## Upstream/downstream dependencies (standing rule)

Each template lists what later sections consume from it.
- **Within 06–12:** if a section cannot draw on an earlier section's outputs as expected, revisit that earlier section before continuing; do not proceed on weaker analysis.
- **For 01–05:** a gap traced back to them is **flagged in 13**, never re-opened. There is no send-back.

## Challenge pass (run at the end of every section)

Before finalizing any section, run a structured challenge pass. Each finding uses the fixed short format: what changed and why, or "no change".

**Diverge form (01, 04): "what did we miss?"** These sections have no conclusion to break, so the pass looks for gaps: missing actors, untested assumptions, disguised solutions, unexplored lenses. The section-specific questions are in each template. The facts question below also applies.

**Judging form (02, 05, 06–13).** Try to break the section's conclusion, whichever way it went. Standard questions:
- What's the strongest argument this analysis is wrong?
- What did I assume that I should have investigated?
- What would a skeptical investor say after reading this?
- *(02 and 05 only)* Is there a non-obvious option I dismissed too quickly?
- **Facts:** for each load-bearing external fact or figure on the claims-to-verify list (especially the high-confidence specifics), what is the actual evidence that it is real, and does the recommendation survive if it is wrong? Flag any asserted without a checkable source. (A section that rests on no external facts answers "n/a".)

Templates may add section-specific questions. Apply both layers.

## The kill model (where a run, or an idea, can stop)

A **kill ends an idea, never the problem.** The first diamond never stops a run: 02 always chooses a problem. A run ends without evaluating any idea only if 05 selects none; 13 and 14 are still written. Killing an idea is a valid and valuable outcome: discovery succeeds when it filters ideas accurately, whether the verdict is pursue or kill.

This section is the **canonical statement of each stop-point's firing conditions**. The veto *families*, the *routing* and the commercial-score kill live in `rubric.md` ("The kill model"), which points back here. Templates apply these gates by reference. The stop-points, in firing order:

- **Problem gate and Market gate (06, per idea)**, *early exits*. A Problem severity or Market size score of **0–2** is a fatal commercial veto for that idea. Problem severity is scored against the idea's own target user. The Market-size veto fires only after the every-assumption check confirms that the SOM fails under every reasonable assumption, measured against the idea's threshold from 05 (which 06 never adjusts). (Defensibility is **not** an early exit; it is finalized at 13.)
- **Structural gate (08)** fires on **any** of three structural dealbreakers, each a *conclusion from* 08's research (a low-conviction finding routes through the validation layer before the kill stands):
  - **Legal / regulatory blocked:**
    - required licensing is obtainable by *no one* building this (no new entrant can get it; if an existing licence holder could supply the regulated function, the veto routes to *partner*). Whether *this founder* could hold it is 10's question, not a gate; **or**
    - the activity is prohibited in the idea's market; **or**
    - compliance requires a structure that cannot exist there (an entity type that can't be formed, partnerships unavailable to new entrants); **or**
    - compliance cost is *obviously disproportionate* to any plausible business value: so high that no version of the idea's model could justify it, and visible without 09/12 needing to quantify value. If quantifying value is needed to make the call, this condition does *not* fire; continue to 09.
  - **Data access blocked:** the data, API or partnership the idea needs is obtainable by *no one* building this (not merely hard for this founder; that question is 10's).
  - **Capability infeasible:** the idea's core function cannot be performed to an adequate standard by *anyone* with current technology.
- **Business-model gate (09)** fires on either of two causes, which route differently: **(a)** the idea's revenue model does not survive the legal envelope, or **(b)** it has no viable economics, which is the **Monetization 0–2** commercial veto (negative unit margins at any plausible scale).
- **Locked-average early exit (after 09).** Once 09 locks Problem, Market and Monetization, check whether the idea's commercial average is **mathematically locked below the borderline band** (below 5.5; an average of 5.5–5.99 at M/L conviction is a band case, whose call needs 10–12). Compute it with Defensibility at its **ceiling**: **6** if no structural-moat candidate surfaced in this idea's research (without one, the finalized score cannot exceed 6, per `rubric.md`'s Defensibility cap), **10** if one did. If even the ceiling can't reach 5.5, early-exit to 13; 10, 11 and 12 are recorded as skipped. In checkpoint mode, propose the short-circuit and let the founder choose; in autonomous mode, apply it and document the lock arithmetic. This is not a veto; it reaches 13 as a commercial-score kill with the grind removed.
- **GTM gate (11):** no go-to-market strategy produces CAC recoverable within the model's plausible payback window, **after the adjustment attempt** (template 11 holds the benchmarks and the adjustment menu). A kill; skip 12.
- **13:** the **Defensibility late veto** (scored provisionally at 07, finalized at 13 once 08/09's moats are known; a veto if still **0–2**) and the **commercial-score decision** (commercial average **< 6**, or a placement demotion; see `rubric.md`). A commercial average in the **5.5–6.5 borderline band at M/L conviction** yields no crisp verdict. It gets elevated scrutiny of the load-bearing claims and a documented qualitative call with three outcomes (**pursue / validate-first / kill**), provisional until the financial-coherence check (see `rubric.md`, "Borderline band").

**Gates are rare by design.** The Structural (08) and Business-model (09) gates fire only on definitive dealbreakers; on most realistic ideas their research concludes "no veto". A non-firing gate is **not** a health signal. The load-bearing output of those sections is the research itself, which feeds the scores, the structural notes and 13.

**At any stop-point,** recommend the stop (kill or park) with explicit rationale **and the challenge pass applied to the stop itself**: what would make it wrong (missed evidence, a misread source, a partnership structure that removes a structural block). Do not develop alternative routes, segments or pivots (see "No alternatives after the screen").
- **Routing.** Commercial vetoes (including the Monetization veto, Business-model gate cause b) are a clean kill of the idea. Structural vetoes route to *partner / kill / park* (see `rubric.md`). **Partner** is the same idea, run with a partner: the evaluation **continues** with the partner built in (09–12 price it, and 13 states it with the verdict), which is how the commercial case the route depends on gets tested. **Kill** ends the idea. **Park** (capability only) ends the evaluation without a kill; 13 records the idea as parked, with the capability change that would reopen it. Business-model gate cause (a) routes to a licensed partner or a different legal structure for the same model when one exists, and the evaluation continues with it built in (the rest of the evaluation tests the commercial case); if none exists, kill.
- **Confirmation.** The kill is confirmed per the conviction-gated rule.
- **After a stop** (a kill or a park). The idea's subfolder holds the sections completed up to and including the stop-point. 13 records the stop-point, the rationale, the challenge pass applied to the stop, and which sections were not run. The run then continues with the next selected idea, if any.

## Cross-idea calibration

For each idea decided at 13 (13's Tasks 1–5), before finalizing its block, check whether `projects/` holds prior evaluations from **other** problem folders. Never use a run's own predecessor (the original of a re-run). Prior evaluations are v3 runs (their 13 blocks hold the score records) and v2.x runs (`09-decision.md`). Sibling ideas in the same run are not used for calibration. Instead, where siblings rest on the same evidence (the same market estimate, the same users), 13 checks that their scores on that dimension agree, or explains the difference; this compares scores only, never verdicts.

If prior evaluations exist:
- Identify the 3 closest by domain or shape.
- Compare this idea's scores against them. Are the scores internally consistent? Does this idea genuinely deserve a higher commercial score than a given prior idea, on what was known then?
- If scores have drifted upward over time (everything starting to look like a 7), flag it explicitly.
- **Scoring consistency only, never verdict consistency.** A prior kill (or pursue) is not evidence for this idea's verdict; "the portfolio has consistently killed this shape" is disallowed reasoning (see `rubric.md`'s Calibration note).
- **Calibration scope.** Compare in-scope ideas only against in-scope prior runs, and out-of-scope ideas only against out-of-scope prior runs (skip the step if there are none).

If there are no prior evaluations, skip this step.

## Scoring

See `rubric.md` for the full scoring system.
- **Commercial score** (the only verdict input): four equally weighted dimensions, combined as a simple average: problem severity (06), market size (06), defensibility (provisional at 07, finalized at 13), and monetization clarity (09). There are no caps: a fatal 0–2 dimension is a *veto*, and two or more weak (3–4) dimensions demote placement.
- **Solo-buildability** (10): a **sidebar, not an axis.** Scored 0–10 with a conviction label against `rubric.md`'s anchors and `user-profile.md`, so it stays calibrated and comparable across ideas. It appears in 13 as a short **build box** under the verdict, never in it.
- **Agent-fit** (07): qualitative and descriptive only.

**The verdict comes from the commercial score alone** (pursue / validate-first / kill, with the borderline band and the vetoes). Solo-buildability never moves a verdict, triggers a question or feeds a gate; it only describes *how* a pursued idea would be built (solo, solo with significant learning, with a collaborator, or with a partner). Pursue verdicts are labelled for durability, **pursue-durable** (structural moat) or **pursue-as-lifestyle-bet** (execution-tier moats, durable at the idea's threshold scale), per `rubric.md`. Agent-fit informs execution planning after a proceed and gives portfolio visibility; it never changes a verdict or breaks ties.

**The make-money threshold** comes from 05, researched from comparable businesses at the idea's scale ambition, and is stated as the revenue the business keeps (excluding money passed on to sellers, suppliers or workers; a marketplace's take, not its gross transaction value). It is never a founder input. Market size and Defensibility durability are judged against it.

## Calibration scope

The framework's anchors, worked examples, agent-fit lenses, wrapper test and CAC/churn assumptions were written and validated on **digital products**. An idea for a physical product (CPG, food, hardware) runs through the same instrument and the evaluation is valid, but three limitations are known and are *not* compensated for in scoring:
- Problem severity is written for painkillers and reads low by construction for indulgence goods.
- Defensibility cannot credit a taste or brand edge before the product exists.
- Culturally grounded preference is demand evidence, never moat evidence.

Score honestly against the anchors as written, and note the limitation where it bites. Set the idea's metadata line to **`Calibration scope: out-of-scope (<reason>)`** so cross-idea calibration keeps it out of the in-scope comparison (the tag changes nothing else); digital-product ideas carry `Calibration scope: in-scope`. An idea that answers a desire rather than a pain keeps the scope of its product type: a desire-driven digital idea is in-scope, and where Problem severity reads low by construction, 06 records it as a finding that 13 reports. A decision memo written from an out-of-scope idea says plainly which dimension reads low by construction and whether the verdict rests on it.

## Post-decision amendments

A completed evaluation may be changed after its decision in exactly four ways. Correcting a run and changing the instrument are different acts and are never mixed.

- **Erratum:** an arithmetic slip, a pinned figure that drifted between sections, a stale cross-reference, or an anchor **misapplied** under the rubric version the run was scored on (for example, buildability reasoning inside a Market score, or a "prospective / unproven" discount on Defensibility, which the moat-potential rule forbids). Errata are **applied**: the score changes if the misapplication changed it, the verdict is re-derived through 13's normal chain, and the original values are preserved in the amendment log. Applying the existing anchors correctly is not score manipulation; adjusting anchors mid-evaluation is.
- **Recalibration:** a change to anchors, dimension definitions, thresholds or decision logic. It goes through `design-notes.md`, updates every dependent file in one pass, bumps the version, and **never re-scores prior runs**.
- **Re-run:** triggered only by **new evidence** (a test result, a verified figure that flips a load-bearing claim). An argument is not evidence: record it in the amendment log with a cheap test and explicit flip conditions, and leave the score alone. New evidence about the problem itself (01–03) triggers a re-run of the whole problem, in `projects/<problem-name>-v2/`. New evidence about one idea triggers a re-run of that idea, in `ideas/<idea-name>-v2/` (if the evidence changes the idea's threshold, the re-run carries a revised handoff, logged as such); 13 and 14 are then reissued with the v2 block in place of the original block, and the amendment log records the re-run and points to the original subfolder, which stays untouched. Either re-run is stamped with the framework version in force; the original stays as calibration data for other problems, never for its own re-run.
- **Added idea:** running a flagged idea after the decision (see "Flagged, not run"). 13 and 14 are reissued with it added; nothing already decided changes.

Rules for every amendment:
1. **Propagate mechanically.** Use the templates' consumption mappings: an amendment that changes a figure, date or score is not complete until every consuming section is updated. Before closing, search the problem folder for the *old* value; if it still appears outside the amendment log (and outside a superseded original kept by a re-run), the amendment is not done. Re-run every task that consumes the corrected figure (for example, 12's scenarios and 13's financial classification), not only the cells that held it. If the re-derived verdict meets an escalation (a Low-conviction stop, or the 13 contradiction), ask the founder and record the answer in the amendment log.
2. **Replace, don't append.** Amended text replaces the superseded text in place, with a one-line `*(amended YYYY-MM-DD — see amendment log)*` marker. No banners at the top of sections, no superseded paragraphs left in the body.
3. **One score record per idea.** Each idea's block in 13 carries the corrected record as authoritative; the original values and date live in the amendment log.
4. **One amendment log** per problem, as an appendix at the end of `13-decision.md`, one entry per change: date · idea · category (erratum / recalibration-note / re-run trigger / added idea / recorded dissent) · what changed · why, citing the rule or evidence · files touched · score and verdict effect. A *recorded dissent* is a defensible alternative reading that was deliberately not applied.
5. **Derivative documents** (a decision memo for a co-founder, partner or reviewer) are written *from* the corrected run, carry no score record of their own, cite the run, and live in the problem folder as `decision-memo.md` (or `decision-memo-<idea-name>.md` when it covers one of several ideas). They are never the system of record and are never read by cross-idea calibration.

## Framework version

Current framework version: **3.0-draft (dry-run build, 2026-10-06)**. v3 restructures the framework on the double diamond:
- a founder entry that names a potential problem;
- a first diamond (Discover, Define) and a produced midpoint brief;
- ideation and a screen that selects up to three ideas;
- the existing evaluation, run per idea;
- one decision file and one run summary per problem.

Problem severity moves to 06 and is scored per idea. Solo-buildability becomes a sidebar: still scored, but the 2×2 matrix is gone and the verdict comes from the commercial score alone. Alternatives are generated only before the screen, which removes developed recovery routes, pivot routing and the band's pivot outcome. The learning-project rule, depth overrides and the v2 brief's guessed fields (threshold, runway, learning) are removed. Word caps are hard and enforced. No anchor, dimension definition or threshold value changed. Three gate rules changed: the legal block no longer depends on this founder (that question moved to 10); a veto routed to a partner continues the evaluation; and at 11 a capacity gap is priced, not disqualifying. (v2.3 added the post-decision amendment procedure and the calibration-scope tag. Earlier history is in `design-notes.md`.)

Any skill change bumps this version. 13 records the exact version **read from this file**, never from the skill's folder name, in each idea's metadata, so evaluations stay comparable across framework changes.

## Output

The final artifact is the populated problem folder.
- **Problem level:** 00–05, `13-decision.md` and `14-summary.md`.
- **Per selected idea:** an `ideas/<idea-name>/` subfolder holding 06–12, or the sections up to where it stopped (a kill, a park, or 09's locked-average early exit).
- **`13-decision.md` is always written,** whatever the outcome: no idea selected at 05, every idea killed, or one or more ideas proceeding. If 02's choice rested on Low-conviction evidence, 13 says so. It is the decision document, readable on its own, with:
  - one block per evaluated idea (for an idea decided at 13: score record, commercial position, verdict and build box; for an idea stopped earlier: its stop block; both with metadata including framework version and calibration scope);
  - the comparison across evaluated ideas;
  - the flagged opportunity areas and ideas that were not run;
  - the open assumptions from 03 with their cheapest tests;
  - the consolidated claims to verify.
- **`14-summary.md` is always written last:** a plain-language record of what was researched, what was learned and what was decided at each step, with the run's word counts. It summarises only and points to 13 for what to do.
