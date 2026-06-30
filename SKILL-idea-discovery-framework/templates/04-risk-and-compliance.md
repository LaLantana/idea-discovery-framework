# Template: 04 — Risk and compliance

## Purpose of this section in the framework

This section evaluates the **structural** picture for the idea in the target market: its regulatory and compliance envelope (its original and still-central scope), plus two checks moved or added here — **data access** (can anyone obtain the data / APIs / partnerships the idea needs) and **capability feasibility** (can current technology do this well at all). It is where the **Structural gate** from `SKILL.md` can fire, on any of three structural dealbreakers — legal/regulatory, data, or capability. A kill recommendation here stops the framework before sections 05–09 run, which changes how this section is structured compared to sections 01–03. The section keeps its name, *Risk and compliance* — the regulatory work is unchanged and load-bearing; the data and capability checks sit on top of it.

This section produces:
- An inventory of the regulatory categories that apply to the idea
- A mapping of specific regulations and their requirements
- Order-of-magnitude estimates of compliance cost and timeline
- Identification of partnership or operational requirements driven by compliance
- A **data-access** assessment (is the data / API / partnership the idea needs structurally available to anyone) — the veto input moved here from section 02
- A **capability-feasibility** assessment (can current technology do this well), drawing on section 03's wrapper test
- A synthesized structural picture characterizing the legal, data, and capability envelope the idea would operate within
- An evaluation against the **Structural gate**'s three conditions (legal / data / capability)
- A recommendation to proceed to section 05, surface concerns, or kill the idea per the Structural gate

**On legal interpretation:** Claude is not a lawyer, and this section's output is not legal advice. The analysis is best-effort synthesis of publicly available regulatory information, oriented around whether the framework can sensibly proceed to section 05. Where regulatory interpretation has material consequences (licensing requirements, structural compliance choices, enforcement risk), Claude flags the need for professional legal review. The user should treat the section's findings as inputs to a legal conversation, not a substitute for one.

Section 04 does not score any commercial dimensions. Its outputs are structural (does the framework continue?) and feed sections 05 (business model design within the legal envelope) and 07 (operational and compliance costs feeding initial investment).

## Brief fields relevant to this section

Before starting the analytical work, draw on these fields from `00-brief.md`:

- **Primary market:** the most load-bearing field for this section. Jurisdiction determines which regulations apply. A regulatory analysis run against the wrong jurisdiction is structurally wrong, not just imperfect.
- **Recommended form factor (from section 03):** different form factors face different regulatory pictures. An agent product handling financial advice faces different rules than a web app providing the same information non-interactively. A B2B SaaS product faces different rules than a consumer-facing app.
- **Idea one-liner:** establishes what regulated activities are involved. The one-liner is the basis for identifying applicable regulatory categories in Task 1.
- **Depth overrides (if any):** acknowledge at the top of the section output. Common overrides: "go deep on financial regulations," "skip detailed analysis on standard SaaS compliance — I know it," "focus on data protection — the rest is standard."

If any of these fields are missing or unclear, surface the gap to the user before starting analytical work. Section 04 especially depends on the primary market being unambiguous — running the analysis against an unclear jurisdiction would produce findings the user cannot rely on.

## Research activated in this section

Web search is mandatory and heavy. Regulations are jurisdiction-specific, change frequently, and Claude's training data is unreliable here. The local lens is structural to this section, not an add-on.

### Web search (mandatory)

Web search must produce, at minimum:
- Applicable regulations in the target market across the categories identified in Task 1 (data protection, financial services, consumer protection, sector-specific licensing, employment, tax, IP, accessibility).
- The regulatory bodies responsible for each applicable category, and their enforcement patterns where information is available.
- Recent enforcement actions in the relevant space (last 12–24 months) — these often reveal what regulators actually enforce vs. what's nominally on the books.
- Any pending legislation or regulatory changes that could affect the idea in the action window (typically 12–18 months out).

Cite sources directly. For regulatory text, cite the regulation by name and number where possible (e.g., "Colombia's Ley 1581 de 2012 on personal data protection," not just "Colombia's data protection law").

### Deep research (user-confirmed)

