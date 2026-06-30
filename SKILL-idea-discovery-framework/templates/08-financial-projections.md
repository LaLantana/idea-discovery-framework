# Template: 08 — Financial projections

## Purpose of this section in the framework

This section assembles the full multi-year financial picture for the idea. It is where the explicit comparison against the make-money threshold happens: section 05 produced unit economics, section 07 produced initial investment, and this section scales those into a multi-year revenue, cost, and profit trajectory.

No process gate fires in this section. The GTM gate in section 07 catches ideas where GTM cannot produce plausible unit economics; by the time section 08 runs, that test has been passed. Section 08's job is to surface whether the full multi-year picture meets the make-money threshold — but a "doesn't meet threshold" finding here is not a kill on its own. It feeds the commercial picture for the matrix in section 09.

**Relationship to the commercial score and matrix:** the commercial score for the matrix (in section 09) comes from dimension scores produced in sections 01–05. Section 08 does *not* produce a commercial score or modify the existing one. Instead, section 08 produces a financial picture that *contextualizes* the commercial score for the matrix decision.

Section 09 uses both pieces:
- The commercial score (numeric, from sections 01–05) determines matrix quadrant placement on the commercial axis.
- The financial picture (from section 08) informs the strategic interpretation of that placement — e.g., "high commercial score, but financial projection shows the threshold met only in optimistic scenarios" is a different strategic situation than "high commercial score with robust threshold achievement across scenarios."

Section 08 should produce the financial picture clearly enough that section 09 can use both pieces together without re-deriving the financial conclusions.

This section produces:
- Multi-year revenue projection scaled from section 05's unit economics and section 07's GTM strategy.
- Multi-year cost projection covering the build cost (year 1), ongoing operating costs, ongoing compliance, and ongoing GTM cost.
- Scenario analysis: conservative, expected, optimistic cases, each testing assumption-specific stories.
- Comparison against the make-money threshold from the brief, with magnitude and conviction qualifier.
- A coherent financial picture for section 09 to consume.

## Brief fields relevant to this section

Before starting the analytical work, draw on these fields from `00-brief.md`:

- **Primary market:** affects pricing benchmarks, growth rate assumptions, and cost inflation assumptions over the modeling window.
- **Make-money threshold:** the explicit comparison target. This is what section 08's projections are evaluated against in Task 5.
- **Recommended business model (from section 05):** determines the revenue structure being projected.
- **Recommended GTM (from section 07):** determines the acquisition pattern that drives revenue scaling.
- **Initial investment picture (from section 07):** provides the year 1 cost base from which multi-year projections extend.
- **Unit economics sketch (from section 05):** provides the per-unit basis for revenue projection.
- **Depth overrides (if any):** acknowledge at the top of the section output. Common overrides: "produce conservative case only — I want to see worst-realistic," "go deep on scaling assumptions," "skip detailed scenario analysis — give me the central case," "model 5 years instead of 3 — the ramp is long," "use 3-year window even if ramp is slow — that's the decision horizon I care about."

If any of these fields are missing or unclear, surface the gap to the user before starting analytical work.

## Research activated in this section

Research is mostly discretionary in this section — section 08 builds from inputs already produced by sections 05 and 07. Some research is warranted for scaling benchmarks and growth rate validation.

### Web search (discretionary)

Use web search when:
- Realistic growth rate benchmarks for comparable products in the target market are needed to validate the revenue projection.
- Retention and churn benchmarks for similar business models would sharpen the revenue assumptions.
- Scaling cost benchmarks (infrastructure scaling, support scaling, ops scaling) are uncertain.
- Industry-typical multi-year trajectories for similar products would help validate the overall picture.

### Deep research (user-confirmed)

Rarely warranted in this section. Possible exception: when the financial picture depends heavily on assumptions that need structured comparable investigation — e.g., scaling cost curves for a novel product category, retention dynamics in an emerging market segment. When warranted, follow the deep-research escalation protocol in `SKILL.md`.

### Source quality

