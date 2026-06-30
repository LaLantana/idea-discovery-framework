# Template: 05 — Business model

## Purpose of this section in the framework

This section evaluates how the idea can generate revenue within the legal envelope established by section 04. It is where the **Business-model gate** can fire. That gate has **two distinct causes**, which route differently: (a) *no model survives the legal envelope* (a structural / legal block — routes by commercial strength to a restructure / licensed partner, else kill) and (b) *no model has viable economics* — the **Monetization 0–2 commercial veto** (routes to a clean kill or a model pivot, never a partner). The section also scores the Monetization clarity dimension of the commercial score.

This section produces:
- A summary of the legal envelope as a constraint on business model design
- A set of 3–5 candidate revenue models, evaluated against the idea, the form factor, the target market, and the legal envelope
- A unit economics sketch for the strongest candidates
- A synthesized business model picture identifying the recommended primary revenue model (and any viable alternates)
- An evaluation against the Business-model gate's two causes (no-legal-model; no-viable-economics)
- A score on the Monetization clarity dimension of the commercial score
- A recommendation to proceed to section 06, surface concerns, or kill the idea per the Business-model gate

## Brief fields relevant to this section

Before starting the analytical work, draw on these fields from `00-brief.md`:

- **Primary market:** payment behaviors, subscription tolerance, and pricing expectations vary significantly by market. The local lens in Task 5 applies the market context to business model viability.
- **Recommended form factor (from section 03):** different form factors structurally constrain or enable different business models. The form factor determines part of the design space for Task 2.
- **Make-money threshold:** used implicitly here. Section 05's job is to identify viable unit economics; the explicit comparison against the threshold happens in section 08's projections.
- **Depth overrides (if any):** acknowledge at the top of the section output. Common overrides: "explore subscription models specifically," "skip ad-based models — not aligned with my vision," "focus on B2B pricing dynamics."

If any of these fields are missing or unclear, surface the gap to the user before starting analytical work.

## Research activated in this section

Research is discretionary in this section. Most of the analytical work can be done from the form factor, the legal envelope, and the local market context already established in sections 01–04. Specific findings warrant searching.

### Web search (discretionary)

Use web search when:
- Industry-typical revenue models in adjacent products would inform candidate generation (Task 2).
- Pricing benchmarks for comparable offerings would sharpen unit economics estimates (Task 4).
- Monetization patterns specific to the target market are uncertain — willingness-to-pay, subscription adoption rates, payment infrastructure norms.
- Recent shifts in monetization (subscription fatigue in certain categories, ad model changes, platform fee shifts) could affect the candidate evaluation.

### Deep research (user-confirmed)

Rarely warranted in this section. Possible exception: ideas in industries with unusual or rapidly-shifting monetization patterns (e.g., emerging AI product categories, regulated marketplaces) where structured investigation of comparables would meaningfully sharpen the analysis. When warranted, follow the deep-research escalation protocol in `SKILL.md`.

### Source quality

Conviction labeling follows the standard categorization from template 01. Industry reports and company filings (revealing actual revenue mix) → H. Aggregated pricing data and analyst reports → M. Blog posts, pricing-page screenshots, and informal benchmarks → L. Cite sources directly.

## Analytical work for this section

These tasks together produce the **Analysis** portion of the section file. The Recommendation, Rationale, and Challenge pass are produced after the analytical work, drawing on it.