Deep research is warranted when:
- The regulatory environment is complex — financial services, healthcare, regulated marketplaces, anything touching identity verification or money movement.
- The idea operates across multiple jurisdictions with different regulatory regimes.
- The regulatory environment is rapidly changing — recent legislation, pending enforcement shifts, active rulemaking.
- The user has flagged regulatory analysis as a depth priority in the brief.

When any of these triggers fire, follow the deep-research escalation protocol in `SKILL.md` (surface the case, wait for explicit confirmation, fall back to regular web search if declined).

### Source quality

Prioritize official sources: regulatory body websites, government publications, primary legislation, court decisions where relevant. These are the authoritative sources.

Treat with strong skepticism: blog posts (especially "regulatory overview" content from companies selling compliance services), legal-marketing content, AI-generated regulatory summaries, news articles that summarize regulations without citing them directly. These often oversimplify, conflate requirements across jurisdictions, or misrepresent enforcement patterns.

Conviction labeling follows the standard categorization from template 01: official regulatory sources and primary legislation → H, reputable industry analysis and law firm publications citing primary sources → M, blog posts and uncited summaries → L. Cite sources directly.

### Local lens for research

Structurally mandatory in this section. Regulations are jurisdiction-specific by definition — a US-centric analysis of a Colombian idea is structurally wrong, not just imperfect. The same is true for any market.

The failure mode: defaulting to whichever regulatory framework is most familiar from training data (often GDPR for data protection, US frameworks for financial services or consumer protection) rather than the actual regulations of the target market. This produces analysis that sounds authoritative but is wrong.

To avoid this:
- Search using local regulatory body names and local terminology, not just English-language equivalents.
- Verify that cited regulations actually apply in the target jurisdiction, not just in the more familiar one.
- When a regulation cited has a more famous equivalent in another jurisdiction (GDPR vs. local data protection law, FDA vs. local health regulator), confirm the local regulation directly rather than reasoning from the more famous one.
- If a search returns mostly US/EU-centric results when the target market is elsewhere, refine the query before reasoning from those results.

## Analytical work for this section

These tasks together produce the **Analysis** portion of the section file. The Recommendation, Rationale, and Challenge pass are produced after the analytical work, drawing on it.

The Structural gate evaluation in Task 9 is the outcome of synthesizing the findings from earlier tasks — it is not a separate analytical exercise.

### Task 1: Identify the regulatory categories that apply

Derive applicable regulatory categories from the idea's actual activities, not from a predefined checklist. The question is: *what activities does this idea involve, and what kinds of regulation typically apply to those activities in the target market?*

To prompt thinking, common categories include (illustrative, not exhaustive):

- **Activities involving personal data:** data protection and privacy regulations.
- **Activities involving money:** financial services regulation, payment processing requirements, money transmission rules.
- **Activities selling to consumers:** consumer protection, advertising standards, subscription billing rules, refund obligations.
- **Activities in specific sectors:** sector-specific licensing (healthcare, education, transportation, food, real estate, legal services, financial advice).
- **Activities involving workers or marketplace participants:** employment law, gig economy rules, marketplace liability.
- **Activities generating revenue:** tax registration and obligations.
- **Activities using or hosting third-party content:** IP, copyright, content moderation, hosting liability.
- **Digital activities specifically:** accessibility requirements, age verification (if minors are users), AI-specific regulation in jurisdictions that have it.

This list is starting prompts, not exhaustive. For each idea, ask: *what is this product doing that a regulator might care about?* Different idea types trigger different categories — a consumer hardware product faces product safety and customs categories not listed above; a marketplace faces antitrust and listing liability categories; a cross-border product faces export controls.

Output: a list of which categories apply to this specific idea, with one-sentence reasoning for each. Flag any category that's non-obvious or that the user may not have anticipated.

### Task 2: Map each applicable regulation to the idea

For each applicable category from Task 1, identify the specific regulations and what they require.

For each applicable regulation, document:
- **Regulation name and identifier:** full official name, date, and number where applicable.
- **Regulatory body:** which agency enforces it.
- **What it requires:** the specific obligations the idea would need to meet (registration, licensing, operational practices, disclosure, audit, reporting, etc.).
- **Trigger conditions:** when the regulation applies — every business in the category, businesses above a size threshold, businesses with specific characteristics. Some regulations have meaningful exemptions or thresholds.

This is the substantive regulatory work.

