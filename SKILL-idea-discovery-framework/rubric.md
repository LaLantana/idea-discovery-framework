# Idea Discovery Rubric

## Purpose

This file defines how product ideas are scored during discovery. `SKILL.md` describes the process; this file describes the measurement. Section templates reference the rubric when they ask Claude to assign scores, and `SKILL.md` references it for the matrix-driven decision in section 9.

The rubric exists to make scores comparable across ideas. Without consistent anchors, a 7 on the third idea means something different than a 7 on the first, and the portfolio decision becomes guesswork. With anchors, scores stay calibrated as the portfolio grows.

The rubric is read in parts, not end-to-end. Each section template activates the dimension anchors it needs; section 9 reads the rubric in full to assemble the overall scores and apply the matrix.

## How scoring works

Three scores are produced per idea:

1. **Commercial score (0–10):** the primary axis. Measures whether the idea can make money. Can kill an idea on its own at low values.
2. **Solo-buildability score (0–10):** the second axis. Measures how realistically the user can ship an MVP given current skills, time, and capital. Defines build strategy; never kills an idea by itself.
3. **Agent-fit:** qualitative descriptive output, not a number. Captures whether the idea is genuinely agent-shaped or whether a simpler form factor fits better. Informs execution planning after a proceed decision; does not influence the matrix.

Commercial × solo-buildability are plotted on a 2×2 matrix to drive the decision (see "The 2×2 matrix" below). Agent-fit is a separate descriptive output that informs execution planning after a proceed decision; it does not affect the matrix or any kill recommendation.

Every score gets a conviction label (H/M/L) following the standing habit in `SKILL.md`. The "Conviction and scoring" section below covers how conviction interacts with the scores during comparison.

Dimension scores are assigned in the framework section that owns that dimension (problem severity in section 01, market size in section 02, and so on). The overall commercial score is assembled in section 09 by averaging the four dimensions (a fatally weak dimension — 0–2 — is handled as a *veto*, not averaged in; see "The kill model" below).

## Commercial score (0–10)

### What it measures

The likelihood that this idea can produce sustainable revenue at a meaningful scale within a realistic timeframe. Not "is the idea interesting" or "does the painpoint exist" — those are inputs. The score answers: *given everything we know, can this make money?*

### Dimensions

Four dimensions feed the commercial score (all Desirability + Viability questions). They are weighted equally — the overall commercial score is their simple average. A dimension scored **0–2 is fatal** and becomes a *veto* (see "The kill model") rather than dragging the average; a milder multiple-weakness pattern is handled by the demotion below. Each dimension is scored in the framework section that owns it; the overall commercial score is assembled in section 09.

- **Problem severity:** how painful, frequent, and urgent the painpoint is for the target user. *(Scored in framework section 01.)*
- **Market size:** the realistic serviceable obtainable market (SOM), not theoretical TAM. How many people will actually pay for this in the target market? *(Scored in framework section 02.)*
- **Defensibility:** what stops a larger competitor (incumbent or general-purpose AI) from absorbing this as a feature once it's proven. *(Scored **provisionally** in framework section 03 and **finalized in section 09** — see "The kill model.")*
- **Monetization clarity:** how obvious the revenue model is, and how willing the target user is to pay (or how willing intermediaries are to pay on their behalf). *(Scored in framework section 05.)*

*Data access is no longer a commercial dimension.* Whether the required data, integrations, or partnerships are structurally available is now a **structural check in section 04** (a blocker there is a veto, not a 0–10 score); whether *this user* can obtain them is assessed in section 06.

### Combining dimensions into the overall commercial score

The overall commercial score is the **arithmetic average** of the four dimension scores (sum ÷ 4). There are no cap rules: fatal dimensions (0–2) leave the average as vetoes, so the average only ever combines survivable dimensions (each ≥ 3).

**"Weak on multiple fronts" demotion.** If two or more dimensions score 3–4, the idea is **placed as low-commercial on the matrix regardless of the average** — a mechanical demotion (parallel to the conviction-at-threshold rule) that needs no human in the loop. It demotes *placement*, not the score: the commercial score stays the honest average, and the demotion plus its trigger (which dimensions were weak) are recorded. This keeps the filter tough on multiply-mediocre ideas without distorting the number.

**Overall conviction** on the commercial score is the **lowest conviction among the four dimensions** — the weakest evidence governs.

**Show your work:** in section 09, state the four dimension scores, the average, the overall conviction, and whether the multiple-weak demotion fired.

### Anchor descriptions (overall)

These describe what each overall band represents. The score itself is the average of the four dimensions; the bands below are how to read the result (and a sanity check — if the computed score and the band diverge sharply, re-examine the dimension scores).

