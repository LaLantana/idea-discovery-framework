# Template: 02 — Market & competitive landscape

## Purpose of this section in the framework

This is the framework's primary external-research section. It establishes who is already operating in the target market, what gaps exist in the current competitive landscape, and whether the target market is large enough to support the idea at the user's make-money threshold.

This section produces:
- A characterization of direct incumbents, substitutes, and white space in the target market
- A bottom-up SOM estimate for the target market
- The dimensions of competitive choice that template 03 will use to generate the differentiation hypothesis
- A score on the Market size dimension of the commercial score (data-access availability is no longer scored here — it moved to section 04 as a structural check)
- A recommendation to proceed to section 03 — or, if Market size is fatally low (0–2), an early-exit kill recommendation; or, in edge cases, a surface-to-user concern

Section 02 **can** produce a kill. Market size is a commercial veto dimension: a score of **0–2** (no market clears the make-money threshold) is a fatal flaw, so it fires here as an **early-exit** — recommend the kill and stop, rather than running sections 03–09 on a market that can't pay. A score of **3 or above** is survivable; it feeds the commercial average at section 09, and the section recommends proceeding to 03.

Data access is **no longer scored in this section.** The market-structure question — can anyone access the data, APIs, or partnerships the idea needs — moved to section 04 as a **structural veto**; the user-level question (can *this* user obtain access) remains in section 06. (See `rubric.md`, "The kill model.")

## Brief fields relevant to this section

Before starting the analytical work, draw on these fields from `00-brief.md`:

- **Primary market:** anchors what market the analysis is about. In Mode C (open search, see below), this field reads "open" and the analytical work selects the primary market with user confirmation.
- **Market expansion question:** determines which of three analytical modes this section runs in. This is the most load-bearing brief field for section 02.
- **Why this market:** provides the user's reasoning for the primary market, useful context for evaluating whether incumbents and substitutes match the user's framing.
- **Make-money threshold:** required for the Market size dimension score. The SOM estimate is evaluated against this threshold.
- **Relevant prior knowledge:** if the user has already researched the market, this field surfaces what's known and reduces redundant research.
- **Depth overrides (if any):** acknowledge at the top of the section output. Common overrides for this section: "skip detailed competitive analysis on the [market] — I know it well," "go deeper on the regulatory environment," "expand the incumbent list — the market is more fragmented than typical."

If any of these fields are missing or unclear, surface the gap to the user before starting analytical work.

## Research activated in this section

This is the framework's heaviest research section. Web search is mandatory. Deep research is warranted in many cases and is user-confirmed when triggered.

### Web search (mandatory)