**On interpretive uncertainty:** Where regulatory interpretation is uncertain — the regulation's application to this specific idea is ambiguous, enforcement patterns are unclear, or the regulation requires interpretation that depends on context Claude doesn't have — flag this explicitly in the Task 2 output. Document the regulation, document the uncertainty, label conviction L, and note that professional legal review is warranted to resolve the interpretation. Do not paper over interpretive ambiguity by picking one reading and presenting it confidently. The user needs to see the ambiguity to know where legal review is worth the cost.

### Task 3: Estimate compliance cost and timeline

For each requirement identified in Task 2, estimate compliance cost in three categories:

- **One-time costs:** initial licensing fees, legal setup, entity formation, initial compliance audits, technical implementation of compliance requirements (e.g., consent management infrastructure for data protection).
- **Ongoing costs:** annual licensing renewals, regular audits, reporting obligations, dedicated compliance personnel or services.
- **Operational complexity:** the degree to which compliance shapes day-to-day operations (e.g., consent flows in product design, data localization affecting infrastructure choices, retention rules affecting feature design).

Use order-of-magnitude estimates with conviction labels — precise numbers aren't needed for this gate, but the rough scale matters. "Initial setup: low five figures, ongoing: low four figures annually, M conviction based on publicly cited compliance services pricing" is the level of precision needed.

Be explicit about what's expensive vs. what's procedural. Some compliance requirements are administratively heavy but financially light; others are the reverse. Both shape what section 05 can design.

### Task 4: Identify partnership or operational requirements

Some regulations require specific partnerships or operational structures. Identify these and what they imply.

Common examples:
- Money movement often requires a banking partner or a money transmitter license — both have significant implications for what the user can build solo.
- Data localization requirements may require infrastructure in specific jurisdictions.
- Sector-specific operations may require licensed personnel (e.g., financial advisor, medical professional) on staff or contracted.
- Marketplace operations may require KYC/identity verification partners.
- Entity formation may need to be in specific jurisdictions to be eligible for certain regulatory regimes.

For each requirement, note: what partnership or structure is needed, what it implies for cost and time, and whether the user can realistically obtain it. The realistic-obtainability question is critical — a "required" partnership the user cannot get is functionally a legal block.

### Task 5: Assess data access (structural veto input)

Data access moved here from section 02 — it is no longer a commercial score, it is a **structural veto**. The question is **market-structure availability**: do the data sources, APIs, integrations, or partnerships the idea needs exist, and is access structurally available *to anyone* building this? (The separate question of whether *this specific user* can obtain access — given their resources and relationships — stays in section 06.)

Assess and conviction-label:
- **What data / access the idea requires** to work at all (real-time inventory, transaction data, a gated API, a partner feed, scrapable sources).
- **Whether that access is structurally available:** public / licensable APIs or partnership programs exist; scrapable sources with no prohibitive legal barrier; or — at the other end — the data is locked inside gatekeepers with no path for a new entrant, or its use is legally prohibited.
- Pull in any data-availability facts section 02's research surfaced (a closed ecosystem, an established partnership program, a known gatekeeper).

**Veto input:** what feeds the Structural gate (Task 9) is whether data access is *blocked* — the precise firing bar (obtainable by **no one** building this, not merely hard for this user) is defined in `SKILL.md`'s kill model. A *low-conviction* block routes through the validation layer before the kill stands — verify before killing on a guess.

### Task 6: Assess capability feasibility (structural veto input)

This check asks whether **current technology can do this well at all** — an opportunity-level question (can *anyone* build this so it works), distinct from section 06's user-level question (can *this user* build it). It consumes section 03's **wrapper test** (Task 3): the wrapper test characterizes what general-purpose technology already does in this space; this task judges whether the idea's core function is *technically achievable to an adequate standard* with today's capabilities.

Assess and conviction-label:
- **The core capability the idea depends on** (e.g., reliable extraction from messy documents, real-time multi-step orchestration, domain reasoning at a quality users would trust).
- **Whether current technology meets that bar:** clearly yes (proven in comparable products); plausibly, with engineering effort; or no — the required quality / reliability is beyond what current technology delivers.
- **Trajectory:** if it is not there yet but improving fast, note that — it routes to *park*, not *kill* (see Task 9).

**Veto input:** what feeds the Structural gate (Task 9) is whether capability is *infeasible* — the precise firing bar (the core function cannot be performed to an adequate standard by **anyone** with current technology) is defined in `SKILL.md`'s kill model. A low-conviction infeasibility routes through the validation layer before the kill stands.

