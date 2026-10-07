# Template: 07 — Form factor and differentiation

## Purpose of this section in the framework

Section 07 judges **how well the idea's form factor fits** and **why anyone would choose this idea**, for one selected idea, in its folder. The form factor comes from 05's handoff; 07 judges it and does not replace it.

This section produces:
- The **agent-fit verdict** (strong / partial / not agent-shaped): qualitative and descriptive only, per `rubric.md`
- The **wrapper test** result: what this product does that a general-purpose LLM cannot
- The **differentiation hypothesis**: the one-sentence sharpest reason a user would choose this over the closest alternative
- A judgement of how well the handoff's form factor fits the problem and the market
- A **provisional** score on the **Defensibility** dimension (finalized in 13, once 08's and 09's moats are known)

Section 07 **cannot kill.** Defensibility is not an early exit: moats can still emerge in 08 (regulatory) or 09 (data, network, business model). The Defensibility veto is a *late* veto, applied in 13 only if the finalized score is still 0–2.

**No alternative form factors.** Form factors are explored in 04 and chosen in 05, which compares variants of the same idea head to head. 07 does not generate or recommend a different form factor (`SKILL.md`, "No alternatives after the screen"). If the handoff's form factor fits poorly, that is a finding against this idea, and the ideas in 04 with other form factors already exist.

The agent-fit verdict never changes a verdict, overrides kills or breaks ties (per `rubric.md`). It records honestly what would be built, and gives visibility across the portfolio.

## Inputs

- **05's handoff:** the idea, who it serves, what is sold, the form factor, the market and the threshold.
- **06:** the incumbents, white space and choice dimensions.
- **04:** the idea's card, including whether it answers the founder's form-factor lead.
- **`user-profile.md`:** any owned distribution the founder already has (an audience or channel), for Defensibility.

## Research activated in this section

**Ordinary web search, discretionary.** Use it to:
- establish what general-purpose LLMs (Claude, ChatGPT, Gemini) currently do in this task area, for the wrapper test. Prefer sources from the past six months; these capabilities change fast;
- find precedents for the form factor in the idea's market (e.g., "successful WhatsApp-based services in Colombia").

Deep research is rarely warranted here. The exception is a highly novel form factor with no clear precedent; follow the pause in `SKILL.md`, "Research and deep research".

**Fact discipline.** The wrapper test and Defensibility rest on fast-moving, checkable facts: what a named platform or LLM shipped, and when. Cite each at the point of use with its conviction and add it to the claims-to-verify list. "The platform already does this" and "no one does this yet" are exactly the confident claims most likely to be wrong. Verify them before they drive the Defensibility score.

## Analytical work for this section

### Agent-fit evaluation lenses