Web search must produce, at minimum:
- A named list of 3–5 direct incumbents in the primary target market, with current product offerings and (where available) recent funding, M&A, or strategic activity.
- A list of indirect competitors and substitutes — adjacent products and the manual workarounds users currently rely on.
- The regulatory environment relevant to the competitive landscape (not the full risk and compliance picture — that's section 04 — but anything that materially shapes who can compete and how).
- Market structure: is the market fragmented or consolidated? Are there clear category leaders? Has there been recent consolidation?

If the brief specified Mode B (primary plus expansion candidates) or Mode C (open search), web search also covers the candidate markets at lower depth.

Cite sources directly in the analysis.

### Deep research (user-confirmed)

Deep research is warranted in this section when:
- The target market is unfamiliar enough that even orienting requires significant work.
- The competitive landscape is highly fragmented with many small players, each requiring some characterization.
- The regulatory environment shaping competition is complex (e.g., licensed industries, jurisdictionally fragmented).
- Mode C (open search) is active and the candidate-market evaluation requires structured comparison across multiple geographies.

When any of these triggers fire, follow the deep-research escalation protocol in `SKILL.md` (surface the case, wait for explicit confirmation, fall back to regular web search if declined).

### Source quality

Bias toward primary sources: company filings, official market reports, regulatory bodies, peer-reviewed research, and reputable industry publications. Treat blog posts, aggregator sites, and AI-generated content lists with skepticism — they often replicate each other's errors and are particularly unreliable for local market information.

Conviction labeling follows the same categorization as the Identify evidence task in template 01: primary sources → H, secondary sources → M, tertiary or hypothesis-level sources → L. Cite sources directly.

### Local lens for research

The geographic lens is especially critical in this section. Incumbents in the target market are not the same as incumbents elsewhere. Apply the lens to *what to search for*, not just *how to interpret what's found*.

Common defaults that mislead in this section:
- **Assuming US-equivalent incumbents.** Fandango is not the incumbent in Colombia; Cine Colombia's app and Tu Boleta are. Search for the actual local players, not the global ones.
- **Assuming the same monetization patterns.** Convenience fees and commission rates vary significantly across markets. Don't assume Fandango's $1.50–3 per ticket transfers to other geographies.
- **Assuming the same regulatory baseline.** Data protection, financial services licensing, and consumer protection laws vary by jurisdiction and shape who can compete.
- **Assuming the same distribution channels.** App stores, payment processors, and discovery surfaces differ significantly by market.

When searching, include the target market explicitly in queries ("movie ticket booking apps Colombia," not just "movie ticket booking apps"). If a search returns mostly US-centric results, refine the query before reasoning from those results.

## Analytical work for this section

These tasks together produce the **Analysis** portion of the section file. The Recommendation, Rationale, and Challenge pass are produced after the analytical work, drawing on it.

The analytical work runs in one of three modes based on the brief's market expansion question.

### Mode selection

Read the brief's market expansion question. Run one of the three modes below:

- **Mode A: "This market only"** — Run Tasks 1–5 on the primary market specified in the brief. Score Market size for that market. No user confirmation required; the brief has specified the market.

- **Mode B: "Primary plus suggest 2–3 expansion candidates"** — Run Tasks 1–5 on the primary market in full depth. Then run the Candidate-market evaluation for 2–3 expansion candidates at lighter depth. Score Market size for the primary market only; expansion-market findings are qualitative for sequencing. No user confirmation required by default — the brief has specified the primary market. *Edge case:* if the expansion analysis surfaces a candidate market that may be a stronger primary than the originally specified one, surface this finding to the user (see Recommendation section).

- **Mode C: "Open search"** — The brief reads "open" for primary market, delegating the primary-market selection to the discovery process. Run the Candidate-market evaluation first across 3–5 plausible markets. **Stop and surface the primary-market recommendation to the user for confirmation before any further work.** Once the user confirms the primary market, run Tasks 1–5 on the confirmed primary. Score Market size for the confirmed primary.

Acknowledge the active mode at the top of the section output ("Running in Mode B: primary market is Colombia, expansion candidates will be evaluated for the LatAm region").

In Mode C, the section produces output in two phases: (1) candidate-market evaluation and primary-market recommendation, surfaced to user; (2) after user confirmation, the full Tasks 1–5 analysis on the confirmed primary. Do not proceed to phase 2 without explicit user confirmation of the primary market selection.

### Task 1: Identify direct incumbents

Name 3–5 direct incumbents in the target market — players already addressing this painpoint or one closely adjacent. Expand the list if the market is highly fragmented with no clear leaders.

For each incumbent, characterize:
- **What they offer:** the product or service in one sentence.
- **Who they serve:** the user segment they target.
- **What they do well:** strengths from the user's perspective.
- **What they do poorly:** weaknesses, gaps, or sources of user frustration.
- **Strategic position:** category leader, fast follower, niche player, declining incumbent, recent entrant.

Avoid listing more than 5 incumbents unless the market genuinely warrants it (fragmented, no clear leaders, or the user specifically asked for deeper coverage in the brief). Beyond 5, additional incumbents rarely change the kill/proceed analysis and add noise.

### Task 2: Identify indirect competitors and substitutes

Direct competitors aren't the only competition. Identify:
- **Adjacent products:** tools or services that don't directly address the painpoint but partially substitute (e.g., for a movie discovery app, this might include streaming services that compete for the same evening's entertainment).
- **Manual workarounds:** what users currently do to manage the painpoint without a dedicated tool (asking in WhatsApp groups, manual price comparison, calling theaters directly).
- **Behavioral alternatives:** how users avoid the painpoint by not engaging with the category at all (skipping the activity, defaulting to a non-optimal but familiar choice).

For each substitute, note: how widely used it is, how painful it is, and whether users would actually switch to a better solution. A widely-used but tolerable workaround is structurally different from a widely-used and painful one.

### Task 3: Identify white space

Based on Tasks 1 and 2, identify gaps in the current landscape:
- **What's not being addressed at all:** specific user needs or painpoint variants that no incumbent or substitute handles.
- **What's being addressed poorly:** needs that are technically covered but with significant friction, cost, or user dissatisfaction.
- **What's being addressed expensively:** needs covered only by premium products inaccessible to a broader user segment.

