# Idea Discovery Rubric

## Purpose

This file defines how ideas are scored and decided during discovery. `SKILL.md` describes the process; this file describes the measurement. Section templates reference the rubric when they ask Claude to assign scores, and section 13 reads it in full to assemble each idea's scores and reach its verdict.

The rubric exists to make scores comparable across ideas. Without consistent anchors, a 7 on the third idea means something different than a 7 on the first, and the portfolio decision becomes guesswork. With anchors, scores stay calibrated as the portfolio grows.

The rubric is read in parts, not end-to-end. Each section template activates the dimension anchors it needs; section 13 reads the rubric in full.

## How scoring works

**Nothing is scored before section 06.** The first diamond (01–03), ideation (04) and the screen (05) carry no scores. From 06 onward, each idea selected by 05 is scored on its own.

Per idea:
1. **Commercial score (0–10):** the decision axis. It measures whether the idea can make money, and it is the **only** input to the verdict. It can kill an idea at low values.
2. **Solo-buildability score (0–10):** a **sidebar**. It measures how realistically the founder can ship an MVP given current skills, time and capital. It is scored so that it stays calibrated and comparable, but it **never influences the verdict** and never kills an idea. It appears in section 13 as a short build box under the verdict.
3. **Agent-fit:** a qualitative, descriptive output, not a number. It records whether the idea is genuinely agent-shaped and how well its form factor fits. It never influences the verdict.

The verdict (pursue / validate-first / kill) comes from the commercial score, the vetoes and the borderline band (see "The decision" below).

Every score gets a conviction label (H/M/L) following the standing habit in `SKILL.md`. "Conviction and scoring" below covers how conviction interacts with scores and decisions.

Dimension scores are assigned in the section that owns each dimension: Problem severity and Market size in 06, Defensibility provisionally in 07, and Monetization clarity in 09. Section 13 assembles the commercial score by averaging the four. A fatally weak dimension (0–2) is handled as a *veto*, not averaged in; see "The kill model".

## Commercial score (0–10)

### What it measures

The likelihood that this idea can produce sustainable revenue at a meaningful scale within a realistic timeframe. Not "is the idea interesting" or "does the problem exist"; those are inputs. The score answers: *given everything we know, can this make money?*

### Dimensions

Four dimensions feed the commercial score. They are weighted equally, and the commercial score is their simple average. A dimension scored **0–2 is fatal** and becomes a *veto* (see "The kill model") rather than dragging the average; a milder multiple-weakness pattern is handled by the demotion below.

- **Problem severity:** how painful, frequent and urgent the problem is **for this idea's own target user** (which may differ from section 03's target user when an idea serves another side). *(Scored in section 06.)*
- **Market size:** the realistic serviceable obtainable market (SOM), not theoretical TAM: how many people will actually pay for this in the idea's market. *(Scored in section 06.)*
- **Defensibility:** what stops a larger competitor (an incumbent or a general-purpose AI) from absorbing this as a feature once it is proven. *(Scored **provisionally** in section 07 and **finalized in section 13**; see "The kill model".)*
- **Monetization clarity:** how obvious the idea's revenue model is, and how willing the target user (or an intermediary) is to pay. *(Scored in section 09.)*

*Data access is not a commercial dimension.* Whether the data, integrations or partnerships the idea needs are available to *anyone* is a **structural check in section 08** (a block there is a veto, not a score). Whether *this founder* can obtain them is a sidebar matter for section 10.

### Combining dimensions into the commercial score

The commercial score is the **arithmetic average** of the four dimensions (sum ÷ 4). There are no cap rules. Fatal dimensions (0–2) leave the average as vetoes, so the average only ever combines survivable dimensions (each ≥3).

**"Weak on multiple fronts" demotion.** If two or more dimensions score 3–4, the idea is **placed low-commercial regardless of the average**. This is a mechanical demotion that needs no human in the loop. It demotes the *placement*, not the score: the commercial score stays the honest average, and the demotion and its trigger (which dimensions were weak) are recorded. This keeps the filter tough on multiply-mediocre ideas without distorting the number.

**Overall conviction** on the commercial score is the **lowest conviction among the four dimensions**: the weakest evidence governs.

**Show your work:** in section 13, state the four dimension scores, the average, the overall conviction, and whether the demotion fired.

### Anchor descriptions (overall)

These describe what each overall band represents. The score itself is the average of the four dimensions; the bands are how to read the result, and a sanity check: if the computed score and the band diverge sharply, re-examine the dimension scores.

- **9–10:** Exceptional. Strong evidence across all four dimensions. The kind of idea that would attract investor interest immediately. Rare.
- **7–8:** Strong. Clear evidence on most dimensions, none weak. Worth pursuing.
- **5–6:** Plausible but uncertain. Mixed evidence; one or two dimensions are strong, others are weak or unknown. Worth more research before committing.
- **3–4:** Weak. Multiple dimensions are unconvincing; the idea would need substantial changes to be viable.
- **0–2:** Not reached as an *overall* score — a fatal dimension is a veto before the average is taken.

### Dimension-level anchors

