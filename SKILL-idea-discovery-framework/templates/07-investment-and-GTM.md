# Template: 07 — Investment and GTM

## Purpose of this section in the framework

This section evaluates how the idea would be brought to market and produces the complete initial investment picture. It is the third section where a process gate can fire — the GTM gate from `SKILL.md` (no GTM strategy produces plausible unit economics). A kill recommendation here stops the framework before section 08 runs, which changes how this section is structured compared to sections that don't have a gate.

This section produces:
- A summary of upstream inputs the GTM analysis must work within
- A set of 2–4 candidate GTM strategies, evaluated against unit economics, runway, capital intensity, execution capacity, and target market fit
- A recommended primary GTM strategy (and any viable alternates)
- The complete initial investment picture combining build, compliance, GTM, and operating costs for the launch-and-early-traction window
- An evaluation against GTM gate's conditions, including an explicit adjustment-attempt step before concluding the gate fires
- A recommendation to proceed to section 08, surface concerns, or kill the idea per GTM gate

Section 07 does not score any commercial dimensions directly. Its outputs feed section 08's financial projections and section 09's decision. Conviction labels apply to CAC estimates, time-to-impact estimates, and investment numbers per the standing habit in `SKILL.md`.

The GTM gate fires *between* sections 07 and 08. If the GTM gate fires, section 08 is skipped and the framework proceeds directly to section 09 for the decision artifact.

## Brief fields relevant to this section

Before starting the analytical work, draw on these fields from `00-brief.md`:

- **Primary market:** GTM is heavily market-specific. Channels, CAC dynamics, and partnership ecosystems vary significantly by market. The local lens in Tasks 2, 3, and 6 applies the market context throughout the GTM analysis.
- **Recommended form factor (from section 03):** different form factors require different acquisition patterns. Mobile apps face app-store discovery dynamics; agent products face uncertain distribution channels; web apps depend on web-based acquisition.
- **Synthesized business model (from section 05):** the revenue model determines which GTM strategies fit. Subscription models optimize for CAC payback; transactional models optimize for transaction frequency; advertising models optimize for engagement.
- **Time and capital estimates (from section 06):** define the build component of initial investment and the realistic launch timeline.
- **Partnership requirements (from sections 04 and 06):** required partnerships affect both the investment picture and the GTM design (some partnerships create distribution channels; others are operational dependencies).
- **Depth overrides (if any):** acknowledge at the top of the section output. Common overrides: "explore B2B sales motion specifically," "skip paid acquisition analysis — not viable for me," "go deep on partnership-led GTM," "use a 9-month post-launch window — sales cycle is long."

If any of these fields are missing or unclear, surface the gap to the user before starting analytical work.

## Research activated in this section

Web search is mandatory in this section, especially for CAC benchmarks and channel costs. The local lens applies heavily to channel selection.

### Web search (mandatory)

Web search must produce, at minimum:
- Realistic CAC benchmarks for comparable products in the target market.
- Channel cost benchmarks (CPC, CPM, content marketing costs, sales motion costs by segment) for the channels under consideration.
- Recent shifts in channel effectiveness — ad platform changes, organic reach changes, partnership ecosystem changes — within the action window.
- Competitive GTM patterns: how do the incumbents identified in section 02 actually acquire customers? Public information on channel mix, sales motion, and acquisition strategy where available.

Cite sources directly. For CAC benchmarks especially, prefer industry-published data over informal "we grew to X" content.

### Deep research (user-confirmed)

Deep research is warranted when:
- GTM in this market or category is unclear and structured comparable research would meaningfully inform strategy.
- Multiple very different GTM strategies need quantitative comparison to determine the most viable.
- The recommended GTM depends on a channel or partnership ecosystem that requires investigation beyond surface-level search.

When any of these triggers fire, follow the deep-research escalation protocol in `SKILL.md`.

### Source quality

Conviction labeling follows the standard categorization from template 01. Industry-published CAC benchmarks → H. Aggregator and analyst reports → M. Blog posts and informal "we grew to X in Y" content → L.

**Be especially skeptical of GTM success stories.** Survivorship bias is severe in this category — the companies whose GTM didn't work don't write blog posts about it. A strategy described as "what worked for similar products" is selection-biased toward success. The relevant question is not "what worked for the successes" but "what's the realistic distribution of outcomes for products that tried this strategy?"