White space is where the differentiation hypothesis (template 03) will be tested. Be specific — "no one does X for Y users at Z price point" is white space; "the market could be better" is not.

If no white space is identifiable, that is itself a finding. Flag it explicitly and consider what it implies for the idea's commercial viability. A saturated market with no white space is not automatically a kill, but it raises the bar significantly for the differentiation hypothesis.

### Task 4: Identify the dimensions of competitive choice

Identify 3–4 dimensions on which users actually choose between options in this category. These are the dimensions that matter for user choice, not a comprehensive feature comparison.

Examples:
- For consumer ticket booking: speed of checkout, price transparency, seat selection clarity, payment method flexibility.
- For B2B finance tools: integration with existing accounting software, data security, audit trail completeness, user onboarding time.

These dimensions are an input to template 03, where the differentiation hypothesis is generated. Template 03 will ask: on which of these dimensions can this idea be sharply differentiated from incumbents?

Avoid:
- A full feature matrix (incumbents × every possible feature) — that's depth without decision value.
- Vague dimensions ("better UX," "good design") — these don't help template 03 generate a specific differentiation hypothesis.
- More than 4 dimensions — beyond that, the dimensions stop describing the actual basis of choice.

### Task 5: Local lens application

Apply the geographic lens specified in the brief to the competitive landscape:
- How does the incumbent landscape in the target market differ from the global reference picture? Are there local players that wouldn't appear in a global search?
- Are there local substitutes or workarounds that wouldn't be obvious from outside the market (e.g., WhatsApp-based informal services, community marketplaces, government-provided alternatives)?
- Are there market-specific factors that change which dimensions of competitive choice actually matter (e.g., payment method flexibility matters more in cash-heavy markets, audit trail completeness matters more in heavily regulated industries)?
- Are there regulatory or infrastructural factors that shape who can compete?

Flag any implicit US/global defaults the analysis has been relying on if the local lens surfaces them.

### Candidate-market evaluation (Modes B and C only)

This task is conditional. Run it if Mode B or Mode C is active; skip it in Mode A.

For each candidate market (2–3 in Mode B, 3–5 in Mode C), evaluate at lighter depth than the primary:
- **Painpoint presence:** is the painpoint real and significant in this market, or does it manifest differently (or not at all)?
- **Market size:** rough order-of-magnitude estimate of the addressable user base.
- **Competitive density:** how crowded is the market? Are there obvious incumbents already covering this space?
- **Build/regulatory accessibility from the user's position:** can the user realistically operate in this market given language, regulations, payment infrastructure, distribution channels, and existing relationships?
- **Cultural fit:** does the proposed solution shape (assuming it stays roughly similar across markets) actually fit how users in this market behave?

Each candidate market gets a short structured assessment (3–5 sentences per market), not a full Tasks 1–5 treatment.