These lenses are the method for Task 1. Examine the idea through each one independently; they are angles, not a checklist to count. Then judge holistically.
- **Dialogue and clarification:** the user's intent is fuzzy, exploratory or needs negotiation. *(Anti-example: the user always knows exactly what they want and would rather filter or click than describe.)*
- **Multi-source synthesis:** the answer combines data from sources with no unified interface. *(Anti-example: all the data lives in one structured database and the user needs a good query interface.)*
- **Persistent context about the user:** preferences, history or constraints accumulate and change recommendations. *(Anti-example: the task is one-shot and past interactions don't change the right answer.)*
- **Tool use and orchestration:** multiple discrete steps sequenced on intermediate results. *(Anti-example: a linear, deterministic workflow with no branching.)*
- **Reasoning under ambiguity:** the right answer depends on trade-offs the user can't fully specify upfront. *(Anti-example: there is a correct answer, and the user just needs it found efficiently.)*

**Verdict heuristic:**
- **Strong agent fit:** several lenses apply strongly, and none clearly argues against agent shape.
- **Partial agent fit:** one or two lenses apply, but the idea has substantial non-agent parts, or one lens argues against agent shape.
- **Not agent-shaped:** no lens applies strongly, or the anti-examples describe the idea better than the positive descriptions.

**Default skepticism.** When torn between two verdicts, choose the less agent-leaning one. This holds however the idea is framed, however interesting an agent version would be, and whatever competitors call themselves.

### Task 1: Evaluate agent-fit

Apply the lenses to the idea as handed over:
- **If the form factor is an agent:** treat it as a hypothesis to test, with default skepticism.
- **If the form factor is not an agent:** check whether the lenses strongly suggest an agent-shaped opportunity was missed. If they do, record it as a finding (it does not change the form factor).

Output: the verdict, with one sentence of reasoning grounded in this idea's specific characteristics.

### Task 2: Run the wrapper test

The question: **what does this purpose-built product do that a general-purpose LLM couldn't do for the user directly?** It is not a yes/no. It is an honest account of what general LLMs already do here, and whether this product offers something meaningfully beyond it.

Purpose-built products typically beat general LLMs on:
- **Proprietary data access:** data the general LLM cannot reach (real-time inventory, the user's own transactions, gated APIs).
- **Transactional capability:** completing actions the LLM cannot (booking, payments, submitting forms with verified identity).
- **Persistent context about the specific user** that changes recommendations over time.
- **Integration with deterministic workflows:** multi-step processes with state management.
- **Multi-tool orchestration with reliability guarantees:** specific tools in specific sequences, with error handling.

If none of these (or a comparable advantage) applies, the test **fails**: a general LLM does this adequately, and the product is a thin wrapper. If the result is ambiguous (the LLM does most but not all of it), say so and judge whether the gap matters in practice; a gap users wouldn't notice is closer to a fail.

**Downgrade rule** (`rubric.md`): a failed wrapper test downgrades the agent-fit verdict by one level (strong → partial, partial → not agent-shaped). A failed test on a "not agent-shaped" verdict needs no change.

The same five advantages are primary inputs to Defensibility. The wrapper test asks *whether* the product has them; Defensibility asks *how strong and durable* they are.

### Task 3: Write the differentiation hypothesis

Using 06's choice dimensions and white space, write **one sentence: the sharpest reason a user would choose this over the closest existing alternative.**

Work through **2–3 candidate hypotheses** and keep the one that best survives "what's the strongest argument against this?". These candidates sharpen this idea's edge; they are not alternative ideas.

- **Sharp** (structural examples): "Users would choose this because it surfaces real-time supplier inventory at checkout, eliminating the 'out of stock after I order' problem behind 30% of cancellations in this category."
- **Weak** (avoid): "better user experience"; "AI-powered" (technology, not a reason to choose); "more features"; "local market focus" (a strategy, not a reason to choose).

If it cannot be written in one sentence, that is a finding. Write the best available sentence and say that it needed generous interpretation.

### Task 4: Judge the form factor's fit

Judge how well the handoff's form factor serves this problem, these users and this market. If 05 compared form-factor variants of this idea, start from that comparison and deepen it rather than repeating it.
- **What it assumes** about how users discover, adopt and use it (e.g., a mobile app assumes app-store habits; a browser extension assumes desktop use).
- **Which parts of the problem** it serves well and which it serves poorly.
- **Local lens:**
  - Is the market mobile-first, which handicaps web apps?
  - Do messaging platforms dominate, favouring WhatsApp or chat-based services?
  - Does it rely on infrastructure assumptions (app-store penetration, card payments, broadband)?

Output: a fit judgement (good / adequate / poor) with one paragraph of reasoning. A poor fit is recorded as a finding against this idea. It is not fixed here.

## Scoring activated in this section

### Defensibility dimension (provisional)

Score Defensibility on the 0–10 scale in `rubric.md`, with an H/M/L conviction label. **The score is provisional**: 13 finalizes it once 08 (regulatory moats) and 09 (data, network and business-model moats) are known. Score what is visible now. Do not guess at later moats, but flag any you expect 08 or 09 to confirm so 13 can reconcile them.

Apply the anchors from `rubric.md`, the **canonical source** (synced copy; the worked examples and both scoring rules live there):
- **High (8–10): structural moats:** proprietary or compounding data, transactional capability, network effects, regulatory licences, deep switching costs, or persistent personalization that competitors can't easily replicate.
- **Medium (5–7):** defensibility without a structural moat. **Execution-tier moats**, durable at the idea's threshold scale: owned distribution (an audience or channel the founder controls), a taste, design or brand edge, focus and shipping cadence, a price or cost structure incumbents won't match, or a niche unattractive for incumbents to contest. A determined incumbent could match it within 12–18 months, but plausibly won't bother. **Cap: without at least one structural moat, Defensibility does not exceed 6.**
- **Low (0–4):** no meaningful moat. A general-purpose AI tool or larger competitor could absorb this as a feature in weeks, *and* nothing (distribution, focus, niche economics) makes them unlikely to.

**Two scoring rules** (canonical in `rubric.md`):
- **Score moat potential.** Every moat of an unbuilt product is prospective, so "prospective / not yet observed" is never by itself a reason to discount.
- **Durability is scaled to the idea's threshold from 05.** At a niche threshold, "sticky for its users and ignorable by incumbents" is creditable Medium-band defensibility, not a venture-grade standard.

**With a failed wrapper test,** defensibility cannot come from the product's intelligence alone. Other structural and execution-tier moats still count; if there are none, the score is Low.

**Owned distribution** visible now (in `user-profile.md` or the research: a newsletter, a following, an installed base) is credited here. It is not booked only as a go-to-market advantage in 11.

A provisional 0–2 does **not** trigger an exit here; it carries to 13.

### Agent-fit verdict (qualitative, not numeric)

Record it in `rubric.md`'s format:
1. **Verdict:** strong agent fit / partial agent fit / not agent-shaped (after any wrapper-test downgrade).
2. **Reasoning:** one sentence grounded in this idea, noting any downgrade.
3. **Form factor and fit:** the handoff's form factor, with Task 4's fit judgement.

## Section-specific content for the four required parts

The four required parts are mandatory per `SKILL.md`.

### Analysis

Labelled subsections, in order: Agent-fit evaluation; Wrapper test; Differentiation hypothesis; Form-factor fit (including the local lens). Then the provisional Defensibility score with its conviction label, a **Moat candidates** line (each candidate as structural or execution-tier, and whether 08 or 09 must confirm it), the agent-fit verdict, and the section's claims-to-verify list.

### Recommendation

Always **"Proceed to 08."** Section 07 cannot kill.

### Rationale

Four to five sentences: the agent-fit verdict and any downgrade; the wrapper-test result; the differentiation hypothesis as written; the form-factor fit; and the provisional Defensibility score with its conviction and the inputs that drove it.

### Challenge pass

The judging form from `SKILL.md` (06–13 omit the "non-obvious option" question), plus the section-specific questions below. Each finding uses the fixed short format: what changed and why, or "no change".

## Challenge pass: section-specific questions

- **Agent-rationalization check:** did we rationalize an agent shape onto a problem a simpler form would serve better? Look for lenses applied loosely, "could be an agent" treated as "should be", a thin wrapper test, or lenses double-counting the same trait.
- **Wrapper-test rigor:** did we name specific capabilities general LLMs have today, from recent sources, and show concretely where this product goes beyond them? "General LLMs can't do this" without specifics is a skipped test, not a passed one.
- **Differentiation sharpness:** is the hypothesis specific enough to be proven wrong? Does it name what is different and why a user would prefer it?
- **Fit honesty:** was the form factor judged on its merits, or accepted because it came from 05 or from the founder's lead?
- **Moat realism:** is any moat credited because it sounds strong, rather than because the evidence supports its potential at this threshold's scale? (A prospective moat is fine; an unsupported one is not.)

## Word cap

**Hard maximum (provisional): 1,000 words, excluding citation markers and the source list.**

## Downstream dependencies

What later sections consume from section 07:
- **08** uses the form factor for its regulatory analysis, including any rules specific to this form factor (an agent and a web app can face different rules), and the wrapper test's capability findings for its capability-feasibility check.
- **09** uses the form factor when evaluating the revenue model (subscription tolerance, transaction friction, app-store fees).
- **10** scopes the build of this form factor.
- **11** uses the form factor to judge channels (app stores, search, messaging platforms).
- **13** finalizes the provisional Defensibility score, reconciling 08's and 09's moats, applies the late veto if it is still 0–2, and reports the agent-fit verdict and form-factor fit.
