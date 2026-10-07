# Template: 09 — Business model

## Purpose of this section in the framework

Section 09 judges whether **the idea's own revenue model**, as fixed in 05's handoff, works: inside the legal envelope from 08, and at the unit level. It is where the **Business-model gate** can fire, and it scores the **Monetization clarity** dimension. It also runs the **locked-average check** that can end the idea's evaluation early.

This section produces:
- A check of the idea's revenue model against 08's legal envelope
- An evaluation of the model's fit with the problem, the form factor, incumbents and the market
- The pricing structure within that model, and a unit-economics sketch
- A score on the **Monetization clarity** dimension, and the locked-average check
- A recommendation: proceed to 10 (with a partner or a different legal structure, if cause (a) routed there), early exit to 13 (locked average), or a kill of this idea at the Business-model gate

**09 does not generate revenue models.** Who pays, what is sold and the payment pattern (subscription, transaction, licence…) were fixed in 04 and 05. 09 evaluates them and works out the pricing within them: price level, tiers and what drives cost. A different payer, product or payment pattern is a different idea, and those already exist in 04 (`SKILL.md`, "No alternatives after the screen").

Section 09 does not build financial projections (12), estimate customer acquisition (11), or compare against the threshold (12). Its question is narrower: *does this model work at the unit level, inside the legal envelope?*

## Inputs

- **05's handoff:** what is sold, who pays, for what and when; the market.
- **08:** the legal envelope, any compliance costs that scale with usage, any partner route (its cut or fees go into the unit economics) and its Moat candidates line.
- **06 and 07:** the Problem severity and Market size scores, and 07's Moat candidates line, for the locked-average check.
- **07:** the form factor.
- **06:** incumbents' pricing and how they make money.
- **03:** the pinned key figures, e.g., what people spend on the problem today.

## Research activated in this section

**Ordinary web search, discretionary.** Use it for:
- pricing benchmarks for comparable offerings in the idea's market;
- payment behaviour in that market: willingness to pay, subscription adoption, payment methods;
- recent shifts that affect the model (subscription fatigue in the category, platform-fee changes).

Deep research is rarely warranted; a possible exception is a category whose monetization is unusual or shifting fast. Follow the pause in `SKILL.md`, "Research and deep research".

**Source quality and fact discipline.** Company filings and industry reports showing actual revenue mix → H. Aggregated pricing data and analyst reports → M. Pricing-page screenshots and informal benchmarks → L. Willingness-to-pay and unit-cost benchmarks are load-bearing and often thin: cite each at the point of use, pin a price or margin figure once and reuse it, and add "people pay for X" claims to the claims-to-verify list. No blanket "no one will pay for this" (or "people clearly pay") without the evidence inline.

## Analytical work for this section

### Task 1: Check the model against the legal envelope

From 08's structural picture, state whether the idea's revenue model:
- **fits** the envelope as it is;
- **fits with adjustment** within the same model (for example, adding a required disclosure, or running payments through a licensed processor); or
- **does not survive** it (the model itself is prohibited, or needs a licence or structure specific to this model that 08 did not already route).

Carry forward any compliance costs that scale with usage (per-transaction KYC fees, usage-linked reporting) into Task 4.

### Task 2: Evaluate the model's fit

- **Fit with the problem:** does payment fall when users get value? Billing before value is delivered creates friction; a monthly subscription for something used once a quarter feels disconnected.
- **Fit with the form factor:**
  - *structural constraints:* app-store fees of 15–30% on mobile subscriptions; browser extensions lack organizational sales paths; checkout abandonment affects web transactions;
  - *market-empirical uncertainty:* for example, how willing people are to pay a subscription for an agent product.
- **Fit with incumbent monetization:** how do 06's incumbents make money? Diverging from them can be a differentiator, or a sign that others tried this and learned why it fails. Divergence needs a reason.
- **Fit with the market:** does the payment behaviour this model assumes match what people in this market actually do?

### Task 3: Set the pricing structure within the model