- **9–10:** Exceptional. Strong evidence across all four dimensions. The kind of idea that would attract investor interest immediately. Rare.
- **7–8:** Strong. Clear evidence on most dimensions, none weak. Worth pursuing.
- **5–6:** Plausible but uncertain. Mixed evidence; one or two dimensions are strong, others are weak or unknown. Worth more research before committing.
- **3–4:** Weak. Multiple dimensions are unconvincing; significant pivots would be needed to make this viable.
- **0–2:** Not reached as an *overall* score — a fatal dimension is a veto before the average is taken.

### Dimension-level anchors

Each dimension is scored on the same 0–10 scale as the overall commercial score. The High/Medium/Low bands below define what each range looks like for that specific dimension. The relevant dimension anchors are activated by the framework section that owns the dimension; Claude does not need to read all dimension anchors at once.

Each dimension also carries one or two *worked examples* — concrete scored sketches showing how a score and its conviction label combine. They are illustrative (anchors-in-use, to fight calibration cold-start before a portfolio of prior evaluations exists), **not additional bands**, and the idea sketches are deliberately generic — score the actual idea against the bands, not against the examples.

**Problem severity** *(used in framework section 01):*
- High (8–10): Multiple signals of acute pain present — users pay for inadequate workarounds *and* the painpoint is both frequent (weekly or more) and material (costs significant time, money, or friction). Users may also complain about the problem unprompted, but unprompted complaints alone are not enough.
- Medium (5–7): Users acknowledge the painpoint when prompted; one or two signals present but not all. Workarounds exist and are imperfect but tolerable.
- Low (0–4): Painpoint is hypothesized but not validated, or users don't recognize it as a problem when asked.

*Worked examples:* **8/H** — SMBs reconcile payment-processor payouts against invoices every week, lose hours to it, and already pay a bookkeeper to fix the errors; interviews with a dozen of them confirm the pain and the spend (acute, frequent, material — primary evidence). **3/M** — hobbyist runners might like auto-tagged routes, but no one pays for tagging today and analogous apps show weak engagement (hypothesized, not felt as urgent — analogous evidence).

**Market size** *(used in framework section 02):*
- High (8–10): SOM in the target market clears the user's "make money" threshold (defined per-idea in the brief) with conservative assumptions. Bottom-up estimate, not analyst-report TAM.
- Medium (5–7): SOM is plausible at base-case assumptions; clears threshold only at optimistic ones.
- Low (0–4): Even optimistic SOM doesn't clear the threshold, or the math depends on assumptions that have no evidence.

*Worked examples:* **8/H** — a bottom-up SOM (national-registry counts × a conservative 3-year reach × realistic ARPU) clears the brief's threshold comfortably under conservative assumptions. **4/M** — the SOM clears the threshold only at a ~15% capture rate, well above comparable tools' 3–5%; at comparable rates it falls short (depends on an unevidenced assumption — analogous comparables).

**Monetization clarity** *(used in framework section 05):*
- High (8–10): At least one revenue model is obvious and proven in adjacent products. Target users (or intermediaries) demonstrably pay for similar things today.
- Medium (5–7): Plausible revenue model exists but isn't proven in this specific market or for this specific user. Requires testing.
- Low (0–4): No clear path to revenue, or all candidate paths require behaviors users don't currently exhibit.

*Worked examples:* **8/H** — a B2B ops tool whose target teams already pay for two adjacent per-seat SaaS products, the same model all three incumbents use (obvious and proven — demonstrated payment). **4/L** — a free consumer app hoping to later sell "aggregated insights," a path no comparable product in the category monetizes and one users don't pay for today (hypothetical path — own reasoning).

**Defensibility** *(scored provisionally in framework section 03, finalized in section 09 — see "The kill model"):*
- High (8–10): Real moats — proprietary data, transactional capability, network effects, regulatory licenses, or persistent personalization that competitors can't easily replicate.
- Medium (5–7): Some defensibility through execution quality, brand, or first-mover advantage. A determined incumbent could match within 12–18 months.
- Low (0–4): No meaningful moat. A general-purpose AI tool or larger competitor could absorb this as a feature in weeks. *(0–2, once finalized at section 09, is a veto.)*

*Worked examples:* **8/M** — a two-sided marketplace whose value compounds with liquidity (a real network-effect moat), but it's unbuilt, so the moat is reasoned from comparable marketplaces, not yet observed (high band — analogous evidence). **3/H** — a "summarize my inbox" agent with no proprietary data or transactional capability and a failed wrapper test; a general LLM does it directly and an incumbent could absorb it in weeks (no moat — strong evidence for the weakness).

## Solo-buildability score (0–10)

### What it measures

How realistically the user can ship an MVP given current skills, time, and capital. The score answers: *can the user realistically ship an MVP themselves, and if not, how far from solo is it?*

This score is independent of the commercial score. A high commercial idea with low solo-buildability isn't killed — it's flagged as requiring partnership. A low commercial idea with high solo-buildability is still killed. The matrix (see below) governs how the two scores combine into a decision.