### Task 7: Local lens application

Confirm the analysis applies to the actual target market, not a US/EU default. Surface any cases where the regulatory picture differs significantly from what a US/EU-centric search would suggest.

Specifically check:
- Did the analysis cite regulations from the actual target jurisdiction? Re-verify each citation if in doubt.
- Did the analysis assume frameworks (GDPR-style data protection, US-style consumer protection, specific licensing regimes) that may not exist or take different form in the target market?
- Are there target-market-specific regulations that wouldn't appear in a generic search (e.g., national-language content requirements, local data localization, sector regulations specific to the country)?
- What's the enforcement reality in the target market? Some jurisdictions have regulations on the books that are rarely enforced; others enforce strictly even on minor violations.

Flag any cases where the local lens revealed a meaningful correction from what an English-language or US/EU-default analysis would have produced.

### Task 8: Synthesize the structural picture

Pull together the findings from Tasks 1–7 into a coherent **structural picture** for the idea — regulatory, data, and capability together. The synthesis should characterize:
- Which regulatory categories apply and which are most significant for this idea.
- The total compliance cost picture (one-time and ongoing) at order-of-magnitude.
- The structural requirements (partnerships, entity formation, licensed personnel) that compliance imposes.
- **The data-access position** (Task 5): available, conditionally available, or blocked — and to whom.
- **The capability-feasibility position** (Task 6): feasible, feasible-with-effort, not-yet, or infeasible.
- The realistic timeline to operational compliance — how long from "decide to build" to "legally allowed to operate."
- Any material structural uncertainty — pending regulatory changes, interpretive ambiguity, enforcement unpredictability, contested data access, or capability that's improving but not yet there.

The output is a paragraph or two characterizing the structural envelope (legal + data + capability) the idea would operate within. This is the input that Task 9 evaluates against the Structural gate, and the legal envelope that section 05 will design business models within.

### Task 9: Evaluate against the Structural gate

Apply the **Structural gate** to the structural picture from Task 8. Its three firing conditions — **legal / regulatory blocked**, **data access blocked** (from Task 5), and **capability infeasible** (from Task 6), each with its precise test (the "obtainable by no one" bar, the disproportionate-cost carve-out) — are defined in `SKILL.md`'s kill model. Evaluate the structural picture (Tasks 1–8) against them. Each is a *conclusion from the research above*, never a substitute for it; a low-conviction finding routes through the validation layer (verify before the kill stands).