Within the model as given, set the price level and structure (for example, tiers, per-seat versus flat, or the take rate), grounded in 06's incumbent pricing and the research. Keep it to what the unit economics need: one or two price points, not an exhaustive tier analysis.

### Task 4: Sketch the unit economics

At order of magnitude, per the unit the model is built on (user, transaction, organization):
- **Revenue per unit.** For pass-through models (marketplaces, resellers, agencies), show the gross value per unit, the take rate and the **revenue the business keeps**.
- **Direct cost per unit:**
  - *AI and LLM costs* where relevant, estimated from the realistic usage pattern. A short call costs fractions of a cent; a multi-turn session with tools and large context can cost dollars.
  - *Payment processing:* typically 2–4% for cards, varying by market.
  - *Compliance costs that scale with usage* (from Task 1).
- **Unit margin direction:** plausibly positive before fixed costs, or does the math break?
- **Per customer per period:** contribution margin per customer per month (or per transaction, with the expected purchase frequency), and the retention or repeat basis behind it, with conviction. 11 tests payback against it.

**Not included here:** acquisition cost (11), fixed costs, multi-year projections and the threshold comparison (all 12). A model with negative unit margins at any plausible scale is not viable however attractive it sounds; thin but positive margins may be viable depending on 12.

Label conviction honestly. The local market is a frequent Low zone: benchmarks from other markets may not transfer.

### Task 5: Apply the local lens

Cross-cutting market factors that affect the model as a whole:
- **Payment infrastructure:** which payment methods are available and trusted? Card-dependent models struggle in cash-heavy or alternative-payment markets.
- **Subscription tolerance** in this market and category.
- **Pricing expectations:** revenue-per-user expectations differ by market, in either direction, from US benchmarks.
- **Cultural payment patterns:** an expectation of free consumer services, slow B2B payment, a preference for one-off over recurring payment.
- **B2B versus B2C dynamics**, which can differ sharply by market.

### Task 6: Evaluate against the Business-model gate

Apply the gate's two causes, canonical in `SKILL.md`, "The kill model":
- **(a) The idea's model does not survive the legal envelope** (Task 1). Route per `SKILL.md`, "The kill model": to a **licensed partner or a different legal structure for the same model** when one exists, otherwise **kill**. Defensibility is still provisional at this point, so a partner route is **conditional on the commercial case holding up**; say so. A partner or structure route **continues to 10** with it built in: price its cut, fees or costs into the unit economics here, and restate the one-time and ongoing compliance costs of the new structure or partner for 11 and 12.
- **(b) The model has no viable economics:** the Monetization 0–2 commercial veto (negative unit margins at any plausible scale). Route: **clean kill** of this idea, never a partner (a partner cannot rescue broken economics) and never a model pivot.

**The gate does not fire** when the model fits the envelope (with or without adjustment) and unit margins are plausibly positive, even if thin or uncertain; 12 will surface any problem. A non-firing gate is the expected outcome and **not a health signal** ("Gates are rare by design"). A weak but viable model shows up in the Monetization score, not the gate.

A veto applies the challenge pass to itself and is confirmed per the conviction-gated rule; a kill resting on a Low-conviction decision-critical claim escalates; a partner or structure route continues, with that claim carried to 13's validation layer. A kill ends **this idea**: 13 records it, and the run continues with the next selected idea, if any.

### Task 7: Run the locked-average check

09 locks the third of the four commercial dimensions. After scoring Monetization, compute this idea's commercial average using Problem severity (06), Market size (06) and Monetization (09), with Defensibility at its **ceiling**:
- **6** if no structural-moat candidate appears in the Moat candidates lines of 07, 08 or this section;
- **10** if one has.

If even that average is **below 5.5**, the commercial verdict is decided: it cannot reach the borderline band. (A ceiling average of 5.5–5.99 is not an exit, because a band case at M/L conviction needs 10–12.) Recommend the **early exit to 13**; 10, 11 and 12 are recorded as skipped. In autonomous mode, apply it and document the arithmetic. In checkpoint mode, propose it and let the founder choose.

## Scoring activated in this section

### Monetization clarity dimension