In Mode B, after evaluating the 2–3 expansion candidates, produce a sequencing recommendation: in what order should expansion be considered after the primary? Note this in the section output. If the analysis surfaces a candidate that looks dramatically stronger than the originally specified primary, surface this finding to the user as well (see Recommendation section's edge case).

In Mode C, after evaluating the 3–5 candidate markets, produce a primary-market recommendation: which candidate should be the primary, with reasoning. Surface this to the user and wait for confirmation before continuing to Tasks 1–5.

## Scoring activated in this section

### Market size dimension

Score the Market size dimension on the 0–10 scale defined in `rubric.md`, with H/M/L conviction label.

Apply the Market-size anchors from `rubric.md` — the **canonical source** (this is a synced copy; the worked examples live there). Keep it in sync if the rubric's anchors change:
- High (8–10): SOM in the target market clears the user's "make money" threshold (defined per-idea in the brief) with conservative assumptions. Bottom-up estimate, not analyst-report TAM.
- Medium (5–7): SOM is plausible at base-case assumptions; clears threshold only at optimistic ones.
- Low (0–4): Even optimistic SOM doesn't clear the threshold, or the math depends on assumptions that have no evidence.

The SOM estimate must be bottom-up. The structure:

1. Define the target user segment numerically (e.g., "moviegoers in major Colombian cities aged 18–45 with smartphones").
2. Estimate the population of that segment (e.g., from census data, app penetration reports, or industry sources).
3. Estimate the fraction realistically reachable as users within the first 3 years.
4. Estimate the average revenue per user per year, based on the brief's monetization hypothesis or analogous comparables.
5. Multiply to produce the SOM.
6. Compare the SOM against the brief's make-money threshold. The comparison is honest: if SOM clears the threshold by 50%+ under conservative assumptions, that's a High-band score. If it clears only under optimistic assumptions, that's Medium. If it fails to clear under any reasonable assumptions, that's Low. Do not adjust the SOM steps to engineer a desired score — the no-distortion rule from the rubric applies here.

Cite the sources for each step. Conviction label reflects the quality of those sources: census data and industry reports → H; reasonable estimates from analogous markets → M; assumptions without external grounding → L.

A 0–2 score is a **fatal commercial veto** — it triggers the **early-exit** (recommend the kill and stop; see the Recommendation section). Because the veto turns entirely on the make-money threshold, run the **threshold sanity-check as part of this evaluation, before the veto fires**: confirm the brief's make-money threshold is the right bar (not implausibly high or low), and that the SOM genuinely fails it under *every* reasonable assumption — not just the conservative case. If a defensible adjustment to the threshold or the target segment would clear it, that is a **pivot** candidate (a re-brief), surfaced with the kill rather than applied as a silent override. Apply the anchor honestly and score the evidence, not the consequence; the 2/3 line is a cliff.

### Data access — assessed in section 04, not scored here

Data access is **no longer a scored dimension** in this section (or anywhere in the commercial score). The market-structure question — do the data sources, APIs, integrations, or partnerships the idea needs exist, and is access structurally available to anyone — is now a **structural veto in section 04 (Risk and compliance)**; the user-level question (can *this* user obtain access, given their resources and relationships) stays in section 06 (Solo-buildability).

If this section's research surfaces data-availability facts (a closed ecosystem, an established partnership program, a gatekeeper), **carry them into section 04** as inputs to its data-access check rather than scoring them here.

## Section-specific content for the four required parts

The four required parts (Analysis, Recommendation, Rationale, Challenge pass) are mandatory in the section file per `SKILL.md`. Below is what each part contains for section 02 specifically.

### Analysis

Structure depends on the active mode.

**Mode A:** Five labeled subsections in order: Incumbents, Substitutes, White space, Choice dimensions, Local lens. Then the Market size dimension score with its conviction label and brief reasoning.

**Mode B:** Same five subsections for the primary market, plus a sixth subsection (Expansion candidates) containing the candidate-market evaluation and sequencing recommendation. The Market size score applies to the primary market only.

**Mode C:** Opens with the Candidate-market evaluation and the primary-market recommendation (surfaced to the user for confirmation before the rest of the analysis runs). After user confirmation, the same five subsections for the confirmed primary, then the Market size score.

In all modes, the subsections should read as a connected investigation, not disconnected blocks. White space (Task 3) builds on Incumbents (Task 1) and Substitutes (Task 2). Choice dimensions (Task 4) interpret the landscape characterized in Tasks 1–3. Local lens (Task 5) modifies all of the above.

### Recommendation

For section 02, the recommendation is one of three:

**"Proceed to section 03"** — the standard case, when Market size is **3 or above**. The score feeds the commercial average later.

**"Early-exit kill"** — when Market size is **0–2** (no market clears the make-money threshold). This is the Market-gate commercial veto (defined in `SKILL.md`'s kill model); it fires here, not at section 09. Run the **threshold sanity-check** (Market size scoring section) before the veto fires — confirm the SOM genuinely fails under every reasonable assumption — then follow the **kill protocol in `SKILL.md`** (all four parts, the challenge pass applied to the kill, conviction-gated confirmation, then write `09-decision.md` noting the early-exit and skipped sections), with two section-specific notes: the challenge-pass-on-kill uses the SOM-vs-TAM and white-space-realness checks below (the ones that test a weak-market kill); and per `rubric.md`, a commercial veto routes to a **clean kill** or a **pivot** (a re-brief targeting a different market or segment) — never "needs a partner."

**"Surface to user before proceeding"** — when the issue is an ambiguity to resolve rather than a clean score:

*Findings about the primary market itself:*
- The market is significantly more crowded than the brief assumed, suggesting the user should reconsider whether to continue.
- No white space is identifiable, raising the bar for the differentiation hypothesis significantly.
- Regulatory barriers to entry have emerged that the user did not anticipate.
- The Market size estimate sits right on the early-exit cliff (a 2 that could defensibly be a 3) at low conviction — surface it rather than auto-killing on thin evidence (the validation layer at the boundary).

*Findings about the market choice (Modes B and C only):*
- Mode C is active and the primary market needs user confirmation before the full Tasks 1–5 run.
- Mode B's expansion-candidate analysis surfaces a candidate market that looks dramatically stronger than the originally specified primary.

In the surface-to-user cases, do not stop the framework — surface the concern, get the user's input, then proceed (or early-exit, if the resolved Market size is 0–2).

### Rationale

The rationale connects the analytical work to the recommendation. It must include:
- The competitive picture in one or two sentences (the landscape, the white space, the key choice dimensions).
- The Market size dimension score with its conviction label.
- The reasoning behind the SOM estimate, in summary form (the size of the target segment, the realistic capture fraction, the per-user revenue assumption).
- Any local-lens findings that materially affected the scores.
- For Modes B and C: the expansion or primary-market recommendation, with reasoning.

The rationale is what the user reads to understand why the section landed where it did. It must not just restate the analysis — it must connect analysis to conclusion explicitly.

### Challenge pass

The standard four falsification questions from `SKILL.md` apply, plus the section-specific questions below.

## Challenge pass: section-specific falsification questions

In addition to the standard four questions from `SKILL.md`, apply these to the Market & competitive analysis:

- **Incumbent-coverage check:** are there incumbents the analysis missed because they don't appear in obvious searches — e.g., local players without strong English-language web presence, B2B incumbents hidden from consumer search, recent entrants not yet covered by industry publications? A complete-looking landscape from US-centric search results is a red flag.
- **Substitute-displacement check:** would users actually switch from the substitutes identified, or are the substitutes "good enough" in practice? A painpoint with widely-used workarounds may not produce switching behavior, even if the workarounds are imperfect.
- **SOM-vs-TAM check:** is the SOM estimate actually the *serviceable obtainable market* (the slice this idea can realistically capture in the action window), or has it slipped into TAM territory (the total market size)? TAM × small capture fraction is not a SOM estimate.
- **White-space-realness check:** if no one is filling the identified white space, why? "No one has done it yet" is rarely the complete answer — usually there is a reason. Common reasons that need to be ruled out: it's been tried and failed, the unit economics don't work for incumbents, regulatory barriers prevent it, the user demand isn't actually there. Genuine timing windows do exist (new technology, regulatory shifts, demographic changes can open real opportunities), but treat "this is a timing window" as a claim that needs evidence, not a default explanation.

Document the findings under the Challenge pass heading even if no changes were made to the analysis. If changes were made, note what changed and why.

## Depth calibration for this section

This section's analysis should produce ~700–1,000 words of substantive content (not counting headers, source citations, or framework boilerplate). This is heavier than `SKILL.md`'s general ~600–800 word check-in threshold because section 02 carries significantly more research and structural work than other sections.

Signs the section is too thin:
- Fewer than 3 incumbents named, or named without characterization beyond "they exist."
- No substitutes or workarounds identified.
- White space asserted without specifics ("there's a gap in the market" without naming what's missing for whom).
- SOM estimate without bottom-up math (just a single number with no derivation).
- Local lens absent or reduced to "the market is similar."

Signs the section is too thick:
- More than 5 incumbents named (unless the market is genuinely fragmented).
- Full feature matrix across many dimensions.
- Exhaustive funding history of each incumbent unless relevant to the analysis.
- Speculation about future market evolution that doesn't change the current scoring.
- More than 4 dimensions of competitive choice.

If the brief specifies a depth override for this section, honor it and acknowledge it at the top of the output. The override may legitimately push the section past the typical word count range (e.g., "go deep on regulatory environment" for a fintech idea).

## Downstream dependencies

What later sections will consume from section 02:

- **Section 03 (Form factor & differentiation)** will consume the dimensions of competitive choice (Task 4) and the white-space findings (Task 3) when generating the differentiation hypothesis. Section 03 will also reference the incumbent landscape (Task 1) when running the wrapper test against general-purpose LLMs.
- **Section 04 (Risk & compliance)** will reference the regulatory environment surfaced in this section's research — and any data-availability facts surfaced here — building on them with the full risk, compliance, data-access, and capability analysis.
- **Section 05 (Business model)** will reference incumbent monetization patterns when evaluating business models for the idea.
- **Section 07 (Investment & GTM)** will reference substitute behavior and choice dimensions when evaluating acquisition strategies — how do users currently find substitutes, and what does that imply about how they'd find this idea?
- **Section 08 (Financial projections)** will reference the Market size estimate as a primary input to the revenue projections.
- **Section 09 (Decision)** will reference the Market size score (with conviction label) when assembling the overall commercial score and applying the matrix.