# Template: 13 — Decision

## Purpose of this section in the framework

Section 13 is the **exit point**. It is written **once for the whole problem**, in the problem folder, after every selected idea has finished its evaluation (or been stopped). It is the run's decision document: readable on its own, with 00–12 as supporting detail. The record of how the run got there (what was researched, what was learned, the decision trail) is 14.

It produces:
- **One block per evaluated idea:**
  - the finalized Defensibility score and the commercial score;
  - the verdict;
  - the financial coherence check;
  - the build box;
  - the idea's metadata.
- **A comparison** across the evaluated ideas
- **What was not run:** flagged opportunity areas (02), flagged ideas (05) and gaps flagged by 06–12
- **What remains open:** 03's open assumptions with their cheapest tests, the recorded findings from 06–12, and the consolidated claims to verify
- **The run's housekeeping:** the pre-decision self-audit and, if ever needed, the amendment log

13 adds no new research. It assembles and decides.

**Each idea is decided on its own evidence.** An idea's verdict comes only from its own 06–12. A sibling's verdict, or any prior run's, is never evidence for this one (`rubric.md`, "The verdict-ratchet guard"). The comparison is written **after** every verdict is fixed, and it never changes one.

**13 is always written:**
- when no idea was selected at 05;
- when every idea was killed;
- when one or more ideas proceed.

## Inputs

- **Per idea:** its 06–12 (or the sections up to its kill), 05's handoff, and 10's build box.
- **Run level:** 01–05's claims-to-verify lists; 02 (flagged areas, and whether the choice rested on Low conviction), 03 (open assumptions), 04 (all ideas), 05 (selection, flagged ideas, answers to the leads).
- **`SKILL.md`:** the framework version, **read from the file itself**, never from the skill's folder name.
- **`projects/`:** prior evaluations from **other** problem folders, for cross-idea calibration.

## Research activated in this section

None.

## Analytical work for this section

Tasks 1–6 run **per evaluated idea**. Tasks 7–9 run **once for the run**.

**An idea stopped before 13** (killed at 06, 08, 09 or 11, or parked at 08) skips Tasks 1–5; go straight to its kill block in Task 6. Tasks 1–5 run for every idea that reached 13 undecided, including one that took 09's locked-average early exit. That idea's verdict comes from its actual finalized scores, not the ceiling used in the lock arithmetic.

### Task 1: Finalize Defensibility and apply the late veto

07 scored Defensibility provisionally. Reconcile it against the moats in the Moat candidates lines of 08 (regulatory) and 09 (data, network, business model). A licence or capability held by a partner is the partner's moat, not this idea's. raise it if they add real defensibility, and say why; otherwise the provisional score stands. Check the cap: no score above 6 without a named structural moat (`rubric.md`). Document the reconciliation.

**Late veto:** a finalized score of **0–2** is a fatal commercial veto, and a **clean kill** of this idea. It follows the kill path (Task 6), confirmed per the conviction-gated rule.

### Task 2: Assemble the commercial score

The four dimensions, equally weighted, as a **simple average** with no caps:
- Problem severity (06);
- Market size (06);
- Defensibility (finalized in Task 1);
- Monetization clarity (09).

Every dimension here is already ≥3, because a 0–2 is a veto at its own section.

**"Weak on multiple fronts" demotion:** if **two or more** dimensions sit at **3–4**, the idea is placed **low-commercial regardless of its average**. Record the demotion and the dimensions that triggered it. The score itself stays the honest average.

**Overall conviction** is the **lowest** of the four. Name any L-conviction dimension.

Run **cross-idea calibration** (`SKILL.md`): compare the scores with the three closest prior evaluations from other problem folders. This checks scoring consistency only, never verdicts. Sibling ideas from this run are not used. Instead, where sibling ideas rest on the same evidence (the same market estimate, the same users), check that their scores on that dimension agree, or explain the difference. This too compares scores only, never verdicts.

### Task 3: Retrieve the financial picture

From 12, in compressed form:
- the threshold result (scenarios, timing, magnitude, conviction, drivers);
- the cumulative capital required;
- the conviction picture;
- the key risks.