Conviction labeling follows the standard categorization from template 01. Industry reports with multi-year financial data → H. Aggregated growth benchmarks and analyst reports → M. Blog posts about "we grew from X to Y" → L. Cite sources directly.

**Same survivorship-bias warning as template 07.** Financial growth stories overwhelmingly come from successful products. The companies whose financials didn't work don't write blog posts about their growth trajectories. If the projections lean heavily on "what worked for similar successful products," the projections are selection-biased toward success — investigate the realistic distribution before relying on the benchmarks.

## Analytical work for this section

These tasks together produce the **Analysis** portion of the section file. The Recommendation, Rationale, and Challenge pass are produced after the analytical work, drawing on it.

No gate fires here, so there's no synthesis-and-evaluate step at the end. Task 8 synthesizes the financial picture for section 09's consumption.

### Task 1: Establish inputs from upstream sections

Pull together the inputs this section needs:

- **Recommended business model and unit economics (from section 05):** revenue per unit, direct cost per unit, unit margin direction. These are the per-unit basis for revenue projection.
- **Initial investment picture (from section 07):** the build + compliance + GTM + operating cost for the launch window. Section 08's year 1 picture starts from this number.
- **Recommended GTM strategy and CAC (from section 07):** the acquisition pattern that determines how revenue scales over time.
- **Make-money threshold (from the brief):** the explicit comparison target. This is what section 08's projections are evaluated against in Task 5.
- **Time-to-MVP and launch timeline (from section 06):** determines when revenue begins in the multi-year picture. If MVP takes 6 months, revenue starts in month 7 at earliest.

**Modeling window choice:** before starting the projection work, decide on the modeling window — typically 3 years, occasionally 5 for businesses with longer ramp (e.g., B2B with multi-year sales cycles, products with significant time-to-traction, capital-intensive products with long payback). Document the choice and the reason. If the brief's depth overrides specify a window (e.g., "model 5 years instead of 3"), honor that.

The window choice affects every subsequent task — Tasks 2–8 all operate over this defined window. Once set, the window is fixed for this section's analysis.

The output of Task 1 is a short summary of the inputs, the modeling window, and the starting assumptions section 08 will use. This summary is reference material for subsequent tasks — it doesn't pre-filter projection logic but grounds the projections in the cumulative picture from sections 03–07.

### Task 2: Project revenue over the modeling window

Project revenue across the defined modeling window. Build the revenue projection from these inputs:

- **Customer acquisition rate:** how many customers per month or per quarter, based on the GTM strategy from section 07 and the CAC from that section. The acquisition rate is typically slow at first and ramps over time as the GTM strategy gains traction.
- **Revenue per customer over time:** revenue per relevant unit (from section 05), modeled across the customer's expected lifetime. Include retention curves (what fraction of customers remain active at month N) and expansion revenue if applicable (upsells, tier upgrades, usage-based growth).
- **Compounding effects:** if the GTM compounds (content marketing that builds an SEO base, referral programs that compound with customer count, network effects in the product), reflect this in the acquisition rate over time. Compounding is not automatic — only model it if there's a specific mechanism.

For each projection year, produce:
- **Customer count:** cumulative active customers at year-end (accounting for churn).
- **Revenue (gross):** total revenue generated during the year.
- **Net revenue:** revenue after refunds, churn-related credits, and any other deductions.

Apply default skepticism. Growth projections are notoriously optimistic — the most common failure mode is assuming acquisition rates that work for established products from day one of a new product. Use realistic ramp assumptions: most products take longer than projected to reach their target acquisition rate, and many never reach it.

Document the key assumptions explicitly with conviction labels — particularly the acquisition rate ramp, retention curve, and any compounding effects.

### Task 3: Project costs over the modeling window

Project costs for the same multi-year window, organized by category:

- **Initial investment (year 1):** drawn directly from section 07's Initial investment picture. Components: build cost, compliance cost, GTM cost, operating cost for the launch window.
- **Ongoing operating costs:** non-GTM, non-compliance operational costs that continue past year 1. Includes infrastructure scaling with usage, customer support scaling with customer count, AI/LLM costs scaling with usage, general operations costs that grow with the business.
- **Ongoing GTM costs:** the GTM strategy's costs continuing past the launch window. Paid acquisition scales with customer acquisition target; content marketing has different scaling (content production cost scales sub-linearly with audience growth); outbound sales scales with sales motion intensity.
- **Ongoing compliance costs:** the compliance picture from section 04 over the modeling window. Includes ongoing licensing renewals, audits, regulatory reporting.
- **Direct costs per unit:** payment processing, per-transaction compliance fees (e.g., KYC), per-interaction AI costs. These scale linearly with usage and become more material at scale.

For each projection year, produce:
- **Total costs broken into categories** (operating, GTM, compliance, direct unit costs).
- **Cost per customer:** as a sanity-check metric. If cost per customer is increasing year-over-year, investigate whether scaling is broken; if it's decreasing too rapidly, investigate whether assumptions are unrealistic.

**Be alert to costs that scale faster than linearly.** Common offenders: AI/LLM costs (interaction-heavy products can produce LLM costs that grow faster than revenue if pricing isn't usage-aligned), customer support costs (in some models support load grows faster than support tooling improvements), infrastructure costs at scale (crossing thresholds for data egress, database scaling, security/compliance). If any cost category is projected to grow faster than revenue, the model is unsustainable at scale and the projection should surface this as a finding.

### Task 4: Build scenario analysis

Build three scenarios that test different coherent stories about how the idea plays out. Each scenario is internally consistent — variables move together in ways that make sense for that scenario's story.

**Expected case:** the central projection using best-current-estimate assumptions. This is the "execution proceeds roughly as planned" picture.

**Conservative case:** the "execution is harder than expected in the ways that matter most for this idea" picture. The conservative case tests the 2–3 assumptions whose downside would most damage the financial picture. Identify these assumptions explicitly before building the scenario:

- For subscription models: CAC and churn typically dominate.
- For transactional models: transaction volume and frequency typically dominate.
- For B2B models: sales cycle length and ACV typically dominate.
- For ad-supported models: engagement and ad rates typically dominate.

Move these assumptions to honest "worse than expected" values. Other assumptions stay at expected unless they're causally linked (e.g., if higher CAC causally implies lower customer count, that linkage is preserved).

**Optimistic case:** the "execution goes well in the ways that matter most" picture. The same 2–3 dominant assumptions move to honest "better than expected" values. Again, other assumptions stay at expected unless causally linked.

For each scenario, produce:
- **Revenue trajectory** over the modeling window.
- **Cost trajectory** over the modeling window.
- **Profit/loss trajectory** (revenue minus costs).
- **Cumulative capital required** — the worst-case cash trough, i.e., the maximum negative cumulative cash position across the window. This is the number that tells the user how much capital they actually need.
- **Time to breakeven** if breakeven happens within the window. If not, note that breakeven happens beyond the modeling window and estimate when.

**On honest scenarios:** the conservative and optimistic cases should be honestly different from expected, not "expected ± 15%" with the same underlying logic. If the conservative case looks like a slight degradation of expected, the assumption-testing wasn't rigorous enough — go back and identify what would actually damage the picture, then test that.

A real conservative case answers the question: "what does it look like if the things that could go wrong, do?" A real optimistic case answers: "what does it look like if the things that could go well, do?" Both questions should produce materially different pictures from expected.

### Task 5: Compare against the make-money threshold

Apply the make-money threshold from the brief to the projections.

The output is a clear statement of threshold achievement that includes:
- **The scenario** (expected, conservative, optimistic).
- **The timing** (year 1, year 2, year 3, beyond window).
- **The magnitude relative to threshold** (e.g., "meets at 1.5× threshold," "meets at threshold," "40% below threshold").
- **The conviction** on the conclusion (H/M/L).
- **The key driver assumptions** for the conclusion (the 2–3 assumptions most responsible for the threshold result).

Example formats:

- "Meets in expected case at year 2 (M conviction) at approximately 1.3× threshold; meets in conservative case at year 3 (L conviction) at approximately threshold, driven by CAC and retention assumptions with thin local benchmarks."
- "Meets in expected case at year 2 (H conviction) at 2× threshold; meets in conservative case at year 3 (M conviction) at 1.4× threshold; meets in optimistic case at year 1 (M conviction) at 1.2× threshold."
- "Does not meet within the modeling window in any scenario. Gets closest in optimistic case at year 3 at 60% of threshold."

A high-confidence, high-magnitude threshold story (meets at 2× in expected case, H conviction) is a much stronger commercial picture than a low-confidence, marginal threshold story (meets at 1.0× in expected case, L conviction). Section 09's matrix decision can use both pieces.

### Task 6: Identify key risks and uncertainties

Identify the key risks in the financial picture, organized by what's at risk and by whether it's monitorable.

**By what's at risk:**

- **Revenue risks:** assumptions or factors that could cause revenue to underperform. Examples: CAC running higher than benchmark, churn higher than expected, conversion rates lower than expected, pricing pressure, slower acquisition ramp.
- **Cost risks:** assumptions or factors that could cause costs to run higher than projected. Examples: scaling costs compounding faster than linearly, infrastructure costs at scale, support costs at scale, AI/LLM costs at higher-than-projected usage volumes.
- **Timing risks:** assumptions or factors that could shift when revenue arrives or costs are incurred. Examples: slower MVP, slower ramp, longer sales cycle than expected, slower time-to-traction.

**By monitorability:**

- **Monitorable risks:** things the user can track during execution and respond to. CAC trending higher than benchmark in month 3 is something the user sees and can adjust to. Churn higher than projected in month 6 is visible in the data.
- **Structural risks:** things inherent to the business that aren't monitorable in real-time. A market shift, a regulatory change, a competitive entrant, a platform policy change. These can't be managed through execution adjustments — they're external conditions that must be absorbed or hedged against.

For each significant risk identified, note:
- **Which projection variable it affects** (revenue, cost, timing, or multiple).
- **How much it could move the picture** (small impact, material impact, breaking impact). Breaking impact = could change a "meets threshold" conclusion to "doesn't meet."
- **Whether it's monitorable** (can be adjusted to in execution) or **structural** (must be absorbed or hedged).

The output is a clear risk picture that section 09 can use to characterize the idea's risk profile in the final decision artifact.

### Task 7: Apply the local lens

How does the target market shape the financial projections?

- **Growth rate expectations:** market growth varies. The same business in a fast-growing market produces different projections than in a stable market. If the target market has known growth dynamics (rapidly expanding, mature, declining), reflect this in the revenue projection assumptions.
- **Pricing dynamics over time:** does pricing typically increase, decrease, or stay flat in this market for this category? Some markets have strong pricing pressure (commoditization, competition) that affects multi-year revenue. Others permit pricing power for differentiated products.
- **Cost inflation:** infrastructure costs, talent costs, marketing costs all evolve at different rates in different markets. A 3-year projection in a high-inflation market needs to account for this differently than in a low-inflation market.
- **Capital availability:** if external capital becomes relevant for scenarios beyond the expected case, what's the realistic capital market in the target market? Some markets have abundant capital for the category; others require atypical fundraising approaches.
- **Other market-specific factors:** anything else specific to the target market that materially affects the projections — currency volatility for multi-year cross-border projections, payment infrastructure changes, sector-specific market dynamics.

Flag any cases where the local lens revealed assumptions that need adjustment for the target market specifically. If the local lens materially changes the projections, document the adjustment and revise Tasks 2–5 as needed.

### Task 8: Synthesize the financial picture

Pull together findings from Tasks 1–7 into a coherent financial picture for section 09's consumption:

- **The expected-case picture:** revenue trajectory, cost trajectory, profit trajectory, threshold achievement, cumulative capital required.
- **Cumulative capital vs. runway:** compare the cumulative capital required (the cash-trough number from Task 4) against the brief's **runway**, if given. If it exceeds the runway, say so — the idea needs more capital than the user can deploy, which section 09 weighs (it can push a "pursue" toward partnership/capital, or stand as a risk to monitor). If the brief gave no runway, report the cumulative capital and note that no ceiling was given.
- **The scenario range:** how do conservative and optimistic cases compare? Where does the conservative case break the threshold story, and how far above does the optimistic case land?
- **The threshold story:** does this meet the make-money threshold, when, at what magnitude, and under what conditions? Include conviction.
- **The conviction picture overall:** which key assumptions are high-conviction (supported by clear benchmarks or evidence) and which are low-conviction (estimates with thin evidence)? Section 09 needs to know whether the financial picture rests on solid or speculative ground.
- **The key risks:** what could derail the picture — both monitorable risks the user can manage and structural risks that must be absorbed.

The synthesis is what section 09 will reference when describing the commercial picture in the final decision artifact. It should be readable as a standalone story about the financial trajectory, not just a recap of the analytical work.

## Scoring activated in this section

Section 08 does not score any commercial dimensions directly. Section 09 will assemble the overall commercial score from the dimension scores produced in sections 01–05. Section 08's outputs inform section 09's interpretation of that commercial score in light of the actual financial picture.

Conviction labels apply to the projections per the standing habit in `SKILL.md`. Assumptions with thin evidence get L conviction. A projection with L-conviction key assumptions should be surfaced as such — the user needs to know whether the financial picture rests on solid or speculative ground before section 09 makes the matrix decision.

If decision-relevant findings have Low conviction (e.g., threshold achievement depends on an L-conviction churn assumption), surface this explicitly. A high-confidence financial picture and a low-confidence one are different inputs to the matrix.

## Section-specific content for the four required parts

The four required parts (Analysis, Recommendation, Rationale, Challenge pass) are mandatory in the section file per `SKILL.md`. Below is what each part contains for section 08 specifically.

### Analysis

Subsections in order: Upstream inputs summary, Revenue projection, Cost projection, Scenario analysis, Threshold comparison, Key risks and uncertainties, Local lens, Synthesized financial picture.

The Analysis subsections should read as a connected investigation, not disconnected blocks. The revenue and cost projections share assumptions and feed the scenario analysis. The threshold comparison draws on the scenarios. The risks reference the assumptions that drive the projections. The local lens may modify multiple subsections. The synthesis pulls everything together for section 09.

**Output format — projection table.** Present the projections as a **structured table**, not prose paragraphs: rows = the modeling years plus a cumulative-capital row; columns = the three scenarios (conservative / expected / optimistic); cells = the key figures (net revenue, total cost, profit/loss, and the cumulative-capital trough). Keep prose for the *assumptions and the story* — what drives each scenario, the threshold comparison, the conviction picture — but the numbers themselves go in the table. This is the one section where prose alone fails the data (per `SKILL.md`'s output-format note).

### Recommendation

Two paths — no kill option from this section:

- **Proceed to section 09** — the standard case. The financial picture is built, scenarios analyzed, threshold comparison made. Section 09 will make the matrix decision using both the commercial score and this section's financial picture.

- **Surface to user before proceeding** — when the analysis surfaced findings the user should see:
  - **The expected case doesn't meet the make-money threshold within the modeling window.** This is not a kill from section 08 — section 09's matrix evaluation will handle the commercial picture overall. But the user should know about the threshold gap before section 09 runs, in case they want to revise assumptions, adjust the threshold, or confirm they're prepared for a likely "low commercial" matrix outcome.
  - The conservative case is significantly different from the expected case in a way that materially changes the risk picture.
  - Key assumptions have L conviction and significantly affect threshold achievement. The user should know whether the financial picture rests on solid or speculative ground before section 09 makes the matrix decision.
  - The cumulative capital required is significantly larger than what the user implied in the brief.
  - The local lens revealed assumption adjustments the user should review.

In all cases, do not stop the framework — surface the concern, get the user's input, then proceed.

### Rationale

For a proceed recommendation, the rationale must include:
- The synthesized financial picture in one or two sentences.
- The threshold achievement summary with magnitude and conviction.
- The cumulative capital required.
- The scenario range (how different conservative and optimistic are from expected).

For a surface recommendation, the rationale includes the above plus the specific concern being surfaced and what the user is being asked to weigh.

### Challenge pass

The standard four falsification questions from `SKILL.md` apply, plus the section-specific questions below.

## Challenge pass: section-specific falsification questions

In addition to the standard four questions from `SKILL.md`, apply these to the financial projections:

- **Growth-rate-realism check:** are the growth rate assumptions actually grounded in comparable benchmarks, or are they aspirational? Most projections fail in two opposite directions: too aggressive in year 1 (assuming the GTM works immediately) and not aggressive enough in year 3 (failing to account for compounding when it does work). Check both.

- **Scaling-cost-honesty check:** do the cost projections account for costs that scale faster than linearly? AI/LLM costs, support costs in some models, infrastructure costs at scale — these can compound faster than expected. If the model's costs all scale linearly with revenue, the cost picture is probably understated.

- **Retention-and-churn-realism check:** are retention assumptions tested against the model's structural retention pressures? Subscription models with low switching costs typically have higher churn than initial projections assume. B2B products with low contract values typically churn faster than enterprise products. Check that retention reflects the model's structural dynamics.

- **Scenario-honesty check:** are the conservative and optimistic scenarios honestly different from the expected case, or are they "expected ± 15%" with the same underlying assumptions? Real scenarios test *different assumption sets*, not different magnitudes of the same assumptions. If the three scenarios look like the same picture at three different sizes, the scenario-building wasn't rigorous.

- **Threshold-comparison-rigor check:** is the threshold comparison rigorous, or is it producing "yes, this meets the threshold" by selecting favorable interpretations? The threshold comparison should be honest about which scenario is producing the conclusion. "Meets in optimistic case" is a much weaker conclusion than "meets in expected case" — don't conflate them.

Document the findings under the Challenge pass heading even if no changes were made to the analysis. If changes were made, note what changed and why.

## Depth calibration for this section

Section 08 is the heaviest analytical work in the framework — multi-year projections with three scenarios, threshold comparison, and risk picture. The total section file will be long by design, not bloat.

Normal depth range: ~1,000–1,500 words of substantive content (excluding headers and framework boilerplate). Comparable to or heavier than section 07.

`SKILL.md`'s general ~600–800 word check-in threshold still applies as a self-check signal — confirm at that point that the additional depth is contributing to the threshold comparison or section 09's matrix decision, not optimizing past the decision threshold.

Signs the section is too thin:
- Single scenario instead of three.
- Cost projection that doesn't reflect scaling — costs growing at the same rate as revenue.
- Threshold comparison without magnitude or conviction qualifier.
- Local lens absent or generic.
- Risks listed without monitorability or impact size.

Signs the section is too thick:
- Year-by-year detailed cost line items at sub-component level (specific software subscription costs broken out, etc.).
- Multiple scenarios that differ only in magnitude, not in assumption logic.
- Sensitivity analysis on dimensions that don't materially affect threshold achievement.
- Detailed financial modeling that exceeds the strategic question — section 08 is not a board-ready financial model, it's enough analysis to make a decision.

If the brief specifies a depth override for this section, honor it and acknowledge it at the top of the output.

## Downstream dependencies

What later sections will consume from section 08:

- **Section 09 (Decision):** will consume the **Synthesized financial picture** and **Threshold comparison** subsections as primary inputs to the matrix decision and the final decision artifact. The cumulative capital required and the scenario range inform whether the matrix decision is "pursue immediately" vs. "pursue with caveats" vs. matrix-driven kill. The conviction qualifier on the threshold conclusion affects how confidently section 09 can characterize the financial picture.