Score Monetization clarity on the 0–10 scale in `rubric.md`, with an H/M/L conviction label. Apply the anchors from `rubric.md`, the **canonical source** (synced copy; the worked examples live there):
- **High (8–10):** at least one revenue model is obvious and proven in adjacent products. Target users (or intermediaries) demonstrably pay for similar things today.
- **Medium (5–7):** a plausible revenue model exists but isn't proven in this specific market or for this specific user. Requires testing.
- **Low (0–4):** no clear path to revenue, or the path requires behaviours users don't currently exhibit.

The score reflects:
- the strength of the idea's model (proven in adjacent products / plausible but unproven / hypothetical);
- the quality of the unit-economics evidence;
- its fit with the legal envelope (clean / needs adjustment / struggles even with adjustment).

Conviction reflects the evidence: proven comparables in this market → H; reasoning from analogous markets → M; hypothesis without grounding → L.

A **0–2** is the **Monetization commercial veto**, cause (b) of the gate. Apply the anchor honestly; the 2/3 line is a cliff, so score the evidence, not the consequence.

## Section-specific content for the four required parts

The four required parts are mandatory per `SKILL.md`.

### Analysis

Labelled subsections, in order: Legal-envelope check; Model fit; Pricing structure; Unit economics; Local lens; Business-model gate evaluation. Then the Monetization score with its conviction label, a **Moat candidates** line (data, network or business-model moats, if any), a **Pinned figures** line, the locked-average arithmetic, and the claims-to-verify list.

### Recommendation

One of five:
- **"Proceed to 10."**
- **"Business-model gate (a), routed to [a licensed partner / a different legal structure for the same model]: proceed to 10"**, conditional on the commercial case.
- **"Early exit to 13 (locked average)"**, with the arithmetic.
- **"Kill — Business-model gate (a)."**
- **"Kill — Business-model gate (b), Monetization veto."**

Findings the founder should weigh that do not fire the gate are **recorded, not surfaced mid-run**: thin margins, a model that diverges from incumbents, local payment constraints. Name them in the Rationale; 11, 12 and 13 use them.

### Rationale

**For a proceed**, cover:
- the model in one sentence;
- the unit economics (revenue per unit, direct cost per unit, margin direction);
- its fit with the legal envelope and the market;
- the Monetization score with its conviction label;
- the locked-average result.

**For a kill**, cover:
- which cause fired, and the specific finding;
- the route;
- the challenge pass applied to the kill;
- a note that it is confirmed per the conviction-gated rule.

### Challenge pass

The judging form from `SKILL.md` (06–13 omit the "non-obvious option" question), plus the section-specific questions below. For a kill, the pass asks what would make the kill wrong. Each finding uses the fixed short format: what changed and why, or "no change".

## Challenge pass: section-specific questions

- **Incumbent-divergence check:** if the model differs from how incumbents make money, is that justified, or a sign it was tried and abandoned?
- **Unit-economics realism:** are all real per-unit costs included (AI and LLM costs, payment fees, usage-linked compliance costs)? A positive margin that leaves one out is not a positive margin.
- **Willingness-to-pay check:** is there evidence people pay for this kind of value (comparable products, observed spending), or only an assumption that they would?
- **Pricing check** (for a cause (b) kill): could a different price level, tier structure or cost-to-serve **within the same model** make the unit economics work? If so, the kill may not survive. A different payer, product or payment pattern is a different idea: if 04 has no such idea, flag that gap for 13.

## Word cap

**Hard maximum (provisional): 1,000 words, excluding citation markers and the source list.**

## Downstream dependencies

What later sections consume from section 09:
- **10** uses the model's infrastructure needs (payments, two-sided onboarding, billing) when scoping the build.
- **11** uses the model and unit economics to judge which acquisition strategies the economics can support, and their payback.
- **12** builds the multi-year projections on the unit economics and pricing, and compares the revenue kept against 05's threshold.
- **13** uses the Monetization score (with conviction) in the commercial score, the gate evaluation, the locked-average result and any data or network moats surfaced here for the final Defensibility score.
