# Template: 06 — Problem severity, market & competitive

## Purpose of this section in the framework

Section 06 is the **first evaluation section**, run once for each idea that 05 selected, in that idea's folder (`ideas/<idea-name>/`). It answers three questions about the idea in the handoff:
- How severe is the problem (or desire) for the people this idea serves?
- Who already competes for them, and where is the room?
- Is the market large enough for this idea to reach its threshold?

This section produces:
- A score on the **Problem severity** dimension, for the idea's own target user
- The idea's competitive landscape: incumbents, substitutes, white space and the dimensions people choose on
- A bottom-up SOM estimate and a score on the **Market size** dimension
- A recommendation to proceed to 07, or a kill of this idea at the **Problem gate** or the **Market gate**

Section 06 **judges the idea it was handed.** It does not choose another market, segment or user, propose a different threshold, or suggest a pivot. If the idea fails, that is a finding against this idea; the alternatives already exist in 04 and in 13's flagged ideas (see `SKILL.md`, "No alternatives after the screen").

## Inputs

- **05's handoff for this idea:** who it serves, what is sold and who pays, form factor, market, scale ambition, **threshold**, and the open assumptions it relies on. 06 never changes the handoff.
- **`03-brief.md`:** the target user, key evidence and pinned key figures.
- **`01-discover.md`:** the Current behaviour, Existing solutions and Constraints findings, which 06 reuses instead of researching again.
- **`02-define.md`:** the insights the idea builds on.

## Research activated in this section

Web search is **mandatory** here. Unless the Problem gate fires first (Task 1), it must produce, at minimum:
- 3–5 named direct incumbents **in the idea's market**, with what they actually offer (features, depth and price, including free tiers);
- any substitutes or workarounds specific to this idea that 01 did not already cover;
- the population and spending data the SOM needs;
- for an idea that serves someone other than 03's target user, the evidence for that user's problem.

Do not re-research what 01 already found; cite it.

Deep research is warranted when the market is unfamiliar enough that orienting takes significant work, or when the landscape is fragmented into many small players. Follow the pause in `SKILL.md`, "Research and deep research".

**Source quality.** Prefer company filings, official statistics, registries, regulators, real pricing and transaction data, and reputable industry publications. Treat blog posts, aggregator lists and AI-generated content with suspicion; they copy each other's errors, especially about local markets. Label by evidence quality, cite at the point of use, pin load-bearing figures once, and add named specifics to the claims-to-verify list (`SKILL.md`, standing habits).

**Local lens.** Search in the idea's market explicitly ("ticket booking apps Colombia", not "ticket booking apps"), and refine any search that returns mostly US results. Do not assume that global incumbents, prices, regulations or channels apply locally.

## Analytical work for this section

### Task 1: Score Problem severity

**Define the user.** If the idea serves 03's target user, reuse that definition. If it serves someone else, define that user the same way: role or identity, the characteristics that affect the problem, how often they meet it, and what they do today.

**Characterize the problem for that user:** what goes wrong (or what they want and cannot get), how much it costs them when it happens, how often, and how tolerable their workarounds are. Reuse 01–03's evidence; add only what is specific to this idea's user.

**Score** Problem severity on the 0–10 scale in `rubric.md`, with an H/M/L conviction label. Apply the anchors from `rubric.md`, the **canonical source** (this is a synced copy; keep it in sync if the rubric changes):
- **High (8–10):** multiple signals of acute pain. Users pay for inadequate workarounds, *and* the problem is both frequent (weekly or more) and material (costs significant time, money or friction). Unprompted complaints may also appear, but they are not enough on their own.
- **Medium (5–7):** users acknowledge the problem when prompted; one or two signals present, not all. Workarounds exist and are imperfect but tolerable.
- **Low (0–4):** the problem is hypothesized but not validated, or users don't recognize it as a problem when asked.

The conviction label reflects evidence quality, not source type.

