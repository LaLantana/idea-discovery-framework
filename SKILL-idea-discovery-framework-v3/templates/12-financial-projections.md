# Template: 12 — Financial projections

## Purpose of this section in the framework

Section 12 builds the **multi-year financial picture** for one idea and makes the explicit comparison against **05's make-money threshold**. 09 produced the unit economics and 11 the initial investment; 12 scales them into revenue, cost and profit over time, under three scenarios.

**No gate fires here.** A "doesn't meet the threshold" finding is not a kill on its own. 12 does not score or change the commercial score. It produces the financial picture that **13** uses to interpret the commercial score, including the financial-coherence check on the borderline band and the high-commercial / weak-financial contradiction.

This section produces:
- Revenue and cost projections over the modeling window
- Three scenarios (conservative, expected, optimistic), each a coherent story
- The comparison against 05's threshold, with timing, magnitude and conviction
- The **cumulative capital required**: the runway this idea needs
- The key risks, and a synthesis for 13

## Inputs

- **05's handoff:** the threshold (a pinned per-idea key figure; never re-derived), and the market.
- **09:** the revenue model, pricing and unit economics.
- **11:** the recommended GTM, its CAC and payback, and the initial investment by component.
- **10:** the time to MVP, which sets when revenue can start.
- **08:** ongoing compliance costs.
- **06:** the SOM, which caps what the projections can plausibly reach.
- **03:** the pinned problem-level figures.

## Research activated in this section

**Ordinary web search, discretionary,** for growth, retention and churn benchmarks for comparable products in the idea's market, scaling-cost benchmarks, and typical multi-year trajectories. Deep research is rarely warranted; follow the pause in `SKILL.md`, "Research and deep research".

**Source quality and fact discipline.** Industry reports with multi-year financials → H; aggregated growth benchmarks → M; "we grew from X to Y" posts → L. Cite each benchmark at the point of use, pin it once and reuse it across scenarios, and add the load-bearing ones to the claims-to-verify list. **Survivorship bias:** growth stories come overwhelmingly from the winners. Check the realistic distribution before leaning on them.

## Analytical work for this section

### Task 1: Set the inputs and the window

Summarize the inputs above. Choose the **modeling window**: 3 years by default, 5 for long ramps (multi-year B2B sales cycles, long time to traction, capital-intensive products). The window must reach at least the year named in 05's threshold. State the choice and why; it is then fixed for this section.

### Task 2: Project revenue

Build from:
- **Acquisition rate:** customers per month or quarter, from 11's GTM and CAC. Slow at first, ramping as the GTM gains traction. Model compounding only where there is a specific mechanism (an SEO base, referrals, network effects).
- **Revenue per customer over time:** from 09, with a retention curve and any expansion revenue (upgrades, usage growth).
- **Timing:** revenue starts after the MVP (from 10).

**For pass-through models** (marketplaces, resellers, agencies), project the **gross** first (transactions × average value), then apply a stated take rate to get the **revenue the business keeps**. Show both. Only the revenue kept is compared against the threshold.

Per year, produce:
- the active customers at year-end, net of churn;
- the gross (pass-through models only);
- the **revenue kept**, net of refunds and credits.

**Default skepticism.** The most common failure is assuming a new product acquires at an established product's rate from day one. Most products take longer than projected to reach their target rate, and many never do.

**SOM check.** 06's SOM is what the idea can capture in its first 3 years. If any scenario's revenue in years 1–3 approaches or exceeds it, either the projection or the SOM is wrong. Cap the projection at the SOM, or, if the SOM is what is wrong, revisit 06 (`SKILL.md`, "Upstream/downstream dependencies"): amend the SOM there with a dated note and re-check the Market size score. Never change it silently. In a 5-year window, growth beyond the SOM after year 3 needs a stated reason (a new segment within the same users, market growth), not just momentum.

Label the key assumptions (acquisition ramp, retention, compounding) with conviction.

### Task 3: Project costs

By category, over the same window:
- **Initial investment:** from 11 (build, compliance, GTM, operating), spread across the window it actually covers, which can run past year 1. The ongoing lines below start only after that window, so nothing is counted twice.
- **Ongoing operating costs:** infrastructure scaling with usage, support scaling with customers, AI/LLM costs scaling with usage, general operations.
- **Ongoing GTM:** paid acquisition scales with the acquisition target, content sub-linearly, sales with sales intensity.
- **Ongoing compliance:** from 08: renewals, audits, reporting.
- **Direct unit costs:** payment processing, per-transaction compliance fees, per-interaction AI costs.

Per year: total costs by category, and cost per customer as a sanity check.

**Watch for costs that grow faster than revenue**: AI/LLM costs when pricing isn't usage-aligned, support load, and infrastructure thresholds (data egress, database scaling, security). If any category outgrows revenue, the model is unsustainable at scale. Say so.

### Task 4: Build the scenarios