### Local lens for research

GTM is heavily market-specific. The local lens is structurally mandatory throughout this section, not just at Task 6.

Common defaults that mislead:
- Assuming US-equivalent channels work in other markets (Google Ads is universal where Google is dominant, but markets with strong local search alternatives have different dynamics).
- Assuming US-equivalent CAC ranges (CAC varies enormously by market, often correlated with revenue per user but not always in predictable ways).
- Assuming the same acquisition cost ratios across markets.
- Missing channels that don't exist in US/Europe but dominate locally — WhatsApp Business as primary B2B channel in some LatAm markets, KakaoTalk in Korea, WeChat in China, regional ad platforms in many markets.

Search using local channel names, local platform names, and local benchmark sources where possible.

## Analytical work for this section

These tasks together produce the **Analysis** portion of the section file. The Recommendation, Rationale, and Challenge pass are produced after the analytical work, drawing on it.

**Reminder of section scope** (full statement in Purpose subsection above): Section 07 produces the GTM strategy and the complete initial investment picture for the launch-and-early-traction window. It does not produce multi-year projections or scenario analysis (those belong in section 08).

The GTM gate evaluation in Task 7 is the outcome of synthesizing the findings and attempting adjustments — it is not a separate analytical exercise.

### Task 1: Establish inputs from upstream sections

Pull together the inputs this section needs:

- **Recommended business model (from section 05):** defines who's being acquired and how value capture works.
- **Unit economics sketch (from section 05):** defines what CAC the model can afford. A model with $X revenue per user over Y time can afford CAC up to some fraction of that, depending on the model type.
- **Compliance cost picture (from section 04):** defines the compliance component of initial investment — one-time costs plus ongoing compliance for the launch window.
- **Build time and capital (from section 06):** defines the build component of initial investment, plus the realistic launch timeline.
- **Solo-buildability picture (from section 06):** defines what GTM execution capacity is available. Solo execution constrains some channels (e.g., outbound sales motion at high volume requires more than one person to sustain).

The output of this task is a short summary of the constraints and inputs the GTM strategy must work within. This summary is reference material for the subsequent tasks — it does not pre-filter strategies, but it grounds the candidate generation in the cumulative picture from sections 03–06.

### Task 2: Generate candidate GTM strategies

Generate 2–4 candidate GTM strategies appropriate to the business model, form factor, and target market. The question is: *given who needs to be acquired and what the unit economics can support, what are the realistic paths to meaningful traction?*

To prompt thinking, common GTM patterns include (illustrative, not exhaustive):

- **Organic patterns:** SEO, content marketing, community-led acquisition, PR and earned media. Slow to compound, defensible long-term, time-heavy, capital-light.
- **Paid patterns:** search ads, social ads, programmatic, paid newsletter sponsorships. Fast, scalable with capital, requires creative and optimization capability.
- **Direct patterns:** outbound sales, founder-led sales, account-based marketing. Capital-light at low volume, capacity-heavy, fits B2B with high enough ACV.
- **Partnership patterns:** distribution partners, channel resellers, integrations, embeds, association partnerships. Depends on partnership development capability and partnership ecosystem availability.
- **Product-led patterns:** referrals, virality, freemium-to-paid, network effects. Depends on product properties that may or may not be present.
- **Hybrid patterns:** combinations of the above — common in practice, especially for ideas with mixed customer segments or different acquisition stages.

This list is starting prompts, not exhaustive. For each idea, ask: *who are the realistic potential customers, where do they already are, and what would meaningfully reach them?* Different ideas have different natural GTM patterns — some products are well-suited to specific patterns not in the list above (e.g., events-led acquisition for high-touch B2B, marketplace-led distribution for SMB products, geographic local-presence for regional businesses).

**Local context for candidate generation:** consider which GTM patterns are actually available and effective in the target market. Some patterns are universal where target users use the relevant channels (SEO is universal where target users use Google); some are market-specific (regional platforms, local channels, market-specific partnership ecosystems). Don't generate candidates that don't make sense in the target market — generating "Google Ads" as a candidate in a market where Google is not dominant is a wasted candidate slot.