Each dimension is scored on the same 0–10 scale. The High/Medium/Low bands below define what each range looks like for that dimension. The section that owns a dimension activates its anchors; Claude does not need to read all of them at once.

Each dimension also carries one or two *worked examples*: concrete scored sketches showing how a score and its conviction label combine. They are illustrative (anchors in use, to fight calibration cold-start before a portfolio exists), **not additional bands**, and deliberately generic. Score the actual idea against the bands, not against the examples.

**Problem severity** *(used in section 06):*
- High (8–10): Multiple signals of acute pain present — users pay for inadequate workarounds *and* the painpoint is both frequent (weekly or more) and material (costs significant time, money, or friction). Users may also complain about the problem unprompted, but unprompted complaints alone are not enough.
- Medium (5–7): Users acknowledge the painpoint when prompted; one or two signals present but not all. Workarounds exist and are imperfect but tolerable.
- Low (0–4): Painpoint is hypothesized but not validated, or users don't recognize it as a problem when asked.

*Worked examples:* **8/H** — SMBs reconcile payment-processor payouts against invoices every week, lose hours to it, and already pay a bookkeeper to fix the errors; interviews with a dozen of them confirm the pain and the spend (acute, frequent, material — primary evidence). **3/M** — hobbyist runners might like auto-tagged routes, but no one pays for tagging today and analogous apps show weak engagement (hypothesized, not felt as urgent — analogous evidence).

*Known limitation:* these anchors are written for painkillers. For an idea that answers a desire rather than a pain, score honestly against the anchors as written, say where they read low by construction, and record it as a finding that section 13 reports. This does not change the idea's calibration scope, which follows the product type (`SKILL.md`, "Calibration scope"). Whether to recalibrate this dimension for desire-driven ideas is an open item in `design-notes.md`.

**Market size** *(used in section 06):*
- High (8–10): SOM in the idea's market clears the idea's make-money threshold (set in section 05) with conservative assumptions. Bottom-up estimate, not analyst-report TAM.
- Medium (5–7): SOM is plausible at base-case assumptions; clears threshold only at optimistic ones.
- Low (0–4): Even optimistic SOM doesn't clear the threshold, or the math depends on assumptions that have no evidence.

*Worked examples:* **8/H** — a bottom-up SOM (national-registry counts × a conservative 3-year reach × realistic ARPU) clears the idea's threshold comfortably under conservative assumptions. **4/M** — the SOM clears the threshold only at a ~15% capture rate, well above comparable tools' 3–5%; at comparable rates it falls short (depends on an unevidenced assumption — analogous comparables).

**Monetization clarity** *(used in section 09):*
- High (8–10): At least one revenue model is obvious and proven in adjacent products. Target users (or intermediaries) demonstrably pay for similar things today.
- Medium (5–7): Plausible revenue model exists but isn't proven in this specific market or for this specific user. Requires testing.
- Low (0–4): No clear path to revenue, or all candidate paths require behaviors users don't currently exhibit.

The idea's revenue model is fixed by sections 04–05, so "a revenue model" here means the idea's own model, as evaluated in section 09.

*Worked examples:* **8/H** — a B2B ops tool whose target teams already pay for two adjacent per-seat SaaS products, the same model all three incumbents use (obvious and proven — demonstrated payment). **4/L** — a free consumer app hoping to later sell "aggregated insights," a path no comparable product in the category monetizes and one users don't pay for today (hypothetical path — own reasoning).

**Defensibility** *(scored provisionally in section 07, finalized in section 13; see "The kill model"):*
- High (8–10): **Structural moats** — proprietary or compounding data, transactional capability, network effects, regulatory licenses, deep switching costs, or persistent personalization that competitors can't easily replicate.
- Medium (5–7): Defensibility without a structural moat — **execution-tier moats** durable at the idea's threshold scale: owned distribution (an audience or channel the founder controls), taste/design/brand edge, focus and shipping cadence, a price/cost structure incumbents won't match, or a niche unattractive for incumbents to contest. A determined incumbent could match within 12–18 months, but plausibly won't bother. **Cap: without at least one structural moat, Defensibility does not exceed 6.**
- Low (0–4): No meaningful moat. A general-purpose AI tool or larger competitor could absorb this as a feature in weeks, *and* nothing — distribution, focus, niche economics — makes them unlikely to. *(0–2, once finalized at section 13, is a veto.)*

Two scoring rules for this dimension:
- **Score moat *potential*.** Every moat of an unbuilt product is prospective, so "prospective / pre-adoption / not yet observed" is never by itself a reason to discount. Score the structural potential of the moat on the evidence. The 8/M worked example below is the calibration: a reasoned, unbuilt moat can sit in the high band at M conviction.
- **Durability is scaled to the idea's make-money threshold** (set in section 05), not to an absolute "venture-durable" standard. At a $150–200k-ARR niche threshold, "sticky for its users and ignorable by incumbents" is creditable Medium-band defensibility; demanding decade-proof moats at that scale applies a bar the idea's threshold never set.