If the GTM gate fired in 11, or the locked-average early exit applied after 09, there is no financial picture. Say so.

Classify the picture as one of:
- **Strong:** meets the threshold in the expected case, a robust range, H/M conviction.
- **Marginal:** meets only in the optimistic case, or rests on L-conviction drivers.
- **Weak:** doesn't meet, or meets only at the threshold with breaking risks.
- **None.**

### Task 4: Reach the verdict (commercial score only)

The verdict comes **from the commercial score alone** (`SKILL.md`, "Scoring"). Solo-buildability is not an input.

| Commercial placement | Verdict |
|---|---|
| **≥6.0** (crisp), no demotion | **Pursue**, labelled **pursue-durable** (rests on at least one structural moat) or **pursue-as-lifestyle-bet** (rests on execution-tier moats, durable at the idea's threshold scale) |
| **<6.0**, or demoted | **Kill** (a commercial-score kill) |
| **5.5–6.5 at M or L** conviction, no demotion | **Borderline**: no crisp verdict (below) |

**Borderline band.**
- Flag the idea "too close to call" and run **elevated scrutiny**: re-verify the load-bearing claims behind the four dimensions and reconcile any tensions.
- Then make a **documented qualitative call** with three possible outcomes: **pursue, validate-first or kill**.
  - A creditable moat (structural or execution-tier) with a coherent financial picture can resolve to **pursue**, labelled for durability.
  - A plausible but unverified case resolves to **validate-first**. Pursue needs every load-bearing claim at M or H; one still at Low makes the call validate-first.
  - No moat leans to **kill**.
- **Overrides:** H conviction in the band stays crisp. The "weak on multiple fronts" demotion takes precedence over the band.
- **The call is provisional** until Task 5's financial-coherence check.
- **In autonomous mode** the band produces a flag and a documented determination, not a pause. A validate-first is emitted as the final verdict unless the validation layer fires on a decision-critical Low-conviction claim, or Task 5's escalation fires. **In checkpoint mode** it pauses, like any section.

**Validation layer and kill confirmation.** Before any verdict is final, pursue or kill, identify the decision-critical Low-conviction claims it rests on, and either validate each one or record it as an accepted risk (`rubric.md`, "The validation layer"). A kill decided here (by the late veto or the commercial score) is confirmed per the conviction-gated rule: it escalates if it rests on a decision-critical Low-conviction claim.

**Distance to the band.** When a crisp kill sits within 0.5 of the band (an average of 5.0–5.4, or a demoted case averaging ≥5.5), state in one sentence how far it is and which one-point calls would open the band.

### Task 5: Check financial coherence

The financial picture qualifies the verdict:
- **Strong:** the verdict is well supported.
- **Marginal:** a pursue carries the caveat "depends on optimistic execution".
- **Weak:** see the contradiction below.
- **None:** the idea is on the kill path from its gate, or was already decided by the locked-average exit.

**High commercial, weak financial: a mandatory escalation, even in autonomous mode.** It applies when the placement is a crisp ≥6, or a band case resolving toward pursue or validate-first, but the financial picture is weak. This is a genuine contradiction, so ask the founder in a plain message (a sanctioned pause; `SKILL.md`, "Pauses during a run"). Offer three options:
- **Trust the commercial score:** pursue, with the weak financials as a risk to monitor.
- **Trust the financial picture:** treat the idea as low-commercial, which makes it a kill.
- **Revisit the analysis:** identify the most likely source of error within 06–12 and re-examine that section. A suspected error in 01–05 is flagged, not reopened.

**For a band case,** the first option is instead **keep the band call** (validate-first, with the weak financials as a risk); it never becomes a pursue the band did not reach. **Revisit once:** if the re-examination leaves the picture weak, ask again with only the first two options.

Record the founder's choice and the reasoning.

**The inverse tension** (favourable financials against a borderline commercial score) is fed into the band's qualitative call as explicit evidence toward pursue or validate-first, and documented. 05's threshold is the standard; do not substitute an unstated durability bar, since durability is already priced into the pursue label.

### Task 6: Write the idea's block

**For a proceeding idea** (pursue or validate-first), the block contains:
- **Score table:** dimension | score | conviction, the average, any demotion, and the overall conviction.
- **Commercial position:** a simple visual of the average on a 0–10 line, with the 6.0 threshold and the 5.5–6.5 band marked.
- **Verdict**, with its durability label, and any caveat from Task 5.
- **Build box**, copied from 10, directly under the verdict. It describes how the idea would be built and never affects the verdict.
- **Action:**
  - **Pursue:** the next steps, the key risks to monitor and the threshold checkpoints. If the idea runs with a partner (a route from 08 or 09, or a partner named in the build box), the partner type to look for, and a statement that the verdict assumes that partner.
  - **Validate-first:** the full payload, which is the verdict's substance and incomplete without all three parts:
    - the **named load-bearing assumptions**: the specific claims the decision turns on, drawn from 03's open assumptions where they apply, plus any specific to this idea;
    - a **cheap test** for each (what to run, rough cost and effort, timeframe);
    - **explicit flip conditions** ("if X, pursue; if Y, kill").
- **Financial summary:** the threshold result and the cumulative capital required (the runway the idea needs).
- **Risks:** monitorable versus structural, L-conviction findings to treat as open questions.

**For an idea killed at 13** (by the late veto or the commercial score), the block contains the score table, the commercial position and the build box ("Build: not assessed" after the locked-average exit), as for a proceeding idea, plus:
- the **finding that decided the kill**, and how the kill was confirmed per the conviction-gated rule;
- **what was learned**: the useful findings.

**For an idea stopped before 13** (killed at 06, 08, 09 or 11, or parked at 08), the block contains:
- the **stop-point and its finding**, and how the stop was confirmed per the conviction-gated rule;
- for a parked idea, the **capability change that would reopen it**;
- the **sections not run**;
- the **scores assigned before the stop**;
- **what was learned**: the useful partial findings.

Nothing is attached to the kill (`SKILL.md`, "No alternatives after the screen"); the other ideas are in 04 and in Task 7's "not run" list.

**Partner or structure routes.** In every block of an idea decided at 13, if the idea ran with a partner or a different legal structure (a route from 08 or 09), say so next to the verdict: the verdict assumes it.

**Metadata,** at the end of every block:
- the score record (all dimensions with conviction, the commercial score, and the solo-buildability score from the build box, or "not assessed" if the idea stopped before 10);
- the verdict and durability label;
- the evaluation date;
- the **framework version as stated in `SKILL.md`**;
- **`Calibration scope:`** `in-scope`, or `out-of-scope (<reason>)`;
- the agent-fit verdict and form-factor fit (from 07), if the idea reached 07;
- the idea's folder.

### Task 7: Compare the ideas, and list what was not run

**Comparison** (only when more than one idea was decided at 13): a table with one row per idea decided at 13 and these columns:

| Idea | Commercial score / conviction | Verdict | Threshold result | Capital required | Build box |
|---|---|---|---|---|---|

Ideas stopped before 13 are listed under the table by stop-point, not given a row. Follow it with two or three sentences on how the ideas differ in evidence strength and risk. The comparison describes; it **never changes a verdict**. If the founder can pursue only one, say which is strongest **on the evidence**, and why.

**Not run.** List:
- **Flagged opportunity areas from 02**, each with its one-line reason;
- **Flagged ideas from 05**, each with its reason, including any flagged because a single Low-conviction claim kept it out;
- **The answer to each lead** (from 05);
- **Gaps flagged by 06–12**: places where a section noted that a different idea might work and 04 has none like it;
- **Flags against 01–05**: suspected errors or gaps in 01–05 noted by later sections (for example, a threshold 06 found doubtful, or something 01 missed), each with its section. They are flagged, never reopened.

The founder decides whether to run any of them (`SKILL.md`, "Flagged, not run").

**If no idea was selected at 05:** 13 consists of the header, the four parts (the Analysis is 05's reason and the "not run" list; the challenge pass targets the decision to select none), Task 8, and self-audit checks 7 and 8.

### Task 8: Consolidate what remains open

- **A weak-evidence warning,** if 02's choice rested on Low-conviction evidence, stated first.
- **Open assumptions:** 03's list with its cheapest tests, plus idea-specific ones (the Low-conviction load-bearing claims on 06–12's claims-to-verify lists) not already in a validate-first payload.
- **Recorded findings:** the findings 06–12 recorded instead of asking mid-run (required partnerships, thin payback, threshold concerns and so on), each with its section.
- **Founder decisions:** answers to pauses and escalations, and any idea the founder set aside, each with its reason.
- **Claims to verify:** the consolidated list from every section, each with its source and conviction. Flag any load-bearing claim that still lacks a checkable source.

### Task 9: Run the pre-decision self-audit

**Self-audit** (mandatory). Record a one-line result for each check:
1. **Arithmetic:** each commercial average recomputed, and any scenario numbers quoted.
2. **Veto hygiene:** no 0–2 averaged in or counted toward the demotion (which counts only 3–4).
3. **Triggers:** the demotion fired exactly at two or more 3–4s; the band was applied exactly at 5.5–6.5 M/L (not H); the Defensibility cap was applied.
4. **Escalation order:** every band case resolving toward pursue or validate-first went through Task 5.
5. **Validate-first completeness:** all three payload parts are present.
6. **Ratchet and independence:** no verdict leans on a prior run's verdict *or a sibling's*.
7. **Claims sweep:** Task 8's list is complete.
8. **Version:** the version recorded matches `SKILL.md`, not the folder name.
9. **Sibling consistency:** dimensions resting on the same evidence score alike across sibling ideas, or the difference is explained.

Correct any failure before finalizing, and note the correction in the Rationale.

The run's word counts are taken in 14, the last file written.

## Section-specific content for the four required parts

The four required parts are mandatory per `SKILL.md`. 13's structure maps onto them:
- **Header** (above the four parts):
  - the problem's working name;
  - the date;
  - the run mode;
  - the framework version in force when this file was issued (each idea block records its own).
- **Analysis:** the idea blocks (Tasks 1–6), the comparison (Task 7).
- **Recommendation:** each idea's verdict in one line, then the run's bottom line: what the founder should do next (pursue X, run the tests for Y, or consider the flagged items).
- **Rationale:** in this order:
  1. why each verdict was reached, with the commercial drivers and the financial drivers;
  2. any contradiction and the founder's choice;
  3. the self-audit result;
  4. Task 8's open items: the weak-evidence warning, the open assumptions, the recorded findings and the claims to verify.
- **Challenge pass:** below.
- **After the four parts:**
  - the "not run" list;
  - if amended, the amendment log (`SKILL.md`, "Post-decision amendments").

Use the fixed short format for challenge-pass findings: what changed and why, or "no change".

## Challenge pass: section-specific questions

The judging form from `SKILL.md` (06–13 omit the "non-obvious option" question), applied to each verdict (for a kill, what would make the kill wrong), plus:
- **Score honesty:** is each average faithful? Was no genuine 0–2 softened to a 3 to dodge a veto? Was the Defensibility reconciliation honest, not inflated by speculative moats? Is the overall conviction the lowest of the four?
- **Verdict rigor:** were band cases handled as borderline (no early crisp verdict, held until Task 5), H-conviction band cases kept crisp, and the demotion applied but not over-applied?
- **Independence:** was each verdict reached before the comparison was written, without reference to a sibling's outcome?
- **Financial contradiction:** was every high-commercial / weak-financial case escalated, not smoothed over?
- **Document honesty:** does the document represent the analysis faithfully, without tilting toward any one idea or verdict? Pursue blocks must show their risks plainly; kill blocks must keep what was learned.
- **Claims:** does any verdict rest on a confident specific that still lacks a checkable source?

## Word cap

**Hard maximum (provisional):** **700 words per evaluated idea**, plus **700 words** for the rest of the file, excluding citation markers, source lists and the amendment log. For example, three evaluated ideas give a ceiling of 2,800 words. A killed idea's block is usually much shorter.

## Downstream dependencies

13 is the last section that judges; the founder acts on it, and 14 summarises the run from it. Its per-idea **metadata** is what cross-idea calibration reads in future runs, and what any amendment updates.