**Desire-driven ideas.** The anchors are written for painkillers. If the idea answers a desire rather than a pain, score honestly against the anchors as written, say where they read low by construction, and record it as a finding (13 reports it). This does not change the idea's calibration scope, which follows the product type (`SKILL.md`, "Calibration scope").

**The Problem gate.** A score of **0–2** is a fatal commercial veto for this idea: an early exit. Apply the anchor honestly; the 2/3 line is a cliff, so score the evidence, not the consequence. If the gate fires, skip Tasks 2–4 and follow "If the idea is killed" below.

### Task 2: Map the competitive landscape

**Incumbents.** Name 3–5 direct incumbents in the idea's market: players already serving this need for these people, or something closely adjacent. Expand only if the market is fragmented with no clear leaders. For each:
- what they **actually** offer, from their product, pricing and reviews, not their marketing or category label;
- who they serve;
- what they do well and poorly, from the user's point of view;
- their position (leader, niche player, recent entrant, declining).

**An incumbent offering something similar is not the same as offering this idea.** Judge depth, not existence: a basic or shallow version, even a free one, can leave real room. Say specifically what each incumbent does and does not do.

**Substitutes.** Start from 01's Current behaviour and Existing solutions findings. Add only substitutes specific to this idea: adjacent products, manual workarounds, and not engaging at all. For each, note how widely it is used, how painful it is, and whether users would actually switch.

**White space.** Name what is not addressed, addressed poorly, or addressed only expensively, specifically: "no one does X for Y users at Z price" is white space; "the market could be better" is not. If there is none, say so; that raises the bar for 07's differentiation hypothesis but is not by itself a kill.

**Choice dimensions.** Name the 3–4 dimensions on which people actually choose in this category (for example: speed, price transparency, payment flexibility). No full feature matrix and no vague dimensions ("better UX"). 07 builds the differentiation hypothesis on these.

**Local lens.** How does the landscape in the idea's market differ from the global picture: local players, informal substitutes (WhatsApp groups, community marketplaces, government services), and local factors that change which dimensions matter?

If the research turns up regulatory facts that shape who can compete, or facts about data, API or partnership access (a closed ecosystem, a gatekeeper), record them for **08** rather than scoring them here.

### Task 3: Estimate the SOM

Build the SOM **bottom-up**:
1. Define the user segment numerically (e.g., "independent restaurants with 10–50 staff in Bogotá and Medellín").
2. Estimate its size, from census, registry or industry data. Reuse 03's pinned figures where they apply.
3. Estimate the share realistically reachable within the first 3 years.
4. Estimate the average revenue per user per year, from 05's revenue model and comparables. For pass-through models (marketplaces, resellers, agencies), use the revenue the business keeps.
5. Multiply to get the SOM, and pin it as a per-idea key figure.

Cite every step. Conviction reflects the quality of the inputs: census and industry data → H; analogous markets → M; ungrounded assumptions → L. Do not adjust a step to reach a desired score.

### Task 4: Score Market size

Score Market size on the 0–10 scale in `rubric.md`, with an H/M/L conviction label, comparing the SOM against **05's threshold**. Apply the anchors from `rubric.md`, the **canonical source** (synced copy):
- **High (8–10):** the SOM clears the threshold with conservative assumptions. Bottom-up, not an analyst-report TAM.
- **Medium (5–7):** the SOM is plausible at base-case assumptions; it clears the threshold only at optimistic ones.
- **Low (0–4):** even the optimistic SOM doesn't clear the threshold, or the math depends on assumptions with no evidence.

Clearing by 50% or more under conservative assumptions is High-band.

**The threshold is fixed.** 06 does not adjust or re-derive 05's threshold; it scores against it. If the threshold itself looks wrong, say so in the Rationale, and 13 reports it.

**A Market-gate kill rests on the threshold too.** If the gate would fire and 05's threshold carries Low conviction, the kill rests on a Low-conviction decision-critical claim, so it escalates under the conviction-gated rule (`SKILL.md`, "Kill confirmation") rather than auto-confirming.