**Scope reminder before starting:** Section 05 does not produce a full financial projection (that's section 08) and does not score CAC or full fixed-cost picture (those come later). Its scope is whether viable unit-level economics exist within the legal envelope. Tasks 1–6 below operate within this scope.

The Business-model gate evaluation in Task 6 is the outcome of synthesizing the findings from earlier tasks — it is not a separate analytical exercise.

### Task 1: Summarize the legal envelope from section 04

Read the Synthesized structural picture from section 04 (focus on its legal-envelope component — the regulatory constraints on business models) and produce a short summary of constraints on business models for reference during Tasks 2–4. Include:

- Revenue models prohibited by regulation (if any).
- Revenue models requiring specific licensing the user has not yet obtained.
- Structural requirements that shape monetization (e.g., money transmitter rules affecting transaction-fee models, healthcare regulations affecting consultation-fee models).
- Compliance costs from section 04 that will be relevant to unit economics in Task 4 (e.g., per-transaction KYC fees, ongoing reporting costs that scale with usage).

The summary is reference material for the subsequent tasks. It does not pre-filter candidates — candidate revenue models are generated in Task 2 and evaluated against this envelope as part of Tasks 2 and 3. A candidate that needs adjustment to fit the envelope is not the same as a candidate that's prohibited; the adjustment is part of the analysis.

### Task 2: Generate candidate revenue models

Generate 3–5 candidate revenue models from the idea's actual characteristics — what value it creates, who experiences that value, when payment makes sense relative to value delivery. The question is: *given this specific product in this specific market, who would pay for what and when?*

To prompt thinking, common revenue model patterns include (illustrative, not exhaustive):

- **Subscription patterns:** per-user, per-organization, tiered, usage-based subscription.
- **Transactional patterns:** commission, take-rate, per-transaction fee.
- **Marketplace patterns:** fees on both sides of a two-sided market.
- **Advertising patterns:** display, sponsored placement, affiliate, lead generation.
- **Licensing patterns:** white-label, API, data licensing.
- **Service patterns:** consulting, implementation, professional services bundled with the product.
- **Freemium patterns:** free tier with paid features, conversion-based.
- **Data patterns:** selling aggregated insights to third parties.
- **B2B2C patterns:** selling to intermediaries who pass cost to end consumers.
- **Hybrid and novel patterns:** combinations of the above, or patterns emerging in newer categories (e.g., agentic commerce revenue shares, AI-specific usage-based pricing).

This list is starting prompts, not exhaustive. For each idea, ask: *what's the natural moment of payment for this product in this market?* Different ideas have different natural moments — some align cleanly with one pattern, others require combinations, others fit emerging patterns that don't yet have established names.

For each candidate generated, characterize briefly:
- **What it is:** the model in one sentence.
- **Who pays:** the payer (user, intermediary, advertiser, partner).
- **What triggers payment:** the action or condition that generates revenue.
- **Envelope check:** does this model fit within the legal envelope from Task 1, require adjustment to fit, or fall outside it entirely? Flag the result.

Apply default skepticism — the first plausible-sounding model is rarely the best one. Generate at least 3 candidates even if the first feels obviously right. The discipline is to consider real alternatives before settling, not to converge prematurely.

### Task 3: Evaluate each candidate against the idea

For each candidate revenue model that's within (or adjustable to) the legal envelope, evaluate:

- **Fit with the painpoint:** does this model align with when users experience value? Models that bill users before value is delivered create friction. Models that capture value at a different point than where users perceive the benefit can feel disconnected (e.g., subscription for a tool used once a quarter).

- **Fit with the form factor:** does this model work with what the user would actually be building? Distinguish two kinds of fit:
  - **Structural constraints:** form factor characteristics that make a model harder or impossible. Browser extensions struggle with B2B contracts because they lack organizational deployment paths. Mobile apps face app-store payment rake on subscriptions (typically 15–30%). Web apps face cart abandonment dynamics that transactional models must accommodate.
  - **Market-empirical constraints:** form factor characteristics with uncertain market behavior. Agent products in 2026 face uncertain subscription tolerance — nothing structural prevents subscriptions, but user willingness is unclear. Note both types of consideration explicitly.

- **Fit with incumbent monetization patterns:** how do existing players in this space monetize? Significant divergence from incumbent patterns is not automatically wrong — it can be a differentiator — but warrants explicit justification. "We'll use a different model" is a claim that needs support, not a default.

- **Fit with the target market:** does this specific candidate fit how purchasing works in the target market? This is a per-candidate check — does the payment behavior this model assumes match what users in this market actually do? Cross-cutting market factors that affect multiple candidates are handled separately in Task 5.

Output for each candidate: a short evaluation noting strengths, weaknesses, and any compliance considerations from the legal envelope. Identify 2–3 strongest candidates to carry into Task 4.

### Task 4: Estimate unit economics for the most promising candidates

For the 2–3 strongest candidates from Task 3, produce a unit economics sketch at order-of-magnitude:

- **Revenue per relevant unit:** how much revenue does this model generate per user, per transaction, per organization, per whatever unit the model is built on?
- **Direct cost per unit:** what does it cost to serve one unit? Include:
  - LLM API costs if applicable. Agent products and AI-heavy products have meaningful per-interaction costs that vary significantly with usage patterns — a single short LLM call costs fractions of a cent, while a multi-turn conversation with tool use and large context windows can cost dollars per session. Estimate based on the realistic usage pattern for this product, not a generic "LLM cost."
  - Payment processing fees (typically 2–4% for card payments, varies by market).
  - Compliance costs that scale with usage (per-transaction KYC fees, regulatory reporting fees).
- **Unit margin direction:** is the model plausibly profitable per unit before fixed costs, or does the math break?

**Scope of this task:** this is a sketch to evaluate model viability, not a financial projection. Specifically *not* included here:
- Customer acquisition cost (CAC is covered in section 07).
- Fixed costs (infrastructure, personnel, ongoing fixed compliance costs) — covered in section 08.
- Multi-year projections, scaling assumptions, or scenario analysis — covered in section 08.
- Comparison against the make-money threshold — covered in section 08.

The question this task answers: *given the realistic per-unit revenue and direct costs, does this model have a viable path to profitability, or does it break before fixed costs even enter the picture?*

A model with negative unit margins at scale is not viable regardless of how attractive it sounds. A model with thin but positive unit margins may be viable depending on what section 08's full picture shows.

Conviction labels apply — explicit estimates with thin evidence get L conviction. The local market is a frequent L-conviction zone here: pricing benchmarks from adjacent markets may not transfer, and willingness-to-pay data for new categories is often unavailable.

### Task 5: Apply the local lens — cross-cutting market factors

Task 3 evaluated each candidate's fit with the target market individually. Task 5 looks at cross-cutting market factors that affect business model design as a whole, beyond any single candidate:

- **Payment infrastructure:** what payment methods are available and trusted in the target market? Credit card-dependent models may struggle in cash-heavy or alternative-payment-heavy markets. This affects multiple candidates simultaneously.
- **Subscription tolerance:** willingness to subscribe varies significantly by market and category. Note where the broader analysis assumes subscription behavior that may not exist locally — this affects all subscription-style candidates, not just one.
- **Pricing expectations:** ARPU expectations vary by market. A pricing baseline calibrated to US benchmarks may be wrong for emerging markets in either direction. This affects the unit economics in Task 4 across all candidates.
- **Cultural patterns around payment:** expectation of free consumer services in certain categories, B2B payment delays as standard, preference for one-time vs. recurring, cash-handling norms in transactions. These shape the design space, not just specific candidates.
- **B2B vs. B2C dynamics:** the divide between B2B and B2C purchasing behavior can be sharper in some markets than others. Note where the analysis assumes purchasing dynamics that may differ locally.

Flag any cross-cutting findings that materially reshape the candidate evaluation. If the local lens reveals a constraint that affects multiple candidates (e.g., the target market has very low subscription tolerance across all categories), that's a system-level finding that may shift the recommended primary model.

### Task 6: Synthesize and evaluate against the Business-model gate

Pull together the findings from Tasks 1–5 into a coherent business model picture for the idea. The synthesis should characterize:
- Which revenue models are viable within the legal envelope.
- Which of those have positive unit economics at the order-of-magnitude estimate.
- Which align with the form factor and target market.
- The recommended primary revenue model (the strongest candidate carrying viability across all four dimensions).
- Any viable alternates worth keeping in consideration.

Apply the **Business-model gate** from `SKILL.md`: is there any viable business model within the legal envelope? The gate's two firing causes — **(a) no model survives the legal envelope** and **(b) no model has viable economics** (the Monetization 0–2 veto) — are defined in `SKILL.md`'s kill model. Identify *which* one fires, because they route differently (per `rubric.md`'s veto routing): cause (a) routes **by commercial strength** — a restructure / licensed partner if the commercial case is strong, otherwise kill; cause (b) is a commercial veto and routes to a **clean kill** or a **model pivot** (a different payer / value-capture / timing — a re-brief), **never** a partner (a partner cannot rescue genuinely broken economics).

**The gate does NOT fire when:**
- A viable model exists with plausibly positive unit margins, even if margins are thin.
- Multiple candidates work and the question is which to prioritize (that's a decision for the user, not a kill).
- Unit economics are uncertain but plausibly positive — let section 08's full picture surface the issue if there is one.

If the gate fires, recommend kill (routed per the cause above). If not, identify the recommended primary revenue model (and any viable alternates) and proceed.

## Scoring activated in this section

### Monetization clarity dimension

Score the Monetization clarity dimension on the 0–10 scale defined in `rubric.md`, with H/M/L conviction label.

Apply the Monetization-clarity anchors from `rubric.md` — the **canonical source** (this is a synced copy; the worked examples live there). Keep it in sync if the rubric's anchors change:
- High (8–10): At least one revenue model is obvious and proven in adjacent products. Target users (or intermediaries) demonstrably pay for similar things today.
- Medium (5–7): Plausible revenue model exists but isn't proven in this specific market or for this specific user. Requires testing.
- Low (0–4): No clear path to revenue, or all candidate paths require behaviors users don't currently exhibit.

The score reflects:
- The strength of the recommended primary revenue model (proven in adjacent products → high; plausible but unproven → medium; hypothetical → low).
- The quality of the unit economics evidence (clear positive margins with reliable benchmarks → high; positive but uncertain → medium; speculative or negative → low).
- The alignment with the legal envelope (clean fit → high; requires adjustment → medium; struggles even with adjustment → low).

When multiple revenue models are viable, score based on the strongest single candidate (the one most likely to be recommended as primary). Note in the score reasoning that monetization optionality exists — having multiple viable models is a positive signal even if it doesn't directly raise the score.

Conviction label reflects the evidence behind the model — proven adjacent comparables in the target market → H; plausible reasoning from analogous markets → M; hypothesis without external grounding → L.

A 0–2 score is the **Monetization commercial veto** — cause (b) of the Business-model gate. It does not feed a capped average; it fires the kill here (routed to a clean kill or a model pivot — never a partner). Apply the anchor honestly and score the evidence, not the consequence; the 2/3 line is a cliff.

## Section-specific content for the four required parts

The four required parts (Analysis, Recommendation, Rationale, Challenge pass) are mandatory in the section file per `SKILL.md`. Below is what each part contains for section 05 specifically.

### Analysis

Subsections in order: Legal envelope summary, Candidate revenue models, Candidate evaluation, Unit economics for strongest candidates, Local lens, Synthesized business model picture, Business-model gate evaluation. Then the Monetization clarity score with conviction label and brief reasoning.

The Analysis subsections should read as a connected investigation, not disconnected blocks. The candidate evaluation explicitly draws on the legal envelope summary and the form-factor recommendation. Unit economics draw on the top candidates from evaluation. The local lens may modify the candidate evaluation. The synthesis pulls all of these together for the Business-model gate evaluation.

### Recommendation

Three possible recommendations from this section:

- **Proceed to section 06** — the standard case. The Business-model gate does not fire, and a recommended primary revenue model is identified. The compliance picture from section 04 is consistent with the recommended model.

- **Surface to user before proceeding** — the Business-model gate does not fire, but findings warrant user input. Specifically:
  - The recommended model materially differs from what the user assumed in the brief — e.g., the brief implied subscription but the analysis recommends transactional. The discrepancy itself is what should be surfaced, with the user given a chance to confirm the analysis is on the right track before continuing.
  - Multiple viable models exist with different strategic implications, and the user's input would help pick the primary.
  - Unit economics are positive but thin enough to warrant the user's attention before section 06 starts scoping the build.
  - The local lens revealed market-specific constraints that materially shape the model in a way the user may not have anticipated.

- **Recommend kill (Business-model gate)** — one of the gate's two causes explicitly applies per Task 6. Route per the cause: cause (a) no-legal-model → **partner** (if commercial is strong and a restructure / licensed partner exists) or **kill**; cause (b) Monetization 0–2 → **clean kill or model pivot** (never partner). The challenge pass applies to the kill itself.

In all cases except kill, do not stop the framework — surface the concern, get the user's input, then proceed. For kill, follow the kill protocol in `SKILL.md`: surface the recommendation with rationale and challenge pass, then confirm per the **conviction-gated rule** (autonomous auto-confirms at High/Medium conviction and escalates only if the kill rests on low-conviction evidence; checkpoint pauses) before writing to `09-decision.md`.

### Rationale

For a proceed recommendation, the rationale must include:
- The recommended primary revenue model in one sentence.
- The unit economics summary (revenue per unit, direct cost per unit, unit margin direction).
- The alignment with the legal envelope and target market.
- The Monetization clarity score with conviction label.

For a surface recommendation, the rationale includes the above plus the specific concern being surfaced and what the user is being asked to weigh.

For a kill recommendation, the rationale includes:
- Which Business-model gate cause applies — (a) no model survives the legal envelope, or (b) Monetization 0–2 (no viable economics) — and the route it takes (partner/kill for (a); kill/pivot for (b)).
- The specific finding that triggers the condition (which candidates were considered and why each fails).
- The challenge pass output applied to the kill itself (see below).
- A note that this kill is confirmed per the conviction-gated rule in `SKILL.md`.

### Challenge pass

The standard four falsification questions from `SKILL.md` apply, plus the section-specific questions below.

For kill recommendations, the challenge pass is applied to the kill itself per `SKILL.md`'s kill model — the questions ask what would make the kill recommendation wrong, not just what would make the analytical findings wrong.

## Challenge pass: section-specific falsification questions

In addition to the standard four questions from `SKILL.md`, apply these to the business model analysis:

- **Incumbent-divergence check:** if the recommended model differs from how incumbents monetize, is the divergence justified or is it a red flag? "We'll use a different model" is sometimes a differentiator and sometimes a sign the model has been tried and abandoned by others who learned why it doesn't work. Investigate before accepting divergence as a feature.

- **Unit-economics-realism check:** do the unit economics include all real costs at the unit level — LLM API costs for agent products, payment processing fees, compliance costs from section 04 that scale with usage? A "positive unit margin" that excludes any of these is not a positive unit margin in practice.

- **Willingness-to-pay check:** is there evidence users actually pay for this kind of value, or is the model based on the assumption that they would? "Users would pay for this" without supporting evidence is hypothesis, not analysis. The willingness-to-pay claim needs grounding — adjacent product behavior, interview data, observed transactions, or explicit user statements.

- **Workaround check (for Business-model gate kill recommendations specifically):** *(Role: surface new business-model structures not generated during the analysis, to pressure-test the kill — the same role as the workaround checks in templates 04 and 07, with the form tuned to each section's structure.)* Are there business model structures not yet considered? Common ones to check:
  - **Different payer:** B2B2C instead of direct-to-consumer (selling to intermediaries who pass cost on).
  - **Different value capture:** data instead of usage (capturing value from aggregated insights rather than per-transaction).
  - **Different timing:** one-time purchase instead of recurring, or vice versa.
  - **Different bundle:** combining with services, hardware, or partnerships to create a viable economic structure.
  
  If a viable model exists outside the candidates evaluated, the kill recommendation may not survive — revise.

Document the findings under the Challenge pass heading even if no changes were made to the analysis. If changes were made, note what changed and why.

## Depth calibration for this section

Section 05 has many analytical subsections by design (legal envelope summary, candidate models, evaluation, unit economics, local lens, synthesis, gate evaluation). The total section file will be longer than templates with fewer analytical tasks. The relevant question is not the total length but whether each subsection is doing its work — a one-sentence subsection is too thin; a multi-paragraph subsection on a side issue is too thick.

Normal depth range: ~700–1,000 words of substantive content (excluding headers and framework boilerplate). Heavier than section 03, lighter than section 02.

`SKILL.md`'s general ~600–800 word check-in threshold still applies as a self-check signal — at that point, confirm the additional depth is contributing to the Business-model gate decision or downstream sections, not optimizing past the decision threshold.

Signs the section is too thin:
- Single revenue model considered, no real alternatives generated.
- Unit economics absent or reduced to "should work."
- Local lens absent or reduced to "the market is similar."
- Business-model gate evaluation reduced to a sentence rather than structured identification of which of its two causes fires.

Signs the section is too thick:
- Full financial model that belongs in section 08 (multi-year projections, scenario analysis, customer acquisition modeling).
- Exhaustive pricing analysis across many tiers when one or two would inform the unit economics question.
- Speculation about future market evolution that doesn't change the current scoring.
- Detailed go-to-market strategy that belongs in section 07.

If the brief specifies a depth override for this section, honor it and acknowledge it at the top of the output.

## Downstream dependencies

What later sections will consume from section 05:

- **Section 06 (Solo-buildability):** will consume the **Synthesized business model picture** subsection when scoping solo-buildability. Some models are buildable solo (subscription SaaS with self-serve onboarding); others require infrastructure or partnerships that affect the build effort (transactional models with payment processing, marketplace models with two-sided dynamics).
- **Section 07 (Investment & GTM):** will consume the **Candidate evaluation** and **Synthesized business model picture** subsections when designing GTM. Different revenue models require different acquisition strategies — subscription products optimize for CAC payback, transactional products optimize for transaction frequency, advertising products optimize for engagement.
- **Section 08 (Financial projections):** will consume the **Unit economics for strongest candidates** and **Synthesized business model picture** subsections as primary inputs to financial projections. The unit economics sketch becomes the base for the multi-year model.
- **Section 09 (Decision):** will consume the **Monetization clarity score** (with conviction label) when assembling the overall commercial score, and will reference the **Synthesized business model picture** and **Business-model gate evaluation** for the final decision artifact.