For each candidate generated, characterize:
- **What it is:** the strategy in one sentence.
- **Channel(s) involved:** specific channels for this strategy.
- **CAC range:** realistic per-customer acquisition cost, drawn from benchmarks where available.
- **Time-to-impact:** how long from starting this strategy to seeing meaningful acquisition.
- **Capital intensity:** out-of-pocket costs to run this strategy effectively.
- **Execution capacity required:** what kind of capability is needed (referencing `user-profile.md` and section 06). Outbound sales motion needs different capacity than SEO; performance marketing needs different capacity than partnership development.

Apply default skepticism — survivorship bias is severe in GTM content, so a strategy that "worked" for similar products may not transfer. Generate at least 2 candidates even if one seems obviously right. The discipline is to consider real alternatives before settling, not to converge prematurely.

### Task 3: Evaluate each candidate against the unit economics and idea

For each candidate from Task 2, evaluate:

- **Can the unit economics afford this CAC?** Section 05 provided the per-unit revenue picture. This task asks whether this candidate's CAC fits within a recoverable payback window for the model. Specific guidance for the payback window evaluation is in Task 7; at this stage, surface whether CAC looks affordable, borderline, or unaffordable.
- **Does the time-to-impact match the runway?** A strategy that takes 18 months to compound is incompatible with a runway of 6 months. The runway is bounded by the user's capital availability (from the brief and section 06) and willingness to fund without traction.
- **Does the capital intensity fit?** A strategy requiring significant upfront marketing spend is incompatible with a low-capital plan.
- **Does the execution capacity match the user's profile?** Per section 06, the user has specific capabilities and constraints. A high-volume outbound sales strategy may not fit a solo-built product. A heavy creative-and-optimization paid acquisition strategy may exceed the marketing execution capacity in `user-profile.md`.
- **Fit with the target market:** does this specific candidate fit how acquisition actually works in the target market? This is a per-candidate check — does the channel/strategy assumed by this candidate match what works locally? Cross-cutting market factors that affect multiple candidates are handled separately in Task 6.

For each candidate, output: viable, viable with adjustments, or not viable, with reasoning.

### Task 4: Identify the recommended GTM strategy

Based on Task 3's evaluation, identify the recommended primary GTM strategy and any viable alternates. The recommendation should be the strongest candidate carrying viability across the evaluation dimensions in Task 3.

If Task 3's evaluation produced no viable candidates, note this — Task 7's gate evaluation will attempt adjustments before concluding the gate fires. Do not conclude that the gate fires at Task 4; that decision is made in Task 7 after the adjustment attempt.

### Task 5: Build the full initial investment picture

Combine cost components into the complete initial investment number for the "launch and reach early traction" window:

**Defining the window:** the window covered by this task is *MVP build time (from section 06) + a post-launch traction window*. The post-launch window is set by the business model rather than a fixed default:
- **~3 months** for consumer products with fast feedback loops (quick acquisition, short purchase cycles).
- **~6 months** for transactional and self-serve models (the general default).
- **~12 months** for B2B subscription or longer-sales-cycle models, where meaningful traction signal takes longer to appear.

Pick the window that matches the recommended business model (from section 05) and GTM (from this section). For a 3-month build with a 6-month post-launch window, the total is 9 months; with a 12-month window, 15 months. This window is the "launch and reach early traction" period — the time the user is funding before the business should either be self-sustaining or have a clear basis for raising more capital.

**Overrides:** the brief's depth-overrides field can override the model-based window if the idea's context calls for it — e.g., "use a 9-month post-launch window because the sales cycle is long." State the window used and whether it came from the model-based default or a brief override.

Components to combine:

- **Build cost (from section 06):** capital required to ship the MVP through to launch. Includes tooling, infrastructure during build, AI tokens for the build itself, paid services used during development.

- **Compliance cost (from section 04):** the full compliance picture for the defined window. Includes:
  - One-time compliance setup (entity formation, initial licensing, technical compliance implementation).
  - Ongoing compliance costs during the window (regulatory reporting, audits, licensing renewals, mandatory professional services tied to regulatory requirements).
  
  All compliance-driven costs go here, even if they're administered through legal or accounting service providers. This is the "if we weren't regulated, we wouldn't pay this" bucket.