*Worked examples:* **8/M** — a two-sided marketplace whose value compounds with liquidity (a real network-effect moat), but it's unbuilt, so the moat is reasoned from comparable marketplaces, not yet observed (high band — analogous evidence). **6/M** — a solo product in a commodity category (site builders, image-generation APIs) with an owned 40k-subscriber distribution channel, a distinct taste/brand position, and a low-price structure that makes the niche unattractive for incumbents to contest; no structural moat, so capped at 6 — durable at the idea's threshold scale, not incumbent-proof (execution-tier — analogous evidence from comparable solo businesses). **3/H** — a "summarize my inbox" agent with no proprietary data or transactional capability, a failed wrapper test, *and* no distribution or niche protection; a general LLM does it directly and an incumbent could absorb it in weeks (no moat — strong evidence for the weakness).

## Solo-buildability (sidebar, 0–10)

### What it measures

How realistically the founder can ship an MVP given current skills, time and capital. The score answers: *can the founder realistically ship an MVP alone, and if not, how far from solo is it?*

The "MVP" is the version that can credibly test the value proposition, not a polished launchable product. Discovery is about confirming the bet, not delivering it.

This score is assigned in section 10.

### A sidebar, not an axis

- **No influence on the verdict.** Solo-buildability never influences the verdict, never kills an idea, never feeds a gate and never triggers a question to the founder. The verdict comes from the commercial score alone.
- **Shown as a build box.** It is shown in section 13 as a short build box under the verdict. It describes *how* a pursued idea would be built (solo, solo with significant learning, with a collaborator, or with a partner), never *whether*.
- **Still scored.** It is scored against the anchors below so that it stays calibrated against `user-profile.md` and comparable across ideas.
- **Skipped on an early exit.** Section 10 is skipped when section 09's locked-average early exit applies, because the idea is already decided.

### Anchor descriptions

Build times below are relative to **`user-profile.md`'s build-speed baseline**; read the baseline build window and the learning tiers from there.