**The Market gate.** A score of **0–2** is a fatal commercial veto for this idea. Before it fires, run the **every-assumption check**: confirm that the SOM fails the threshold under *every* reasonable assumption, not just the conservative case. The 2/3 line is a cliff; score the evidence, not the consequence.

### If the idea is killed

A kill at either gate ends **this idea**, not the run. Follow the kill protocol in `SKILL.md`, "The kill model":
- Write all four required parts.
- Apply the challenge pass to the kill itself, using the section-specific questions that test that gate.
- Confirm the kill per the conviction-gated rule (a kill resting on a Low-conviction decision-critical claim escalates).
- The commercial veto is a **clean kill**: no pivot, no alternative segment or market.

13 records the stop-point and the sections not run. The run then continues with the next selected idea, if any.

## Section-specific content for the four required parts

The four required parts are mandatory per `SKILL.md`.

### Analysis

Six labelled subsections, in order:
1. **Problem severity:** the user, the problem, the score and its conviction.
2. **Incumbents.**
3. **Substitutes.**
4. **White space and choice dimensions.**
5. **Local lens.**
6. **SOM and Market size:** the bottom-up table, the score and its conviction.

Then a **For 08** line (any regulatory, data or access facts surfaced here), a **Pinned figures** line (the SOM and any other figure pinned here) and the section's claims-to-verify list. If the Problem gate fired, only subsection 1 is written.

### Recommendation

One of three:
- **"Proceed to 07."**
- **"Kill — Problem gate"** (Problem severity 0–2).
- **"Kill — Market gate"** (Market size 0–2, after the every-assumption check).

### Rationale

Four to six sentences: the problem's severity for this user and the evidence behind it; the competitive picture (who, where the room is, the key choice dimensions); the SOM reasoning in summary (segment size, reachable share, revenue per user); and both scores with their conviction labels.

### Challenge pass

The judging form from `SKILL.md` (06–13 omit the "non-obvious option" question), plus the section-specific questions below. Each finding uses the fixed short format: what changed and why, or "no change".

## Challenge pass: section-specific questions

**Problem severity:**
- **Bubble check:** is the problem felt mainly by people like the founder? Would it look different outside that circle?
- **Frequency check:** has severity been confused with frequency? An acute but rare problem is not the same as a mild but constant one.
- **Workaround check:** are the workarounds actually painful, or tolerable enough that people don't look for something better? "I do this manually" is not "I would pay to stop doing this manually."
- **Articulation check:** would these people describe this as a problem in their own words?

**Market and competition:**
- **Coverage check:** did the search miss incumbents without strong English-language presence, B2B players hidden from consumer search, or recent entrants?
- **Depth check:** was any incumbent judged by its category or marketing rather than by what it actually does?
- **Switching check:** would people actually leave their current substitutes, or are those good enough in practice?
- **SOM-vs-TAM check:** is the SOM really what this idea can capture in its first years, or has it slipped into total market size? TAM × a small percentage is not a SOM.
- **White-space realness:** if no one fills this gap, why not? "No one has done it yet" is rarely the whole answer. Rule out: tried and failed, economics that don't work, regulatory barriers, no real demand. A timing window needs evidence.

## Word cap

**Hard maximum (provisional): 1,500 words, excluding citation markers and the source list.** Incumbents and substitutes can be compact tables; the SOM is a short table plus two or three sentences.

## Downstream dependencies

What later sections consume from section 06:
- **07** builds the differentiation hypothesis on the choice dimensions and white space, and uses the incumbents in the wrapper test.
- **08** builds on the regulatory and data-access facts surfaced here.
- **09** uses incumbent pricing and monetization as benchmarks for the idea's unit economics.
- **11** uses the substitutes, choice dimensions and user definition to judge acquisition channels.
- **12** uses the SOM as a primary input to the revenue projections.
- **13** uses the Problem severity and Market size scores, with conviction labels, in the commercial score.