- **GTM cost (from this section's Task 4 recommendation):** capital required to execute the recommended GTM strategy through the post-launch window. This is the GTM strategy in action — content production, ad spend, sales motion costs, partnership development costs. Includes only costs incurred to acquire customers; operational support of the product is in the operating bucket below.

- **Operating costs (from this section):** non-GTM, non-compliance operational costs for the defined window. Includes:
  - Infrastructure beyond MVP (post-launch hosting, scaling infrastructure, monitoring).
  - Customer support setup and ongoing customer support costs.
  - AI/LLM costs at expected post-launch volume.
  - General accounting and legal services not tied to regulatory compliance (e.g., bookkeeping, contract review, general legal consultation).
  - General business operations (banking, basic tooling, software subscriptions).
  
  This is the "running the business" bucket — costs the business would have whether regulated or not, and whether it had customers or not.

The output is a single initial investment number with components broken out, conviction-labeled. Show the components and the total — the breakdown is necessary for section 08's projections, which will model each component differently.

**Compare against the runway.** Check the total initial investment for the window against the brief's **runway** (the capital the user can deploy — the field referenced in Task 3). If the investment exceeds the runway, flag it: the idea needs more capital to reach traction than the user has said they can put in, a finding for section 09 (it may push a "pursue" toward "pursue with partnership / capital," or stand as a risk to monitor). If the brief gave no runway, report the investment number and note that no runway ceiling was provided.

**Scope of this task:** this is the cost to launch and reach early traction within the defined window. Specifically *not* included here:

- Capital required to scale beyond initial traction (covered in section 08).
- Multi-year cost projections beyond the window (covered in section 08).
- Scenario analysis or contingency capital (covered in section 08).
- Comparison against the make-money threshold (covered in section 08).

The question this task answers: *how much capital does the user need to get from "decide to build" to "see whether this works"?* Section 08 builds the picture beyond that point.

### Task 6: Apply the local lens — cross-cutting market factors

Task 3 evaluated each candidate's fit with the target market individually. Task 6 looks at cross-cutting market factors that affect GTM and investment design as a whole, beyond any single candidate:

- **Channel availability and effectiveness:** which channels actually work in the target market across the entire candidate space? Some channels are universal where target users use them; some markets have channels that don't exist elsewhere (regional ad platforms, local content platforms, market-specific social networks, dominant messaging platforms).
- **CAC and pricing dynamics:** CAC benchmarks from one market often don't transfer. Some markets have lower CAC but also lower revenue per user; some have specific bidding dynamics for paid channels; some have higher trust signals from word-of-mouth that change the math entirely.
- **Cultural patterns around purchasing:** B2B buying cycles, consumer trust signals, the role of word-of-mouth, sensitivity to advertising — all vary by market and affect multiple candidates simultaneously.
- **Partnership ecosystem:** the partnership landscape (distribution partners, integration platforms, channel partners, association memberships) differs significantly by market. Some markets have well-developed partnership ecosystems; others require building partnerships from scratch with no precedent.
- **Local execution constraints:** payment for ads, hiring marketing help, contracting with agencies — all have market-specific considerations that affect investment costs across candidates. Some markets have strong agency ecosystems; some markets require in-house execution because the agency capability isn't there.

Flag any cross-cutting findings that materially reshape the candidate evaluation or the investment picture. If a finding affects multiple candidates simultaneously, document the effect and revise the recommended GTM from Task 4 if appropriate.

### Task 7: Synthesize and evaluate against the GTM gate

Pull together findings from Tasks 1–6 into a coherent GTM and investment picture. The synthesis should characterize:

- The recommended primary GTM strategy with reasoning.
- Any viable alternates.
- The full initial investment picture.
- The realistic timeline from start to meaningful traction.
- Key risks in the GTM execution.

Apply the GTM gate from `SKILL.md`: does any GTM strategy produce plausible unit economics?

**Step 1: Evaluate candidates against unit economics.**

For each candidate from Task 4 (including the recommended primary and any alternates), check whether CAC is recoverable within the model's plausible payback window:

- **Subscription models:** CAC recoverable within 6–18 months of subscription revenue is typically plausible. Beyond that, the model is fragile to churn — small increases in churn rate push the recovery window beyond what the model can sustain.
- **Transactional models:** CAC should be recoverable within a small number of transactions or quickly through repeat usage. Single-transaction recovery is ideal; multi-transaction recovery within the first 3 months is acceptable.
- **B2B models:** longer payback windows are acceptable (up to 24 months) if the contract sizes and retention support it. ACV and net revenue retention determine the acceptable window — higher ACV and stronger retention permit longer payback.
- **Other models:** apply the equivalent logic — CAC must be recoverable in a window that matches how the model actually generates revenue.

**Step 2: If no candidate is recoverable, attempt adjustments before concluding the gate fires.**

Adjustments are organized from least to most aggressive — try less aggressive adjustments first, then more aggressive ones if those don't rescue the picture. Document each adjustment attempted and the result.

**Less aggressive adjustments:**

- **Different channel within the same strategy:** paid acquisition spans many channels with different costs; outbound sales spans different motion intensities; partnership development spans different partner types. Investigate whether a different channel within a strategy changes the CAC picture.
- **Different business model adjustment:** modest price change, bundling, tier restructuring — adjustments that don't require revisiting section 05's full analysis. A 20% price increase that brings CAC within recoverable range is an adjustment; a fundamental rework of the business model is not.

**More aggressive adjustments:**

- **Different customer segment within the same audience:** different segments often have different CAC and revenue per user. A downmarket segment may have lower CAC but lower revenue; an upmarket segment may have higher CAC but much higher revenue and longer retention. Investigate whether a different segment changes the picture.
- **Fundamentally different audience:** consumer instead of business, business instead of consumer, prosumer bridging the two. This is a larger shift than a segment change — it changes who the product is for. Only valid if the change still serves the original painpoint from section 01.
- **Different geographic strategy:** focusing on a subset of the target market where dynamics are different (specific city, specific region, specific industry vertical concentrated geographically). This may produce a viable GTM in a smaller market that doesn't apply across the full target.
- **Different model structures not yet tried:** unbundling, white-label, B2B2C through intermediaries, freemium with a much longer free runway. These are structural changes to the business model — only valid if they don't require fully revisiting sections 04 and 05.

If any adjustment produces a viable candidate, document the adjustment explicitly (including how aggressive it was — the user needs to know whether they're proceeding with a modest tweak or a fundamental change). GTM gate does not fire — proceed to section 08 with the adjusted picture.

**Step 3: Apply the GTM gate.**

The gate's firing condition is defined in `SKILL.md`'s kill model: **it fires when, after the Step-2 adjustment attempt, no candidate GTM strategy produces CAC recoverable within the model's plausible payback window** — the payback-window benchmarks (Step 1) and the adjustment menu (Step 2) are the analytical guidance for assessing it.

**GTM gate does NOT fire when:**

- A candidate produces recoverable CAC (the standard case).
- CAC is uncertain but plausibly recoverable — let section 08's full projections surface the issue if there is one.
- Adjustments in Step 2 produced a viable candidate.

If GTM gate fires, recommend kill and skip section 08 (per `SKILL.md`'s kill protocol). If not, finalize the recommended GTM and the full investment picture, and proceed.

## Scoring activated in this section

Section 07 does not score any commercial dimensions directly. Its outputs feed section 08's financial projections and section 09's decision. Conviction labels apply to the CAC estimates, time-to-impact estimates, and investment numbers per the standing habit in `SKILL.md`.

If a finding has Low conviction and is decision-relevant (i.e., it materially affects whether the GTM gate fires or whether the initial investment picture is plausible), surface this explicitly — this is the validation layer: validate or explicitly accept the load-bearing low-conviction claim before the decision stands. A kill based on Low-conviction CAC benchmarks is exactly the case where the challenge pass and the conviction-gated escalation matter most.

## Section-specific content for the four required parts

The four required parts (Analysis, Recommendation, Rationale, Challenge pass) are mandatory in the section file per `SKILL.md`. Below is what each part contains for section 07 specifically.

### Analysis

Subsections in order: Upstream inputs summary, Candidate GTM strategies, Candidate evaluation, Recommended GTM, Initial investment picture, Local lens (cross-cutting), Synthesized GTM and investment picture, GTM gate evaluation.

The Analysis subsections should read as a connected investigation, not disconnected blocks. The candidate evaluation explicitly draws on the upstream inputs summary and the unit economics from section 05. The investment picture combines components from sections 04, 06, and this section's GTM analysis. The local lens may modify the candidate evaluation. The synthesis pulls everything together for the GTM gate evaluation.

### Recommendation

Three possible recommendations from this section:

- **Proceed to section 08** — the standard case. GTM gate does not fire, a recommended GTM strategy is identified, and the full investment picture is established. Section 08 will build multi-year projections from this base.

- **Surface to user before proceeding** — GTM gate does not fire, but findings warrant user input. Specifically:
  - The recommended GTM materially differs from what the user assumed in the brief — e.g., the brief implied content-marketing-led growth, the analysis recommends outbound sales. The discrepancy itself is what should be surfaced.
  - CAC is recoverable but high relative to unit economics in ways the user should weigh before section 08 builds projections on that basis.
  - Investment number is significantly larger than the user anticipated, given the brief's framing.
  - Adjustments in Step 2 of GTM gate evaluation rescued the recommendation:
    - If the adjustment was *less aggressive* (different channel, modest business model tweak), note the adjustment in the rationale but proceed normally. The user may want to know, but the idea hasn't changed fundamentally.
    - If the adjustment was *more aggressive* (different segment, different audience, geographic shift, model structure change), surface to the user explicitly. The idea they're pursuing is now meaningfully different from what they specified in the brief — they should confirm before section 08 builds projections on that basis.
  - The local lens revealed cross-cutting market factors that materially reshape the GTM picture from what the upstream sections implied.

- **Recommend kill (GTM gate)** — the GTM gate's conditions explicitly apply per Task 7. Section 08 is skipped. The challenge pass applies to the kill itself.

In all cases except kill, do not stop the framework — surface the concern, get the user's input, then proceed. For kill, follow the kill protocol in `SKILL.md`: surface the recommendation with rationale and challenge pass, then confirm per the **conviction-gated rule** (autonomous auto-confirms at High/Medium conviction and escalates only if the kill rests on low-conviction evidence; checkpoint pauses) before writing to `09-decision.md`.

### Rationale

For a proceed recommendation, the rationale must include:
- The recommended primary GTM strategy in one sentence, with the channel and acquisition pattern.
- The full initial investment picture (total and component breakdown).
- The alignment with unit economics (CAC recoverable within the model's payback window).
- The realistic timeline from start to meaningful traction.

For a surface recommendation, the rationale includes the above plus the specific concern being surfaced and what the user is being asked to weigh.

For a kill recommendation, the rationale includes:
- The specific finding that triggers GTM gate (which candidates were considered, why each fails on the unit economics test).
- The adjustments attempted in Step 2 (organized by aggressiveness level) and why each failed to rescue the picture.
- The challenge pass output applied to the kill itself (see below).
- A note that this kill is confirmed per the conviction-gated rule in `SKILL.md`.

### Challenge pass

The standard four falsification questions from `SKILL.md` apply, plus the section-specific questions below.

For kill recommendations, the challenge pass is applied to the kill itself per `SKILL.md`'s kill model — the questions ask what would make the kill recommendation wrong, not just what would make the analytical findings wrong.

## Challenge pass: section-specific falsification questions

In addition to the standard four questions from `SKILL.md`, apply these to the GTM and investment analysis:

- **CAC-benchmark-realism check:** are the CAC benchmarks used in candidate evaluation actually from comparable products in the target market, or are they aspirational numbers from US-centric sources that may not transfer? A "comparable product" must share at least target market, segment, and acquisition pattern — a US enterprise SaaS CAC is not a benchmark for a LatAm SMB SaaS, even if the products look similar on the surface.

- **Survivorship-bias check:** is the recommended GTM strategy based on what worked for successful products, or has it been tested against what didn't work for products that failed? The companies whose GTM didn't work don't write the blog posts. If the strategy's evidence base is mostly success stories, the strategy is selection-biased — investigate the failures before relying on the strategy.

- **Execution-capacity-honesty check:** does the recommended GTM strategy actually fit the user profile and solo-buildability picture? A strategy that requires capabilities outside the profile is not viable, regardless of how attractive it sounds. "I'll learn paid acquisition" is a learning commitment, not an execution capacity — and learning paid acquisition while also building the product is rarely realistic.

- **Investment-completeness check:** does the initial investment picture include all real costs — build + compliance + GTM + operating — or has something been missed? Common omissions: AI token costs at meaningful scale (not just MVP-level usage), customer support infrastructure beyond founder-handled tickets, accounting and legal setup beyond initial compliance, hosting and infrastructure beyond the build budget, payment processing volume costs at post-launch volume.

- **Adjustment-honesty check (for GTM gate evaluations that ran Step 2 adjustments):** did the Step 2 adjustment actually produce a viable candidate, or did it require optimistic assumptions to make the math work? Adjustments that require stretching CAC benchmarks or revenue assumptions to make a candidate "viable" are not real adjustments — they're rationalizations that delay the GTM gate finding.

- **Workaround check (for GTM gate kill recommendations specifically):** *(Role: unlike templates 04 and 05 — which introduce new alternatives in their workaround checks — Step 2 of this section's gate evaluation already generates and tests adjustments, so here the workaround check is a thoroughness check on that Step 2 rather than a fresh alternatives search.)* Was Step 2 of the gate evaluation actually thorough? Specifically:
  - Did Step 2 attempt all categories from less aggressive (channel, business model adjustment) through more aggressive (segment, audience, geography, model structure)?
  - Were the more aggressive adjustments dismissed because they "wouldn't serve the original painpoint" or "would require revisiting upstream sections" — when those constraints are actually negotiable for the user?
  - Are there combinations of adjustments not tried (e.g., different audience + different model structure together) that might rescue the picture?
  
  If Step 2 was incomplete in any of these ways, the kill recommendation may not survive a thorough Step 2 attempt — revise.

Document the findings under the Challenge pass heading even if no changes were made to the analysis. If changes were made, note what changed and why.

## Depth calibration for this section

Section 07 is a heavy section. The work involves CAC benchmark research, candidate generation and evaluation, full investment assembly across multiple cost components, and the gate evaluation with its adjustment step. Total section length reflects this work, not bloat.

Normal depth range: ~900–1,400 words of substantive content (excluding headers and framework boilerplate). Comparable to section 02 in weight, heavier than section 05.

`SKILL.md`'s general ~600–800 word check-in threshold still applies as a self-check signal. For section 07, exceeding 600–800 words is expected — but the check-in remains useful: confirm at that point that the additional depth is contributing to the GTM gate decision or section 08's projections, not optimizing past the decision threshold.

Signs the section is too thin:
- Single GTM strategy considered, no real alternatives generated.
- CAC benchmarks absent or generic ("paid acquisition is expensive").
- Investment picture missing components (e.g., GTM cost not broken out from operating cost).
- GTM gate evaluation reduced to a sentence rather than structured application of the three-step process.
- Step 2 adjustments skipped when no candidate was initially viable.

Signs the section is too thick:
- Detailed channel execution plan that belongs in post-decision roadmapping (specific creative assets, week-by-week sales cadence, content calendar specifics).
- Exhaustive competitive GTM analysis that exceeds the strategic question (15-competitor channel mix breakdowns when 3 representative ones would inform the decision).
- Multi-year projections that belong in section 08.
- Specific tooling and vendor selection that belongs in execution planning.

If the brief specifies a depth override for this section, honor it and acknowledge it at the top of the output.

## Downstream dependencies

What later sections will consume from section 07:

- **Section 08 (Financial projections):** will consume the **Recommended GTM**, the **Initial investment picture**, and the CAC/payback context from the **Candidate evaluation** as primary inputs to financial projections. The initial investment number becomes the base from which multi-year capital requirements are projected. The CAC and unit economics together become the basis for scaling assumptions.
- **Section 09 (Decision):** will consume the **Synthesized GTM and investment picture** and **GTM gate evaluation** subsections for the final decision artifact. If GTM gate fired, section 09 receives the kill recommendation directly and produces the kill decision artifact. If the matrix lands in a quadrant requiring user action (partnership strategy, pursue with caveats), section 09 references this section's recommended GTM and investment picture for the action specifics.