The "MVP" being scored is the version that can credibly test the value proposition, not a polished launchable product. Discovery is about confirming the bet, not delivering it.

This score is assigned in framework section 06.

### Anchor descriptions

Build times below are relative to **`user-profile.md`'s build-speed baseline** — read the baseline build window and the learning tiers from there.

- **9–10:** Trivially solo-buildable. Ships solo **within the baseline build window**, using skills the user already has or can learn within it. No partnerships, licensing, or external capital needed for MVP.
- **7–8:** Solo-buildable with effort. Ships solo in the **new-but-accessible-learning tier** (per the profile) — learning new but accessible skills (frontend frameworks the user hasn't used, basic backend, integrations with public APIs). No partnerships required, but may benefit from one.
- **5–6:** Solo-buildable with significant learning or specific tools. Ships solo in the **significant-learning tier** (per the profile), OR within roughly the baseline window if the user brings in one specific collaborator for a defined component.
- **3–4:** Needs partnership for one critical component. Requires a meaningful partnership (technical co-founder, domain expert, data partner) to ship a credible MVP within a realistic action window. A solo path exists but is impractical given the user's skills and the time required.
- **0–2:** Requires team, capital, or licensing the user does not have. No realistic solo or single-partnership path to MVP.

*Worked examples:* **9/H** — a self-serve web app over a Supabase backend with public-API integrations, squarely in the profile's documented frontend + simple-database capability; ships within the baseline window. **3/M** — the core is a real-time, high-reliability matching engine at scale, needing a backend specialist the profile lacks; a solo path exists but is impractical (adjacent-capability reasoning, not a documented match).

### Why this isn't a kill criterion

The 2×2 matrix (see "The 2×2 matrix" below) treats solo-buildability as a strategy signal, not a go/no-go filter. Specifically:

- A high-commercial / low-solo-build idea triggers the "approach partners with a clear view" path. Worth pursuing with a partnership strategy, not killed.
- A low-commercial / high-solo-build idea is killed by default — easy to build does not rescue an idea that can't make money. The user may exercise the optional learning-project override if the brief indicates a relevant learning interest (see the matrix section for details).
- A low-commercial / low-solo-build idea is killed for the commercial reason. Solo-build is irrelevant to that kill.
In all cases, the kill decision is driven by commercial score, not solo-build. Solo-build only changes *how* a viable idea gets pursued.

One edge case worth flagging: a 0–2 solo-buildability score combined with low commercial conviction (L on enough commercial signals that the overall commercial score is itself uncertain) is worth surfacing to the user before completing the analysis. The question is: *is this idea worth the research investment to upgrade commercial conviction, given that even strong commercial evidence would still leave the user dependent on partners or capital to act on it?* The user may choose to proceed (they have access to partners and want to validate the idea anyway), to deprioritize (move to other ideas while this stays as a future candidate), or to kill outright. Claude does not make this call alone.

## Agent-fit (qualitative)

### What this captures

Whether the idea is agent-shaped, or whether a different form factor (web app, mobile app, browser extension, plain database tool) fits the problem better. The output is a short qualitative note, not a number.

**This is not a viability filter.** Some ideas are simply not agentic, and that's fine — the rubric is not trying to force an agent shape onto problems that don't need one. A great non-agentic idea is still a great idea. Agent-fit does not determine whether the user takes on the idea; the commercial score and the 2×2 matrix do that.

### Default verdict and purpose

Agent-fit defaults toward *not agent-shaped* and requires evidence to move off it. When the user has described an idea as "an agent" or "agentic," that framing is a hypothesis to challenge, not a starting assumption — the failure mode this guards against is rationalizing an agent shape onto a problem better served by a simpler form factor.

The operational method for the evaluation — the five evaluation lenses with their anti-examples, the verdict heuristic, and how default skepticism is applied in each mode — lives in template 03, where the evaluation is performed. This section defines the output format, the wrapper-test downgrade rule, and how the verdict is used.

Agent-fit exists for two reasons only:
1. To document the *honest* form-factor recommendation for an idea, so the user has clarity on what they'd actually be building if they proceeded.
2. To provide portfolio-level pattern visibility across multiple evaluations (see "How agent-fit is used" below).

This score is assigned in framework section 03.

### Format

Agent-fit is captured as a short note with three parts:

1. **Verdict:** one of *strong agent fit*, *partial agent fit*, or *not agent-shaped*.
2. **Reasoning:** one sentence explaining the verdict, grounded in the specific characteristics of the idea (not generic agent vs. non-agent talking points).
3. **Recommended form factor:** the actual shape the user would build if they proceeded — agent, web app, mobile app, browser extension, internal tool, hybrid, etc.

Example formats:

> **Verdict:** Strong agent fit.
> **Reasoning:** The discovery moment (what should I watch tonight, given mood, time, traffic, partner preferences) genuinely benefits from dialogue and multi-source synthesis that a filter UI can't replicate.
> **Recommended form factor:** Agent for discovery, with a web fallback for direct-intent users who already know what they want.

> **Verdict:** Not agent-shaped.
> **Reasoning:** The core workflow is invoice-to-budget matching, which is deterministic data processing — users want speed and accuracy, not conversation.
> **Recommended form factor:** Web app with strong data ingestion and rules engine. LLM useful for edge cases (ambiguous invoices), not as the primary interface.

> **Verdict:** Partial agent fit.
> **Reasoning:** The core task (expense categorization) is deterministic, but the surrounding workflow (budget guidance, anomaly investigation) benefits from dialogue.
> **Recommended form factor:** Web app with embedded agent assistance for the dialogue-shaped subtasks. Pure agent would be over-engineered.

### The wrapper-test downgrade rule

In framework section 03, after assigning an initial agent-fit verdict, Claude runs the wrapper test (the question and its mechanics are defined in template 03, Task 3): *what does this purpose-built product do that a general-purpose LLM (Claude, ChatGPT, Gemini) couldn't do for the user directly?*

The wrapper test result interacts with agent-fit as follows:

- If the wrapper test *passes* (the product offers something a general-purpose LLM cannot): the agent-fit verdict stands.
- If the wrapper test *fails* (a general-purpose LLM can do this adequately for the user): the agent-fit verdict is downgraded by one level — *strong* becomes *partial*, *partial* becomes *not agent-shaped*. A failed wrapper test on a *not agent-shaped* idea is consistent and requires no change.

The wrapper test also feeds the Defensibility dimension of the commercial score (low defensibility for thin wrappers) and section 04's capability-feasibility check, but the agent-fit interaction above is independent — it's about honest form-factor recommendation, not commercial viability.

### How agent-fit is used

Agent-fit is a descriptive output, not a decision input. It produces information the user reads alongside the matrix-driven decision, but it does not change matrix positions, override kill recommendations, or function as a tiebreaker between ideas.

It has two specific uses:

**Use 1: Honest form-factor recommendation, for execution planning.**

After the matrix produces a proceed decision, the user needs to know what they would actually be building. Agent-fit answers that question honestly. If the user framed an idea as "an agent" but the honest verdict is "not agent-shaped" with a recommended form factor of "web app," that recommendation is what feeds execution planning. The matrix says whether to pursue; agent-fit says what to pursue *as*.

This use applies only after the matrix has produced a proceed recommendation. For killed ideas, agent-fit is documented in the analysis but has no further role.

**Use 2: Portfolio-level pattern visibility.**

Across multiple evaluations, the distribution of agent-fit verdicts is itself informative. If most ideas come up "not agent-shaped," that is a signal about the kind of opportunities being generated and what skills the user would build if they pursued them. This information lives in the cross-idea calibration step (see `SKILL.md`) and may inform what kinds of ideas the user generates next.

This use applies across the portfolio, not within a single evaluation.

### What agent-fit is not used for

To be explicit:

- Agent-fit does not move ideas between matrix quadrants.
- Agent-fit does not override a kill recommendation.
- Agent-fit does not act as a tiebreaker between ideas in the same quadrant. If multiple ideas land in the same matrix position, the user weighs them using whatever criteria they choose — strategic fit, market interest, partnership availability, personal energy — but agent-fit is not given a privileged role among those criteria.
- Agent-fit does not reward an idea for being "more agentic" or penalize it for being "less agentic" relative to its competitors in the portfolio.

The verdict is honest description of what the user would build if they proceeded. That is its entire job.

## Conviction and scoring

### Purpose of this section

The standing habit from `SKILL.md` is to apply H/M/L conviction labels to every judgment call, score, and quantitative estimate throughout the analysis. This section defines how conviction labels are used *during scoring* — specifically, how they affect comparison between scores, how they inform decisions, and what rules prevent them from being misused.

### Conviction definitions (reference)

Restating from `SKILL.md` for ease of reference:

- **High (H):** backed by external evidence — interviews, primary data, market research, observed behavior, transactions you can point to.
- **Medium (M):** backed by analogous evidence — similar products' performance, indirect signals, reasoning from comparable markets, structured assumptions from credible sources.
- **Low (L):** your own reasoning, no external validation yet. The judgment may be sound, but it has not been tested against the world.

Conviction is a label on *evidence quality*, not on the user's confidence or Claude's confidence. A judgment can feel highly confident and still be Low conviction if no external evidence supports it.

### The no-distortion rule

A score must reflect the user's honest reading of the dimension anchor, regardless of how much evidence backs it. Distorting a score because conviction is Low — in either direction — is a misuse of the rubric.

The score answers: *where does the evidence I have point?*
The conviction label answers: *how good is that evidence?*

These are independent. The score should not be inflated because evidence is thin (to make the analysis feel more decisive), and it should not be deflated either (out of false humility about thin evidence). Both distortions corrupt the rubric; the conviction label is the dedicated mechanism for representing evidence quality, and using it as designed keeps the score honest.

The correct pattern when evidence is thin:
- Assign the score that best matches the dimension anchor based on what's known.
- Label conviction L.
- Note what evidence would be needed to upgrade conviction.

The incorrect patterns:
- Scoring higher than the evidence supports, on the grounds that it "feels right" or "the upside is large."
- Scoring lower than the anchor supports, out of false humility about evidence quality.
- Skipping the conviction label or defaulting everything to M.
- Treating low conviction as a reason to defer scoring entirely.

Low conviction is not a failure of the analysis. It is an honest signal of where research investment would produce the largest improvement in decision quality.

### How conviction modifies comparison between scores

Within a single idea, the dimension scores combine into the overall commercial score by averaging (the score layer is conviction-invariant — see "Score layer vs decision layer" below). Conviction does not change a dimension's value — a 2/H is a veto the same way a 2/L is, though a low-conviction veto routes through the validation layer before the kill stands.

Where conviction matters is in *comparison between ideas*. The decision principle:

> When conviction differs significantly between two ideas being compared, the comparison is not yet a decision — it is a research prompt. The default action is to upgrade conviction on the weaker-evidenced side before committing. The fallback action, when research is not possible within the user's time or budget, is to prefer the higher-conviction score, because committing on weak evidence is riskier than committing on strong evidence at a slightly lower score.

Worked examples (all following the same principle, varied by how dramatic the gap is):

- **Idea A: commercial 7/H vs. Idea B: commercial 7/L.** Same score, different evidence base. Default action: do not choose yet — run the cheapest test that could move Idea B from 7/L to 7/M or 7/H. Fallback (if no research possible): prefer Idea A.

- **Idea A: commercial 6/H vs. Idea B: commercial 7/L.** A common case. The 6/H is real; the 7/L is a hope. Default action: upgrade conviction on Idea B — the score gap is small enough that the comparison genuinely depends on whether the 7 holds up. Fallback (if no research possible): prefer Idea A, since the 6/H is decision-grade and the 7/L is not.

- **Idea A: commercial 8/L vs. Idea B: commercial 6/H.** Score gap is large enough to matter, but conviction is reversed. Default action: do the smallest possible test that could upgrade Idea A's 8/L to 8/M — if it survives the test, Idea A becomes the clear winner; if it doesn't, Idea A's score drops and Idea B wins by default. Fallback (if no research possible): prefer Idea B, because acting on an 8/L is a speculative bet, while acting on a 6/H is a documented one.

The pattern across all three: conviction differences are not tiebreakers, they are signals that the comparison is incomplete. The work of completing it is research.

### Using conviction to prioritize research

Conviction labels turn the rubric into a research agenda, not just a scorecard.

After scoring an idea, scan for the Low-conviction labels on dimensions that materially affect the decision. Each one is a candidate research investment. The order of priority:

1. **Low-conviction scores on high-impact dimensions.** If monetization clarity is 7/L, validating that score (or revising it downward) changes the commercial picture more than refining a 9/H on something else.
2. **Low-conviction scores near a boundary.** A 3/L on a dimension where moving to 2 triggers a veto, or a dimension sitting right at the 2/3 line, is high-priority research — the boundary is decision-relevant.
3. **Low-conviction scores on dimensions with cheap validation paths.** A market size estimate that could be sharpened by a single afternoon of bottom-up estimation is a faster upgrade than a defensibility judgment that requires interviewing competitors' customers.

When surfacing the analysis to the user, Claude explicitly lists the highest-priority Low-conviction items as suggested research, ordered by the rules above. This converts conviction labels into actionable next steps rather than leaving them as static metadata.

### Score layer vs decision layer

Conviction operates on two layers, and keeping them separate resolves an apparent contradiction:

- **Score layer — conviction-invariant.** A dimension's value doesn't move with conviction (a 2 is a 2 at H or L); the overall commercial conviction is the *lowest of the four* dimensions. The no-distortion rule lives here.
- **Decision layer — conviction-sensitive.** Matrix placement uses conviction at the threshold (6/L → low), and the validation layer and kill-confirmation rules below gate decisions that rest on thin, load-bearing evidence.

So "a 2/L vetoes like a 2/H" (score layer) and "low-conviction decisions get validated" (decision layer) are one coherent system, not a contradiction.

### The validation layer

At any decision (proceed *or* kill), identify the **decision-critical** low-conviction claims — the load-bearing ones that would flip the decision if wrong (ranked by the "Using conviction to prioritize research" rules above). The decision is not final until each is **validated** (research) or **explicitly accepted** as a recorded risk ("proceeding / killing on thin evidence on X, eyes open").

This is symmetric — it applies to proceeds and kills alike. It gates only the load-bearing low-conviction items, not every L-label, so it adds discipline, not weight.

### Kill confirmation (conviction-gated)

The framework is autonomy-first. In **autonomous mode**, a kill **auto-confirms** unless the validation layer fires on it: if a decision-critical claim driving the kill is Low conviction, the kill **escalates to the human** (validate-or-accept) before it stands; High/Medium-conviction kills proceed without a pause. In **checkpoint mode**, all kills pause (that is the mode's purpose). A kill escalates exactly when it rests on thin, decision-critical evidence — there is no separate gate.

(The section-09 high-commercial / weak-financial contradiction remains a mandatory escalation even in autonomous mode — it is a genuine ambiguity, not a kill.)

## The 2×2 matrix

### Purpose

The matrix is the decision tool for section 09. It takes the two numeric scores produced by the rubric — commercial and solo-buildability — and maps them to one of four strategic outcomes. The matrix is what turns "two numbers" into "what should the user actually do with this idea." Vetoes are resolved *before* the matrix (see "The kill model"), so the matrix only places ideas that survived every dealbreaker; a low-commercial placement here is a **matrix kill** — death by mediocrity, not by a single fatal flaw.

### Axes

**Horizontal axis: Commercial score (0–10).** The primary axis. Higher = more likely to make money.

**Vertical axis: Solo-buildability score (0–10).** The secondary axis. Higher = more realistically shippable by the user alone within the action window.

The split between "high" and "low" on each axis is at 6/10. A score of 6 or above is high; 5 or below is low.

The reasoning for the threshold:

- The dimension anchors define 7+ as the "strong" band (clear evidence, worth pursuing) and 5 or below as the "weak or insufficient" band (mixed evidence, not yet supported).
- A score of 6 is the borderline case between the two bands.
- The matrix includes 6 on the "high" side because being more restrictive than the anchors would mean killing ideas the anchors themselves describe as plausible.
- 5 is on the "low" side because the anchors describe it as "plausible but uncertain" — uncertainty has not yet been resolved, so the idea is not ready to act on.

Conviction at the threshold:

A score of 6 with Low conviction is treated as below the threshold (≤5) on its axis. Specifically:

- A 6/L on commercial is treated as below the horizontal threshold (low commercial) until conviction is upgraded.
- A 6/L on solo-buildability is treated as below the vertical threshold (low solo-buildability) until conviction is upgraded.
- These rules apply independently per axis. An idea with commercial 6/L and solo-buildability 6/L is treated as low/low on both axes until conviction is upgraded on either.
- The reason: a 6/L is "I think this just clears the bar, but I have no evidence." Treating that as "high" would be inflation through the matrix what the no-distortion rule prevents in scoring.

A second placement demotion comes from scoring: if **two or more commercial dimensions scored 3–4**, the idea is placed as low-commercial regardless of the average (the "weak on multiple fronts" demotion). Both demotions affect *placement*, not the underlying scores, and both are mechanical — they hold in autonomous mode.

### Quadrant interpretations

**High commercial (≥6) / High solo-buildability (≥6) — "Pursue immediately"**

The straightforward case. The idea can make money, and the user can build it themselves within a realistic window.

- Action: proceed to execution planning.
- Next steps after discovery: KPI definition, MVP scope, launch roadmap. These live outside the discovery skill; the discovery deliverable is the kill/proceed decision plus the inputs that would feed those next steps.
- This is the only quadrant where the user can act on the idea without additional structural requirements (partnership, learning-project reframing). Kills also produce a clean recommendation, but a negative one. Pursue-with-partnership is structurally conditional. Pursue-immediately is unconditional.
- "Immediately" means immediately *relative to the other quadrants*. The user may still choose to deprioritize for personal reasons (currently committed to another build, waiting on a dependency, etc.). The matrix says the idea is ready; sequencing is the user's call.

**High commercial (≥6) / Low solo-buildability (≤5) — "Pursue with partnership strategy"**

The idea can make money, but the user cannot realistically ship it alone within the action window. This is not a kill — it is a different shape of pursuit.

- Action: proceed, but with the explicit recognition that execution requires a partner, capital, or some external resource the user does not currently have.
- Next steps after discovery: the user defines what the partnership shape needs to be (technical co-founder, domain expert, data partner, capital partner, etc.), and approaches potential partners with the discovery analysis as the basis for the conversation. The user's framing for this: "approach potential partners with a clear view."
- Risk to flag in section 09: partnership-dependent ideas have longer time-to-launch and depend on finding the right partner. The discovery analysis should note the realistic timeline for assembling that partnership, and what happens if no partner materializes within a defined window.

**Low commercial (≤5) / High solo-buildability (≥6) — "Kill, with optional learning-project override"**

The idea is easy to build but unlikely to make money. The matrix default is kill — easy to build does not rescue an idea that cannot generate revenue.

The user may exercise one optional override before the kill is finalized: **pursue as learning project.** This option is surfaced only when the brief indicates a relevant learning interest in the technology area (frontend, AI agents, full-stack, etc.). When exercised, the user explicitly chooses to pursue the idea with no expectation of revenue. The framework's output in this case is *not* a green light for commercial pursuit — it is explicit acknowledgment that the user is investing time in skill-building, with no expectation of return. The discovery analysis should note this distinction so the user does not later confuse the two.

If the override is not exercised (or not available because the brief indicates no relevant learning interest), the kill stands. The decision document may note related ideas worth evaluating as separate next briefs where the analysis supports such adjacencies, but these are portfolio notes for the user's consideration, not a framework path.

The learning-project override applies to low-commercial / high-buildability kills (matrix kills and commercial-veto kills) — the idea is buildable, just not monetizable. It does **not** apply to the low-commercial / low-buildability quadrant (the idea isn't buildable, so skill-building isn't meaningful) or to **structural-veto kills** (legal / data / capability blocked — the idea can't be built or operated). The override follows *buildability*.

**Low commercial (≤5) / Low solo-buildability (≤5) — "Kill"**

The idea cannot make money and cannot be built by the user. No quadrant interpretation, no exception, no surfaced option. Kill.

- The kill is driven by the commercial score, not the solo-buildability score. Solo-buildability is irrelevant to this kill — the idea would be killed for the commercial reason even if it were trivially buildable. This is consistent with the rubric's principle that solo-buildability is never a kill criterion.
- The discovery analysis still produces a 09-decision.md documenting the kill, the rationale, and the challenge pass output applied to the kill itself (per `SKILL.md`).

### Visual reference

For section 09 output, the matrix is described in prose with the idea's position explicitly stated, and **a simple 2×2 visual (markdown or ASCII, with the idea's position marked) is encouraged** alongside the prose — see template 09. A literal visual is not strictly required, but the position must be unambiguous either way. Example phrasings:

> "This idea is in the 'Pursue with partnership strategy' quadrant: commercial score 7/M, solo-buildability score 3/H. The score gap on solo-buildability is the determining factor — the user can realistically ship adjacent ideas alone, but this one needs a data partnership before any MVP is credible."

> "This idea is in the 'Kill' quadrant: commercial score 4/H, solo-buildability score 8/H. Easy to build, but the commercial case is weak with strong evidence behind that weakness. Recommend kill."

The position statement is mandatory in section 09. The reasoning that connects the scores to the quadrant is mandatory. Implicit positioning ("it's somewhere between pursue and kill") is not acceptable — every idea lands in exactly one of the four quadrants.

## The kill model

This is the consolidated reference for every point at which the framework can stop and recommend a kill. There are two kinds of stop: **vetoes** (dealbreakers) and the **matrix kill** (death by mediocrity).

### Vetoes

A **veto** is a dealbreaker — a condition that kills the idea regardless of how strong everything else is. A veto **fires at the section where its condition is definitively assessable**, and it is a *conclusion from research*, never a substitute for it: a veto fires only on adequately-researched findings, and a low-conviction veto routes through the validation layer (verify before the kill stands).

Two families:

**Commercial vetoes** — a commercial dimension scored **0–2** (fatal):
- **Problem severity 0–2** (no real / severe problem) — fires at section 01 (early-exit).
- **Market size 0–2** (no market clears the make-money threshold) — fires at section 02 (early-exit).
- **Monetization clarity 0–2** (no viable revenue model) — fires at section 05 (the Business-model gate).
- **Defensibility 0–2** — *not* definitive until section 09, because moats can emerge in 04 (regulatory) and 05 (data / network / business-model). Scored provisionally at 03; **finalized at 09**; vetoes there if still fatal (a *late* veto, not an early-exit).

**Structural vetoes** — a structural blocker, all assessed in section 04 (the Structural gate):
- **Legal / regulatory blocked.**
- **Data access blocked.**
- **Capability infeasible** (current tech can't do this well).

### The gates (named by function)

A "gate" is a section where a veto can fire. The gates, named by what they test (not numbered): **Problem gate** (01) and **Market gate** (02) — the early-exits — plus the **Structural gate** (04), the **Business-model gate** (05), the **GTM gate** (07), the **Defensibility late veto**, and the **matrix decision** at section 09.

Each gate's **firing conditions are defined in `SKILL.md`'s "The kill model"** — the single canonical source. This rubric supplies the *measurement and routing*: what a veto is (the two families above), how each veto routes (below), and the matrix kill.

### Veto routing — kill is the default, route by type

Every veto defaults to **recommend the kill**; before finalizing, it surfaces the one recovery direction appropriate to its type. Bedrock rule: **a partner can never rescue a commercial death** (a genuine lack of demand or revenue can't be partnered).

- **Commercial vetoes** → clean kill, or *pivot-suggested* (a re-brief with a different segment / market / wedge / model). Never "needs a partner."
- **Structural vetoes** → route uniformly: **partner** if a partner can supply the missing piece (licensed partner for legal, data partner for data, specialized-capability partner for capability) *and* commercial is strong; **kill** if it's unavailable to anyone; **park** (capability only) if the tech isn't there yet but is improving. Routing at section 04 uses a partial commercial picture (Monetization not yet scored, Defensibility still provisional), so a partnership route surfaced there is *conditional on the commercial case holding up*.

Pivots are re-briefs, not continuations — a different segment / market is a different idea, evaluated fresh.

### The matrix kill

An idea that survives **every** veto reaches the matrix. If its commercial **average is < 6** (mediocre across the board, no single fatal flaw), it is a **matrix kill** — driven by the commercial score, not solo-buildability. The two placement demotions (conviction-at-threshold 6/L→low; "weak on multiple fronts") can also push a borderline idea into the low-commercial band. The learning-project override applies here in the high-buildability case (see the matrix section).

### Kill confirmation, challenge pass, and documentation

Every kill — veto or matrix — includes the **challenge pass applied to the kill itself** (per `SKILL.md`), and is **confirmed per the conviction-gated rule** ("Kill confirmation" in the Conviction section: auto-confirmed at High/Medium conviction in autonomous mode, escalated to the human if low-conviction; always paused in checkpoint mode). Once confirmed, `09-decision.md` is written and the framework stops; the decision file notes which sections were skipped.

Process-gate findings (the structural blocks, the GTM economics test) are analytical, not scored — where the underlying finding is uncertain (contested legal interpretation, assumption-dependent economics), the uncertainty is documented in the kill rationale and the user can choose to research before confirming.

### What is not a kill criterion

To be explicit:

- **Solo-buildability is never a kill criterion.** Low solo-buildability moves an idea to "pursue with partnership strategy," not to kill. The only path by which it contributes to a kill is the low-commercial / low-buildability quadrant, and there the kill is driven by commercial.
- **Agent-fit is never a kill criterion.** The verdict is descriptive only. "Not agent-shaped" changes the recommended form factor, not the decision.
- **Conviction is never a kill criterion on its own.** Low conviction is a signal for research, not a kill. An idea with strong scores at Low conviction is a research opportunity.
- **User preference is never an *automated* kill criterion.** The user may kill an idea for personal reasons; those are documented as user-driven kills in `09-decision.md`, distinct from framework-driven kills.

## Calibration note

### Purpose

The rubric is designed to be reused across many ideas. Over time, the consistency of scoring across evaluations matters as much as the accuracy of any single score — the user's portfolio-level decisions depend on a 7 today meaning the same thing as a 7 six months from now. This section captures the calibration concerns that develop *across* evaluations, not within any single one.

The cross-idea calibration mechanism itself lives in `SKILL.md` (the "compare against the 3 closest prior evaluations" rule applied at section 09). This section names the failure modes that mechanism is designed to catch.

### Score inflation

The most common failure mode in scoring systems used over time: the average score drifts upward as the user has accumulated investment in the framework itself. Each new idea looks better than the last because the user has become more optimistic about the process, more attached to the act of pursuing, or more reluctant to record a "weak" verdict on something they spent time analyzing.

The general principle being violated: scores should be anchored to the rubric's anchor descriptions, not to the user's current mood or the relative strength of the ideas being considered this month. A 7 in month one and a 7 in month twelve should describe ideas that are similarly strong against the absolute anchors, not similarly strong against each other.

The signal that inflation is occurring:
- Most recent evaluations cluster at 6–8 on commercial, while earlier evaluations spanned 3–9.
- The dimension anchors increasingly require generous interpretation to justify the assigned scores.
- Kill recommendations have become rare.

The correction: when the cross-idea calibration check in section 09 (per `SKILL.md`) runs, it identifies the 3 closest prior evaluations by domain or shape and asks directly — does this idea genuinely deserve a higher commercial score than [prior idea] given what was known then? If the answer relies on generous interpretation of the current idea or harsh interpretation of the prior, the current score is inflated. Surface the specific prior idea named in the comparison so the user can review the side-by-side.

The framework's purpose is to filter, not to validate. A portfolio in which most ideas score above 5 is a portfolio that has stopped filtering.

### Conviction drift

A related failure mode, specific to conviction labels: over time, the temptation is to default to M on everything — neither boldly High nor humbly Low. This is conviction drift, and it corrupts the rubric in a more subtle way than score inflation, because M can be assigned to anything without obvious red flags.

Medium is not a default. It is a specific claim: *analogous evidence exists*. That claim should be defensible.

The correction: when assigning M, briefly note what specifically makes it M rather than L or H. If the answer cannot be articulated — if there is no actual analogous evidence to point to, just a vague sense that the judgment is "more than a guess" — the honest label is L. M earned by default is the same problem as a 7 earned by default.