- **9–10:** Trivially solo-buildable. Ships solo **within the baseline build window**, using skills the user already has or can learn within it. No partnerships, licensing, or external capital needed for MVP.
- **7–8:** Solo-buildable with effort. Ships solo in the **new-but-accessible-learning tier** (per the profile) — learning new but accessible skills (frontend frameworks the user hasn't used, basic backend, integrations with public APIs). No partnerships required, but may benefit from one.
- **5–6:** Solo-buildable with significant learning or specific tools. Ships solo in the **significant-learning tier** (per the profile), OR within roughly the baseline window if the user brings in one specific collaborator for a defined component.
- **3–4:** Needs partnership for one critical component. Requires a meaningful partnership (technical co-founder, domain expert, data partner) to ship a credible MVP within a realistic action window. A solo path exists but is impractical given the user's skills and the time required.
- **0–2:** Requires team, capital, or licensing the user does not have. No realistic solo or single-partnership path to MVP.

*Worked examples:* **9/H** — a self-serve web app over a Supabase backend with public-API integrations, squarely in the profile's documented frontend + simple-database capability; ships within the baseline window. **3/M** — the core is a real-time, high-reliability matching engine at scale, needing a backend specialist the profile lacks; a solo path exists but is impractical (adjacent-capability reasoning, not a documented match).

## Agent-fit (qualitative)

### What this captures

Whether the idea is agent-shaped, and how well its form factor (chosen in section 05) fits the problem. The output is a short qualitative note, not a number.

**This is not a viability filter.** Some ideas are simply not agentic, and that's fine; the rubric is not trying to force an agent shape onto problems that don't need one. A great non-agentic idea is still a great idea. Agent-fit does not determine whether an idea is pursued; the commercial score does.

### Default verdict and purpose

Agent-fit defaults toward *not agent-shaped* and requires evidence to move off it. When an idea's form factor is "an agent", that is a hypothesis to challenge, not a starting assumption. The failure mode this guards against is rationalizing an agent shape onto a problem better served by a simpler form factor.

The operational method (the five evaluation lenses with their anti-examples, the verdict heuristic and default skepticism) lives in template 07, where the evaluation is performed. This section defines the output format, the wrapper-test downgrade rule, and how the verdict is used.

Agent-fit exists for two reasons only:
1. To record honestly what would be built, and how well the chosen form factor fits, so the founder has clarity on what they would actually be building.
2. To give portfolio-level visibility across evaluations (see "How agent-fit is used").

This verdict is assigned in section 07.

### Format

Agent-fit is captured as a short note with three parts:
1. **Verdict:** one of *strong agent fit*, *partial agent fit*, or *not agent-shaped*.
2. **Reasoning:** one sentence explaining the verdict, grounded in the specific characteristics of the idea (not generic agent-versus-non-agent talking points).
3. **Form factor and fit:** the form factor from section 05's handoff, with section 07's fit judgement (good / adequate / poor). Section 07 does not recommend a different form factor; form factors are explored in 04 and chosen in 05.

Example formats:

> **Verdict:** Strong agent fit.
> **Reasoning:** The discovery moment (what should I watch tonight, given mood, time, traffic and a partner's preferences) genuinely benefits from dialogue and multi-source synthesis that a filter UI can't replicate.
> **Form factor and fit:** Agent with a web fallback for direct-intent users. Good fit.

> **Verdict:** Not agent-shaped.
> **Reasoning:** The core workflow is invoice-to-budget matching, which is deterministic data processing; users want speed and accuracy, not conversation.
> **Form factor and fit:** Web app with a rules engine. Good fit; an LLM helps only with ambiguous invoices.

> **Verdict:** Partial agent fit.
> **Reasoning:** The core task (expense categorization) is deterministic, but the surrounding workflow (budget guidance, anomaly investigation) benefits from dialogue.
> **Form factor and fit:** Pure agent. Poor fit: over-engineered for the deterministic core (recorded as a finding against this idea).

### The wrapper-test downgrade rule

In section 07, after assigning an initial agent-fit verdict, Claude runs the wrapper test (defined in template 07, Task 2): *what does this purpose-built product do that a general-purpose LLM (Claude, ChatGPT, Gemini) couldn't do for the user directly?*

- If the wrapper test *passes* (the product offers something a general-purpose LLM cannot), the agent-fit verdict stands.
- If the wrapper test *fails* (a general-purpose LLM can do this adequately), the verdict is downgraded by one level: *strong* becomes *partial*, *partial* becomes *not agent-shaped*. A failed wrapper test on a *not agent-shaped* idea is consistent and needs no change.

The wrapper test also feeds the Defensibility dimension (low defensibility for thin wrappers) and section 08's capability-feasibility check. The agent-fit interaction above is independent of both; it is about an honest description of what would be built, not commercial viability.

### How agent-fit is used

Agent-fit is a descriptive output, not a decision input. The founder reads it alongside the verdict, but it never changes a verdict, overrides a kill or breaks ties between ideas.

**Use 1: An honest record of what would be built, for execution planning.** After a pursue verdict, the founder needs to know what they would actually be building and whether its form factor fits. A poor fit is recorded as a finding against the idea.

This applies only after a pursue or validate-first verdict. For killed ideas, agent-fit is documented in the analysis but has no further role.

**Use 2: Portfolio-level pattern visibility.** Across evaluations, the distribution of verdicts is itself informative: if most ideas come up "not agent-shaped", that says something about the opportunities being generated. This lives in the cross-idea calibration step (`SKILL.md`). It applies across the portfolio, not within one evaluation.

### What agent-fit is not used for

- It does not change a verdict.
- It does not override a kill.
- It does not break ties between ideas. If several ideas are comparable, the founder weighs them by whatever criteria they choose; agent-fit has no privileged role among those criteria.
- It does not reward an idea for being "more agentic", or penalize one for being "less agentic".

## Conviction and scoring

### Purpose of this section

The standing habit in `SKILL.md` is to apply H/M/L conviction labels to every judgement call, score and quantitative estimate. This section defines how conviction is used *during scoring and deciding*: how it affects comparison between scores and decisions, and what rules prevent it from being misused.

### Conviction definitions (reference)

Restated from `SKILL.md`:
- **High (H):** backed by external evidence: interviews, primary data, market research, observed behaviour, transactions you can point to.
- **Medium (M):** backed by analogous evidence: similar products' performance, indirect signals, reasoning from comparable markets, structured assumptions from credible sources.
- **Low (L):** your own reasoning, with no external validation yet. The judgement may be sound, but it has not been tested against the world.

Conviction is a label on *evidence quality*, not on the founder's or Claude's confidence. A judgement can feel highly confident and still be Low conviction if no external evidence supports it.

**Quality, not source type.** Conviction tracks how *directly and reliably the evidence measures the specific claim*: its directness, methodological soundness, representativeness and recency. It does not depend on whether the source is "primary" or "secondary". This framework's research is almost always secondary, so source type alone never sets the tier. An authoritative secondary source (official statistics such as a national registry or census, a rigorous published survey, real transaction or pricing data) can be **H**, while a small or poorly run primary study is not. Two guardrails follow:
- *"I only have secondary sources" is never a justification for M.* The basis for M is that the evidence is **indirect or analogous** (comparable products' performance, the mere existence of a paying category, structured assumptions from credible sources), not that it is secondary.
- *The mere existence of a primary study does not confer H.* Its quality must be assessable and sound; otherwise it is labelled for what it actually supports.

The route to upgrading conviction is direct, sound measurement of the claim, which authoritative secondary sources can provide too, not the mere acquisition of a document.

### The no-distortion rule

A score must reflect an honest reading of the dimension anchor, regardless of how much evidence backs it. Distorting a score because conviction is Low, in either direction, is a misuse of the rubric.

The score answers: *where does the evidence I have point?*
The conviction label answers: *how good is that evidence?*

These are independent. Don't inflate a score because evidence is thin (to make the analysis feel more decisive), and don't deflate it either (out of false humility). Both distortions corrupt the rubric. The conviction label is the dedicated mechanism for representing evidence quality; using it as designed keeps the score honest.

The correct pattern when evidence is thin:
- Assign the score that best matches the anchor on what is known.
- Label conviction L.
- Note what evidence would upgrade it.

The incorrect patterns:
- Scoring higher than the evidence supports because it "feels right" or "the upside is large".
- Scoring lower than the anchor supports, out of false humility.
- Skipping the conviction label, or defaulting everything to M.
- Treating low conviction as a reason to defer scoring entirely.

Low conviction is not a failure of the analysis. It is an honest signal of where research would most improve the decision.

### How conviction modifies comparison between scores

Within a single idea, the dimension scores combine into the commercial score by averaging; the score layer is conviction-invariant (see "Score layer vs decision layer"). Conviction does not change a dimension's value: a 2/H is a veto the same way a 2/L is, although a low-conviction veto routes through the validation layer before the kill stands.

Conviction matters when *comparing ideas*, as section 13's comparison does. The principle:

> When conviction differs significantly between two ideas being compared, the comparison is not yet a decision; it is a research prompt. The default action is to upgrade conviction on the weaker-evidenced side before committing. The fallback, when research is not possible within the founder's time or budget, is to prefer the higher-conviction score, because committing on weak evidence is riskier than committing on strong evidence at a slightly lower score.

Worked examples, all following the same principle:
- **Idea A: commercial 7/H vs. Idea B: commercial 7/L.** Same score, different evidence. Default: don't choose yet; run the cheapest test that could move B to 7/M or 7/H. Fallback: prefer A.
- **Idea A: commercial 6/H vs. Idea B: commercial 7/L.** A common case. The 6/H is real; the 7/L is a hope. Default: upgrade conviction on B, since the gap is small enough that the comparison depends on whether the 7 holds. Fallback: prefer A.
- **Idea A: commercial 8/L vs. Idea B: commercial 6/H.** A large gap, with conviction reversed. Default: run the smallest test that could move A to 8/M. If it survives, A is the clear winner; if not, its score drops and B wins. Fallback: prefer B; acting on an 8/L is a speculative bet, acting on a 6/H a documented one.

Across all three: conviction differences are not tiebreakers. They signal that the comparison is incomplete, and the work of completing it is research. The comparison never changes a verdict; each idea's verdict is fixed on its own evidence first.

### Using conviction to prioritize research

Conviction labels turn the rubric into a research agenda, not just a scorecard. After scoring, scan for Low-conviction labels on dimensions that materially affect the decision. Priority:
1. **Low conviction on high-impact dimensions.** If Monetization is 7/L, validating it (or revising it down) changes the commercial picture more than refining a 9/H elsewhere.
2. **Low conviction near a boundary.** A 3/L where a 2 would trigger a veto, or a dimension right at the 2/3 line, is high-priority: the boundary is decision-relevant.
3. **Low conviction with cheap validation paths.** A market size that an afternoon of bottom-up estimation could sharpen is a faster upgrade than a defensibility judgement that needs interviews with competitors' customers.

Section 13 lists the highest-priority Low-conviction items as suggested research, in this order, among its open items.

### Score layer vs decision layer

Conviction operates on two layers:
- **Score layer: conviction-invariant.** A dimension's value doesn't move with conviction (a 2 is a 2 at H or L); the overall commercial conviction is the *lowest of the four*. The no-distortion rule lives here.
- **Decision layer: conviction-sensitive.** The **borderline band** uses conviction near the 6.0 threshold, and the validation layer and kill-confirmation rules below gate decisions that rest on thin, load-bearing evidence.

So "a 2/L vetoes like a 2/H" (score layer) and "low-conviction decisions get validated" (decision layer) are one coherent system, not a contradiction.

### The validation layer

At any decision (proceed *or* kill), identify the **decision-critical** low-conviction claims: the load-bearing ones that would flip the decision if wrong, ranked by the priority rules above. The decision is not final until each is **validated** (researched) or **explicitly accepted** as a recorded risk ("proceeding / killing on thin evidence on X, eyes open").

It is symmetric: it applies to proceeds and kills alike. It gates only the load-bearing low-conviction items, not every L label, so it adds discipline, not weight.

**A companion, verifiability-gated layer.** The validation layer gates on *low conviction*, so it will not catch a **confidently stated** fabrication, or a load-bearing figure that drifts between sections. That is the highest-risk case, because hallucination concentrates on confident specifics, and it is the job of the **fact-verification habit** in `SKILL.md`:
- cite at the point of use with source and conviction;
- pin load-bearing figures once;
- roll them into a claims-to-verify list;
- justify every blanket conclusion.

It is backed by the facts question in the challenge pass. The two compose: conviction-gated validation for *judgements*, verifiability-gated checking for *facts*. Neither replaces the other.

### Kill confirmation (conviction-gated)

When a kill (or a park) pauses for the founder is canonical in `SKILL.md`, "Kill confirmation". The decision-layer principle behind it: a stop escalates exactly when it rests on thin, decision-critical evidence, which is the validation layer at work; there is no separate gate. The one escalation that is not about a stop, section 13's high-commercial / weak-financial contradiction, is covered under "Borderline band".

## The decision (commercial score)

### Purpose

The verdict for each idea comes from its **commercial score alone**, applied in section 13. Vetoes are resolved *before* the decision (see "The kill model"), so the decision only places ideas that survived every dealbreaker. A low-commercial placement here is a **commercial-score kill**: death by mediocrity, not by a single fatal flaw.

Solo-buildability is not an input. It is reported beside the verdict as the build box (see "Solo-buildability (sidebar)").

### The threshold

The split between high and low commercial is **6/10**: 6 or above is high, 5 or below is low.

- The dimension anchors define 7+ as "strong" (clear evidence, worth pursuing) and 5 or below as "weak or insufficient" (mixed evidence, not yet supported). A 6 is the borderline case between them.
- 6 sits on the high side because being stricter than the anchors would mean killing ideas the anchors themselves describe as plausible.
- 5 sits on the low side because the anchors call it "plausible but uncertain": the uncertainty is unresolved, so the idea is not ready to act on.

**Conviction at the threshold** is handled by the **borderline band** below. A 6/L is never simply "high": that would be inflation through the decision, which the no-distortion rule prevents in scoring. The band replaces a blunt demotion with scrutiny, not optimism.

**The "weak on multiple fronts" demotion** (two or more dimensions at 3–4) places an idea low-commercial regardless of its average. Both it and the band affect *placement*, not the underlying score, and both hold in autonomous mode.

### Borderline band

A crisp verdict *right at* the 6.0 line manufactures false confidence: the framework is least reliable exactly where the score is closest to the threshold. So a commercial score in the **5.5–6.5 band at M or L conviction** does **not** produce a crisp verdict. Instead:
- **Flag it "too close to call"** and make a **documented qualitative call** with **three possible outcomes: pursue, validate-first or kill.** The moat and defensibility read governs the direction but does not foreclose pursue:
  - a creditable moat (structural *or* execution-tier, per the Defensibility anchors) with a coherent financial picture can resolve to **pursue**, named per the pursue vocabulary below;
  - a plausible but unverified case resolves to **validate-first**: pursue needs every load-bearing claim at M or H, so one still at Low makes the call validate-first;
  - no moat leans to **kill**.
- **Validate-first** is a formal verdict, not a hedge. Its payload is mandatory; a validate-first without all three parts is incomplete (checked in section 13's self-audit):
  - the **named load-bearing assumptions**: the specific claims the decision turns on, drawn from section 03's open assumptions where they apply, plus any specific to the idea;
  - **cheap validation tests** for each, with rough cost and effort (interviews, a waitlist test, a pricing probe);
  - **explicit flip conditions** ("if X, pursue; if Y, kill").
- **Trigger elevated scrutiny:** re-verify the load-bearing claims behind the four dimensions (via the fact-verification habit in `SKILL.md`) and reconcile any tensions between them before making the call.
- **The band call is provisional until the financial-coherence check** (template 13, Task 5). A band case resolving toward pursue or validate-first against a **weak** financial picture triggers the mandatory high-commercial / weak-financial escalation, exactly as a crisp ≥6 placement would; the band must not resolve upstream of that check. The **inverse tension** (favourable financials against a borderline commercial score, for example a base case that clears the idea's threshold) is fed into the qualitative call explicitly and documented, not resolved ad hoc.

**Precedence**, so the near-threshold rules stay consistent:
- The band **subsumes** the conviction-at-threshold case: a 6.0/L lands in the band and is resolved by scrutiny and a qualitative call (usually still kill when no moat is present, but reasoned rather than mechanical).
- The **"weak on multiple fronts" demotion takes precedence**: if two or more dimensions scored 3–4, placement is crisp low-commercial, not borderline.
- **H conviction** anywhere in 5.5–6.5 stays crisp, with the 6.0 threshold applying as normal. Strong evidence supports the placement, so there is no false-decisiveness risk.

**Autonomous mode:** the borderline outcome is a flag plus a documented determination with elevated scrutiny, not a new pause. A **validate-first is emitted as the final verdict** (with its full payload) unless the validation layer independently fires on a decision-critical low-conviction claim, or the financial-coherence escalation fires. **Checkpoint mode:** it pauses like any section.

**Calibration discipline applies with force here:** prior band cases' *verdicts*, and sibling ideas' verdicts, are not evidence for this one (see "Calibration note").

### Verdicts

**Pursue vocabulary: durability is priced into the verdict.** Every pursue verdict (crisp or band-resolved) is named for its durability tier:
- **pursue-durable:** the defensibility case rests on at least one structural moat;
- **pursue-as-lifestyle-bet:** it rests on execution-tier moats creditable at the idea's threshold scale (see the Defensibility anchors), so it is durable at solo scale but not incumbent-proof.

The label does not change the action. It makes the durability question visible in the verdict, rather than letting an implicit "durable business" standard silently decide the outcome.

**The verdicts:**
- **Pursue** (commercial ≥6, crisp, no demotion; or band-resolved). Proceed to execution planning: KPI definition, MVP scope, launch roadmap. These live outside the discovery skill; the discovery deliverable is the verdict plus the inputs that would feed them. The **build box** says how it would be built. If that needs a partner, finding one (and the time that takes) is part of the next steps, not a condition on the verdict. "Pursue" means the idea is ready; sequencing is the founder's call.
- **Validate-first** (band-resolved only). Run the named cheap tests and apply the flip conditions.
- **Kill** (commercial <6 outside the band, or demoted; or band-resolved). A commercial-score kill of this idea. Nothing is attached to it (`SKILL.md`, "No alternatives after the screen").

### Visual reference

Section 13 shows each evaluated idea's **commercial position**: the commercial average on a 0–10 line, with the 6.0 threshold and the 5.5–6.5 band marked. The build box sits under the verdict. The position must be unambiguous. For example:

> "Commercial 6.75/M: above the band, crisp **pursue-as-lifestyle-bet** (execution-tier moats only). Build: 6/M: solo with significant learning (~4–6 months); a payments partner. MVP capital ~$5–10k."

> "Commercial 4.5/H: a crisp commercial-score kill, with strong evidence behind the weakness. Build: 8/H: solo (~6 weeks). MVP capital ~$1k." (The build box is shown, but it is not decision-relevant.)

The position statement, and the reasoning connecting the scores to the verdict, are mandatory in section 13. Implicit positioning ("somewhere between pursue and kill") is not acceptable.

## The kill model

This is the consolidated reference for every point at which an **idea** can be stopped. **A kill ends an idea, never the problem**; the run continues with the next selected idea. There are two kinds of stop: **vetoes** (dealbreakers) and the **commercial-score kill** (death by mediocrity).

### Vetoes

A **veto** is a dealbreaker: a condition that kills the idea regardless of how strong everything else is. A veto **fires at the section where its condition is definitively assessable**, and it is a *conclusion from research*, never a substitute for it. It fires only on adequately researched findings, and a low-conviction veto routes through the validation layer (verify before the kill stands).

Two families:

**Commercial vetoes:** a commercial dimension scored **0–2** (fatal):
- **Problem severity 0–2** (no real or severe problem for this idea's user): fires at section 06 (early exit).
- **Market size 0–2** (the market cannot reach the idea's threshold): fires at section 06 (early exit).
- **Monetization clarity 0–2** (the idea's model has no viable economics): fires at section 09 (Business-model gate, cause b).
- **Defensibility 0–2:** *not* definitive until section 13, because moats can emerge in 08 (regulatory) and 09 (data, network, business model). Scored provisionally at 07, **finalized at 13**, and vetoes there if still fatal (a *late* veto, not an early exit).

**Structural vetoes:** a structural block, assessed in section 08 (the Structural gate):
- **Legal / regulatory blocked.** A required licence counts as a block only if *no one* building this could obtain it. Whether this founder could hold it is a sidebar matter for section 10, never a veto.
- **Data access blocked.**
- **Capability infeasible** (current technology can't do this well).

Two further gates stop an idea without a dimension score: section 09's Business-model gate, cause **(a)** (the idea's revenue model does not survive the legal envelope), and section 11's GTM gate (no go-to-market strategy recovers its acquisition cost within the model's payback window, after the adjustment attempt).

### The gates (named by function)

A "gate" is a section where a veto can fire. Named by what they test:
- the **Problem gate** and **Market gate** (06): the early exits;
- the **Structural gate** (08);
- the **Business-model gate** (09);
- the **GTM gate** (11);
- the **Defensibility late veto** and the **commercial-score decision** (13).

Each gate's **firing conditions are canonical in `SKILL.md`, "The kill model"**. This rubric supplies the *measurement and routing*: what a veto is, how each veto routes, and the commercial-score kill.

### Veto routing: kill is the default, route by type

Every veto defaults to **recommend the kill**. Bedrock rule: **a partner can never rescue a commercial death**; a genuine lack of demand or revenue can't be partnered.
- **Commercial vetoes:** a **clean kill** of the idea. Never "needs a partner".
- **Structural vetoes** route uniformly:
  - **partner**, if a partner can supply the missing piece (a licensed partner for legal, a data partner for data, a specialized-capability partner for capability);
  - **kill**, if the piece is unavailable to anyone;
  - **park** (capability only), if the technology isn't there yet but is improving. A parked idea stops without being killed; section 13 records it with the capability change that would reopen it.

  The partner route is the same idea, run with a partner. Routing at section 08 uses a partial commercial picture (Monetization not yet scored, Defensibility still provisional), so a partner route is *conditional on the commercial case holding up*. The evaluation therefore **continues with the partner built in**: sections 09–12 price it, and the rest of the evaluation tests that condition.
- **Business-model gate, cause (a):** route to a licensed partner or a different legal structure for the *same* model when one exists (conditional on the commercial case, which the rest of the evaluation tests), and the evaluation continues with it built in; if none exists, kill.
- **GTM gate:** kill. Section 11's adjustment attempt (channel, pricing within the model, beachhead) comes before the gate, not after it.

### The commercial-score kill

An idea that survives **every** veto reaches the decision. If its commercial **average is below 6** (mediocre across the board, no single fatal flaw), it is a **commercial-score kill**, unless it falls in the **5.5–6.5 M/L borderline band**. There, the verdict is a documented qualitative call (pursue / validate-first / kill), not an automatic kill. The **"weak on multiple fronts"** demotion can also place an idea low-commercial regardless of its average, and it **takes precedence over the band**.

Section 09's **locked-average early exit** is this kill reached early: when the average cannot reach 5.5 (the bottom of the borderline band) even with Defensibility at its ceiling, the idea goes straight to 13 and 10, 11 and 12 are skipped (conditions canonical in `SKILL.md`). It is not a veto. In 13 the verdict still comes from the actual finalized scores, not the ceiling.

### Kill confirmation, challenge pass and documentation

Every kill, veto or commercial-score, includes the **challenge pass applied to the kill itself** (`SKILL.md`), and is **confirmed per the conviction-gated rule** (see "Kill confirmation" above). Once confirmed:
- section 13 records the stop-point, the finding and the sections not run;
- the run continues with the next selected idea, if any.

Process-gate findings (the structural blocks, the GTM economics test) are analytical, not scored. Where the underlying finding is uncertain (a contested legal reading, assumption-dependent economics), the uncertainty is documented in the kill rationale. If it is decision-critical and Low conviction, the kill escalates.

### What is not a kill criterion

- **Solo-buildability is never a kill criterion, and never a verdict input.** It is a sidebar.
- **The founder's own capabilities and credentials are never a kill criterion.** A licence this founder couldn't hold, or a skill gap, is priced or partnered (sections 10 and 11), not vetoed.
- **Agent-fit is never a kill criterion.** The verdict is descriptive only.
- **Conviction is never a kill criterion on its own.** Low conviction is a signal for research, not a kill.
- **Founder preference is never an *automated* kill criterion.** The founder may set an idea aside for personal reasons; that is recorded as a founder decision in section 13, distinct from a framework verdict.

## Calibration note

### Purpose

The rubric is reused across many ideas. Over time, the consistency of scoring across evaluations matters as much as the accuracy of any single score: the founder's portfolio decisions depend on a 7 today meaning the same thing as a 7 in six months. This section names the calibration concerns that develop *across* evaluations.

The cross-idea calibration mechanism lives in `SKILL.md`: comparing each idea, in section 13, with the three closest prior evaluations by domain or shape, **from other problem folders**. Sibling ideas from the same run are not calibration data; section 13 compares them side by side and checks that scores resting on the same evidence agree. This section names the failure modes that mechanism exists to catch.

### Score inflation

The most common failure in scoring systems used over time: the average score drifts upward as investment in the framework accumulates. Each new idea looks better than the last because of growing optimism about the process, attachment to the act of pursuing, or reluctance to record a "weak" verdict on something that took time to analyse.

Scores should be anchored to the anchor descriptions, not to current mood or to the relative strength of this month's ideas. A 7 in month one and a 7 in month twelve should describe ideas that are similarly strong against the absolute anchors, not similarly strong against each other.

Signs that inflation is occurring:
- Recent evaluations cluster at 6–8 on commercial, while earlier ones spanned 3–9.
- The anchors increasingly need generous interpretation to justify the scores.
- Kills have become rare.

**The correction.** When section 13's calibration check runs, it identifies the three closest prior evaluations by domain or shape and asks directly: does this idea genuinely deserve a higher commercial score than that prior idea, given what was known then? If the answer relies on a generous reading of the current idea, or a harsh reading of the prior one, the current score is inflated. Name the prior idea so the founder can compare them side by side.

The framework's purpose is to filter, not to validate. A portfolio in which most ideas score above 5 has stopped filtering.

### The verdict-ratchet guard

Cross-idea calibration checks **scoring consistency only, never verdict consistency**. "Does this idea deserve a 7 on Market when that prior idea earned a 6?" is the mechanism working.

**Disallowed reasoning:**
- "the portfolio has consistently killed this shape";
- "that prior idea was killed, so consistency requires killing this one";
- citing a prior or **sibling** kill as anchoring evidence for the current verdict.

Against a portfolio of accumulated kills, verdict consistency turns the anti-inflation check into a one-way ratchet: borderline cases get killed partly *for consistency with prior kills*, which is precedent, not evidence. Each verdict must stand on its own idea's evidence against the absolute anchors. Symmetrically, once the portfolio holds pursues, "we've been passing ideas like this" is not evidence for a pass. Section 13's self-audit checks that no verdict leaned on another idea's verdict.

### Conviction drift

A related failure, specific to conviction labels: over time, the temptation is to default to M on everything, neither boldly High nor humbly Low. Conviction drift corrupts the rubric more subtly than score inflation, because M can be assigned to anything without obvious red flags.

Medium is not a default. It is a specific claim, that *analogous evidence exists*, and the claim should be defensible.

**The correction:** when assigning M, note briefly what makes it M rather than L or H. If that can't be articulated (if there is no actual analogous evidence to point to, just a sense that the judgement is "more than a guess"), the honest label is L. M earned by default is the same problem as a 7 earned by default.