Three scenarios, each internally consistent, with variables moving together as that story implies:
- **Expected:** best current estimates; execution goes roughly as planned.
- **Conservative:** the 2–3 assumptions whose downside would hurt most move to honest worse-than-expected values. Typically:
  - subscription: CAC and churn;
  - transactional: volume and frequency;
  - B2B: sales cycle and contract value;
  - ad-supported: engagement and ad rates.

  Name the assumptions first. Others stay at expected unless causally linked.
- **Optimistic:** the same dominant assumptions move to honest better-than-expected values.

For each scenario: the revenue, cost and profit/loss trajectories; the **cumulative capital required** (the deepest negative cumulative cash position across the window); and the time to breakeven, or when beyond the window it would come.

**Honest scenarios** test different assumption sets, not "expected ± 15%". The conservative case should answer "what if the things that could go wrong, do?", and look materially different.

### Task 5: Compare against the threshold

Compare the **revenue kept** against **05's threshold** and state:
- in which scenarios it is met;
- when (which year, or beyond the window);
- by how much (e.g., "1.5× threshold", "40% below");
- with what conviction;
- driven by which 2–3 assumptions.

For example: "Meets in the expected case in year 2 (M) at about 1.3× threshold; meets in the conservative case in year 3 (L) at about the threshold, driven by CAC and retention assumptions with thin local benchmarks."

A high-confidence, high-magnitude result is a much stronger picture than a marginal, low-confidence one. Never present "meets in the optimistic case" as if it were "meets in the expected case".

### Task 6: Identify the key risks

For each significant risk, state:
- **what it affects:** revenue, cost or timing;
- **how much:** small, material, or breaking (could flip a "meets threshold" conclusion);
- **whether it is monitorable** (visible in execution, so the founder can respond) **or structural** (market shifts, regulation, a competitor, a platform policy, which must be absorbed or hedged).

### Task 7: Apply the local lens

- **Market growth:** fast-growing, mature or declining.
- **Pricing over time:** commoditization pressure or pricing power.
- **Cost inflation** in this market.
- **Capital availability**, if outside capital becomes relevant.
- **Currency volatility** for cross-border projections, and any other market-specific factor.

If the lens changes the projections, revise Tasks 2–5 and say what changed.

### Task 8: Synthesize for 13

A short, standalone story:
- the expected-case trajectory;
- the threshold result (scenarios, timing, magnitude, conviction);
- the scenario range;
- the **cumulative capital required**, reported as the runway the idea needs. There is no founder-stated runway to compare against;
- which key assumptions are solid and which are speculative;
- the key risks.

## Scoring activated in this section

12 scores no commercial dimension. Conviction labels apply to every projection assumption. If the threshold result depends on a Low-conviction assumption (a churn rate, a CAC), say so plainly: 13 needs to know whether the financial picture rests on solid or speculative ground.

## Section-specific content for the four required parts

The four required parts are mandatory per `SKILL.md`.

### Analysis

Labelled subsections, in order: Inputs and window; Revenue projection; Cost projection; Scenarios; Threshold comparison; Key risks; Local lens; Synthesis.

**The projection table.** Present the numbers as a **structured table**: one row per year plus a cumulative-capital row, one column per scenario. The cells hold the revenue kept (and the gross, for pass-through models), total cost, profit or loss, and the cumulative-capital trough. Keep prose for the assumptions and the story.

### Recommendation

Always **"Proceed to 13."** No gate fires here.

Findings the founder should weigh are **recorded, not surfaced mid-run**: the expected case missing the threshold; a conservative case that changes the risk picture; a threshold result resting on Low-conviction assumptions; a large cumulative capital requirement; local-lens adjustments. Name them in the Rationale; 13 uses them.

### Rationale

Three to five sentences:
- the financial picture in brief;
- the threshold result, with magnitude and conviction;
- the cumulative capital required;
- how far the conservative and optimistic cases sit from the expected one.

### Challenge pass

The judging form from `SKILL.md` (06–13 omit the "non-obvious option" question), plus the section-specific questions below. Each finding uses the fixed short format: what changed and why, or "no change".

## Challenge pass: section-specific questions

- **Growth realism:** are growth assumptions grounded in comparable benchmarks? Check both failure directions: too aggressive in year 1, and too timid in year 3 if compounding is real.
- **Scaling-cost honesty:** if every cost scales linearly with revenue, the cost picture is probably understated.
- **Retention realism:** does retention reflect the model's structural pressures? Low switching costs and low contract values mean higher churn than first assumed.
- **Scenario honesty:** do the three scenarios test different assumption sets, or the same picture at three sizes?
- **Threshold rigor:** is it clear which scenario produces the conclusion, and is the revenue kept (not the gross) what is compared?
- **SOM consistency:** does any scenario outgrow, within its first 3 years, the market 06 sized? Is any later growth beyond it explained?

## Word cap

**Hard maximum (provisional): 1,500 words, excluding citation markers and the source list.** The projection table counts; it is mostly numbers.

## Downstream dependencies

What later sections consume from section 12:
- **13** uses the synthesis and the threshold comparison to interpret the commercial score. They feed the financial-coherence check (on borderline-band verdicts and on the high-commercial / weak-financial contradiction), the cumulative capital (reported as the runway the idea needs), the conviction picture and the key risks.