**Gate evaluation outcome — and routing (per `rubric.md`'s structural-veto routing):**
- If any condition is met, the gate fires. **Structural vetoes route uniformly:** **partner** if a partner can supply the missing piece (licensed partner for legal, data partner for data, specialized-capability partner for capability) *and* the commercial case is strong; **kill** if the thing is unavailable to anyone; **park** (capability only) if the technology isn't there yet but is improving.
- **Important caveat — the routing here uses a *partial* commercial picture:** Monetization (05) isn't scored yet and Defensibility (03) is still provisional. So a *partner* route surfaced here is **conditional on the commercial case holding up** — state that explicitly when surfacing it.
- The kill (when that's the route) carries the **challenge pass applied to the kill itself** and is confirmed per the conviction-gated rule.
- If no condition is met, the gate does not fire. Recommend proceed (or surface, per the Recommendation subsection).

## Scoring activated in this section

Section 04 does not score any commercial dimensions directly (data access, once a commercial dimension, is now one of its structural vetoes — assessed, not scored). Its outputs feed the legal, data, and capability findings into the **Structural gate**, and inform sections 05 (business model viable within the legal envelope) and 07 (operational cost). No conviction-labeled commercial scores are produced here, but conviction labels apply to the structural findings themselves per the standing habit in `SKILL.md`.

If a finding has Low conviction and is decision-relevant (i.e., it materially affects whether the Structural gate fires), surface this explicitly — this is the validation layer: a structural veto resting on low-conviction evidence must be validated or explicitly accepted before the kill stands. A kill based on Low-conviction regulatory interpretation (or a contested data / capability finding) is exactly the case where the challenge pass and the conviction-gated escalation matter most.

## Section-specific content for the four required parts

The four required parts (Analysis, Recommendation, Rationale, Challenge pass) are mandatory in the section file per `SKILL.md`. Below is what each part contains for section 04 specifically.

### Analysis

Subsections in order: Applicable regulatory categories, Specific regulations and requirements, Compliance cost and timeline estimates, Partnership/operational requirements, Data access, Capability feasibility, Local lens, Synthesized structural picture, Structural gate evaluation.

The Synthesized structural picture is the consolidated view of the analytical work. The Structural gate evaluation is the structured judgment against the gate's three conditions (legal / data / capability).

The Analysis subsections should read as a connected investigation, not disconnected blocks. The synthesis explicitly draws on findings from Tasks 1–7; the Structural gate evaluation explicitly draws on the synthesis.

### Recommendation

Three possible recommendations from this section:

- **Proceed to section 05** — the standard case. Both of the following must hold:
  - The Structural gate does not fire (no legal block, no obvious disproportion, no data block, no capability-infeasibility).
  - The structural picture doesn't contain surprises that materially change the idea — no unexpected licensing requirements, no jurisdictional issues the user didn't anticipate, no enforcement risks, no newly-surfaced data or capability concerns the user should weigh.

- **Surface to user before proceeding** — when the Structural gate does not fire but the analysis surfaced findings the user should see before continuing. Specifically:
  - Compliance requires partnerships or operational structures the user may not have anticipated (banking partner, entity formation in a specific jurisdiction, licensed personnel).
  - Compliance cost is material relative to the user's "make money" threshold but not obviously disproportionate. The cost matters for business model design but doesn't kill the idea outright.
  - Data access is conditional (achievable but requires negotiation, a partnership, or gray-area scraping) rather than clearly blocked — the cost and route matter downstream.
  - Capability is feasible-with-effort or improving-but-not-yet, rather than clearly infeasible — worth the user's judgment on timing.
  - Regulatory uncertainty exists — pending legislation, recent enforcement changes, or interpretive ambiguity that affects what compliance looks like.
  - Regulations apply that materially contradict the user's framing in the brief — e.g., the brief framed this as a SaaS product but the analysis surfaced consumer-protection or financial-services applicability the user didn't anticipate. The discrepancy itself is what should be surfaced.

- **Recommend kill (Structural gate)** — only when one of the three structural conditions explicitly applies, per Task 9. **Route uniformly per `rubric.md`:** partner (if a partner can supply the missing piece and commercial is strong — stated as conditional on the partial commercial picture), kill (if unavailable to anyone), or park (capability only, if the tech is improving). The challenge pass applies to the kill itself.

In all cases except kill, do not stop the framework — surface the concern, get the user's input, then proceed. For kill, follow the kill protocol in `SKILL.md`: surface the recommendation with rationale and challenge pass, then confirm per the **conviction-gated rule** (autonomous auto-confirms at High/Medium conviction and escalates only if the kill rests on low-conviction evidence; checkpoint pauses) before writing to `09-decision.md`.

### Rationale

For a proceed recommendation, the rationale must include:
- What regulations apply, in one or two sentences.
- The rough compliance cost picture (order of magnitude).
- Any structural requirements (partnerships, entity formation) the user will need.

For a surface recommendation, the rationale includes the above plus the specific concern being surfaced and what the user is being asked to weigh.

For a kill recommendation, the rationale includes:
- Which Structural gate condition applies (legal block / obvious disproportion / data blocked / capability infeasible).
- The specific finding that triggers the condition (regulation name and requirement; or the data source / capability and why it is blocked or infeasible to anyone).
- The route taken (partner / kill / park) and, for a partner route, the explicit note that it is conditional on the still-partial commercial picture.
- The challenge pass output applied to the kill itself (see below).
- A note that this kill is confirmed per the conviction-gated rule in `SKILL.md`.

### Challenge pass

The standard four falsification questions from `SKILL.md` apply, plus the section-specific questions below.

For kill recommendations, the challenge pass is applied to the kill itself per `SKILL.md`'s kill model — the questions ask what would make the kill recommendation wrong, not just what would make the analytical findings wrong.

## Challenge pass: section-specific falsification questions

In addition to the standard four questions from `SKILL.md`, apply these to the risk and compliance analysis:

- **Jurisdiction-correctness check:** did the analysis apply the right jurisdiction's regulations, or did it default to US/EU? Re-verify each cited regulation if in doubt.
- **Regulatory-interpretation check:** are the regulations being read correctly, or has the analysis confused enforcement intent (what regulators care about) with regulatory text (what the law actually says)? These can diverge, especially in markets where enforcement is selective.
- **Workaround check (for kill recommendations specifically):** *(Role: surface new legal/structural alternatives not raised during the analysis, to pressure-test the kill. Templates 04 and 05 introduce fresh alternatives this way; template 07 instead runs a thoroughness check on its Step 2 — the form is tuned to each section's structure.)* Are there legal structural workarounds that change the regulatory picture? Consider: different entity type (consumer LLC vs. licensed financial entity), different operational structure (referral arrangement vs. direct provision), partnership rather than direct provision (using a licensed partner's infrastructure), different market entry (B2B2C vs. direct-to-consumer, where the intermediate party holds the regulated function). If a workaround exists, the kill recommendation may not survive — revise.
- **Enforcement-realism check:** is the regulation actually enforced in this market, or is it on the books but rarely applied? This affects compliance cost realism. A regulation enforced strictly with substantial fines is a different compliance picture than a regulation rarely cited even when violated. Note: this check is for cost-realism calibration only — Claude should not advise the user to ignore regulations because they're rarely enforced. The user makes that call.

Document the findings under the Challenge pass heading even if no changes were made to the analysis. If changes were made, note what changed and why.

## Depth calibration for this section

Depth varies significantly by idea. A SaaS product in a low-regulation B2B space needs much less depth here than a fintech or healthcare idea. The depth heuristic: enough to be confident about whether the Structural gate fires, and enough to give section 05 a clear legal envelope to design business models within.

Normal depth ranges for this section:
- **Low-regulation idea** (B2B SaaS, content tools, productivity software in unregulated categories): ~400–600 words. Tasks 1–7 still run, but most categories from Task 1 may not apply, and the cost estimates are typically straightforward.
- **Moderately regulated idea** (consumer products, marketplaces, data-heavy products): ~600–900 words. Multiple categories apply with non-trivial requirements.
- **Heavily regulated idea** (fintech, healthcare, regulated marketplaces, identity-touching products): ~900–1500 words. Multiple categories apply with substantial requirements; partnership requirements likely; the Structural gate evaluation is non-trivial.

`SKILL.md`'s general ~600–800 word check-in threshold still applies as a self-check signal. For the moderate and heavy tiers, exceeding 600–800 words is expected — but the check-in remains useful: confirm at that point that the additional depth is contributing to the Structural gate decision or section 05's envelope, not optimizing past the decision threshold.

Signs the section is too thin:
- Regulatory categories listed without specific regulations named.
- Compliance cost estimated as "varies" or "depends" with no order-of-magnitude.
- Structural gate evaluation reduced to a sentence rather than structured application of its three conditions (legal / data / capability).
- Local lens absent or generic.

Signs the section is too thick:
- Multiple paragraphs on regulations that don't materially affect the gate or section 05's business model design.
- Detailed legal interpretation that exceeds Claude's competence and should be deferred to professional legal review.
- Speculation about future regulatory change beyond the action window.
- Enforcement history not relevant to the cost realism question.

If the brief specifies a depth override for this section, honor it and acknowledge it at the top of the output.

## Downstream dependencies

What later sections will consume from section 04:

- **Section 05 (Business model):** will consume the **Synthesized structural picture** subsection (its legal-envelope component) as the envelope to design business models within. Some revenue models may be prohibited or require specific licensing; section 05 designs within these constraints.
- **Section 06 (Solo-buildability):** will consume the **Partnership/operational requirements** subsection when evaluating whether the user can ship solo. A required banking partner or licensed personnel directly affects solo-buildability.
- **Section 07 (Investment & GTM):** will consume the **Compliance cost and timeline estimates** subsection when estimating initial investment and operational costs.
- **Section 08 (Financial projections):** will consume the ongoing compliance cost estimates from the same subsection as a line item in cost projections.
- **Section 09 (Decision):** will consume the **Synthesized structural picture** and **Structural gate evaluation** subsections for the final risk picture, including any regulatory, data-access, or capability uncertainty flagged as needing professional review; the data and capability findings also feed section 09's finalization of the provisional Defensibility score (regulatory and data moats can raise it).