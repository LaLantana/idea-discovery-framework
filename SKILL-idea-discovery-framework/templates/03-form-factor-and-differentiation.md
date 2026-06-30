# Template: 03 — Form factor and differentiation

## Purpose of this section in the framework

This section produces the form-factor recommendation that feeds execution planning, evaluates whether the idea is genuinely agent-shaped, runs the wrapper test against general-purpose LLMs, generates the differentiation hypothesis, and scores the Defensibility dimension of the commercial score.

This section produces:
- A form-factor recommendation (agent, web app, mobile app, browser extension, hybrid, etc.) — the actual shape the user would build if the idea proceeds
- The agent-fit verdict (strong / partial / not agent-shaped), captured qualitatively per `rubric.md`
- The wrapper test result — what this purpose-built product does that a general-purpose LLM cannot
- The differentiation hypothesis — the one-sentence sharpest reason a user would choose this over the closest existing alternative
- A **provisional** score on the Defensibility dimension of the commercial score (finalized at section 09, once moats from sections 04–05 are known)
- A recommendation to proceed to section 04, or in edge cases, to surface concerns to the user

Section 03 does not produce a kill recommendation on its own — and Defensibility is deliberately **not** an early-exit veto. Unlike Problem severity (01) and Market size (02), a weak moat is **not definitive here**: defensibility can still emerge in section 04 (regulatory moats) or section 05 (data / network / business-model moats). So Defensibility is scored **provisionally** in this section and **finalized at section 09**, where the provisional score is reconciled against any moats surfaced downstream. The Defensibility veto is a *late* veto — it fires at 09 only if the finalized score is still 0–2. (See `rubric.md`, "The kill model.")

The agent-fit verdict is qualitative and descriptive only. It does not affect matrix positions, override kill recommendations, or function as a tiebreaker. Its role is to inform execution planning after a proceed decision and to provide portfolio-level visibility into the kinds of ideas being evaluated (per `rubric.md`'s Agent-fit section).

## Brief fields relevant to this section

Before starting the analytical work, draw on these fields from `00-brief.md`:

- **Solution hypothesis:** the most load-bearing field for this section. Either names a specific form factor (agent, web app, mobile app, etc.) or reads "evaluate form factor as part of analysis." Determines the mode this section runs in.
- **Why this form factor (if specified):** the user's reasoning for the form-factor specification. Useful context but not justification — the analysis evaluates the specification independently.
- **Learning value:** if the user has stated an interest in building agents specifically, this field is relevant when interpreting the agent-fit verdict and form-factor recommendation. A "not agent-shaped" verdict on an idea where the user explicitly stated learning interest in agents is worth surfacing as a finding.
- **Depth overrides (if any):** acknowledge at the top of the section output. Common overrides for this section: "go deeper on competitive form-factor analysis," "skip the wrapper test — I've already validated this isn't a wrapper," "focus on differentiation — the form factor is settled."

If any of these fields are missing or unclear, surface the gap to the user before starting analytical work.

## Research activated in this section

This section is mostly analytical, but research is warranted for the wrapper test and for identifying competitive form-factor patterns.

### Web search (discretionary)

Use web search when:
- The wrapper test requires understanding what general-purpose LLMs currently do well in the relevant task area (Claude, ChatGPT, Gemini capabilities are not static — recent capability releases may change the wrapper test result).
- Identifying form-factor patterns in adjacent products would help generate or evaluate candidate form factors (Task 2).
- Finding precedent for non-obvious form factors (e.g., "are there successful WhatsApp-based products in [target market]?").

### Deep research (user-confirmed)

Deep research is rarely warranted in this section. The possible exception: highly novel form factors with no clear precedent, where structured investigation across multiple comparables would help generate or evaluate candidates. When warranted, follow the deep-research escalation protocol in `SKILL.md`.

### Source quality

Conviction labeling follows the same categorization as the Identify evidence task in template 01: primary sources → H, secondary sources → M, tertiary or hypothesis-level sources → L. Cite sources directly. For wrapper test research specifically, prioritize sources from the past 6 months relative to today's date — general-purpose LLM capabilities evolve quickly.

## Analytical work for this section

These tasks together produce the **Analysis** portion of the section file. The Recommendation, Rationale, and Challenge pass are produced after the analytical work, drawing on it.

The analytical work runs in one of two modes based on the brief's solution hypothesis field.

### Mode selection

Read the brief's solution hypothesis field. Run one of the two modes below:

- **Mode A: User specified a form factor.** The brief named "agent," "web app," "mobile app," etc. The agent-fit evaluation in Task 1 challenges or checks the user's specification depending on what was specified.
- **Mode B: Form factor deferred to analysis.** The brief reads "evaluate form factor as part of analysis." Task 1 runs as a fresh evaluation with no form factor weighted in.

In both modes, the analysis must produce a verdict, a recommended form factor, and the wrapper test result.

Acknowledge the active mode at the top of the section output ("Running in Mode A: user specified agent — applying default skepticism per the form-factor handling protocol").

### Agent-fit evaluation lenses

These lenses are the operational method for Task 1. (They previously lived in `rubric.md`; the rubric now keeps only the verdict format, the wrapper-test downgrade rule, and the usage rules.) Evaluate the idea against each lens independently — they are not a checklist to count, but angles to examine. After working through them, judge holistically.

- **Dialogue and clarification.** The user's intent is fuzzy, exploratory, or needs negotiation. (Anti-example: the user always knows exactly what they want and would prefer to filter or click rather than describe.)
- **Multi-source synthesis.** The answer requires combining data from sources that don't have a unified interface. (Anti-example: all the data lives in one structured database and the user just needs a good query interface.)
- **Persistent context about the user.** Preferences, history, or constraints accumulate and meaningfully change recommendations. (Anti-example: the task is one-shot and prior interactions don't change what the right answer is.)
- **Tool use and orchestration.** The task involves multiple discrete steps that need to be sequenced based on intermediate results. (Anti-example: the workflow is linear and deterministic, with no branching based on intermediate output.)
- **Reasoning under ambiguity.** The right answer isn't predetermined; it depends on weighing trade-offs the user can't fully specify upfront. (Anti-example: there is a correct answer and the user just needs the system to find it efficiently.)

**Heuristic for the verdict:**
- *Strong agent fit:* multiple lenses apply strongly, with no lens clearly arguing against agent shape.
- *Partial agent fit:* one or two lenses apply, but the idea has substantial non-agent components or one lens clearly argues against agent shape.
- *Not agent-shaped:* no lens applies strongly, or the anti-examples describe the idea better than the positive descriptions.

When uncertain between two verdicts, choose the less agent-leaning one — this is default skepticism in action. That skepticism applies regardless of how the user framed the idea, how interesting an agent version would be, whether building an agent has learning value, or whether competitors are calling themselves "AI agents." The job is honest assessment, not enthusiasm matching.

### Task 1: Evaluate agent-fit

The framing of this task depends on the active mode:

- **Mode A with user-specified agent form factor:** apply default skepticism — actively challenge the agent assumption using the five evaluation lenses above. Treat the user's specification as a hypothesis to test, not a starting point. When uncertain between two verdicts, choose the less agent-leaning one (the default-skepticism principle described above).

- **Mode A with user-specified non-agent form factor (web app, mobile app, etc.):** apply the agent-fit lenses to check whether the user's specification missed an agent-shaped opportunity. The default assumption is that the user's specification is correct; the agent-fit evaluation produces an exception only if the lenses strongly suggest otherwise. The point of the check is not to argue the user into an agent — it's to surface the rare case where an agent shape is genuinely better for this problem and the user's specification missed it.

- **Mode B (deferred):** run the agent-fit evaluation fresh, with no specified form factor to weight against. Apply default skepticism — "not agent-shaped" is the presumed verdict until evidence accumulates for partial or strong fit.

All three sub-cases produce the same output: a verdict (strong agent fit / partial agent fit / not agent-shaped) with one-sentence reasoning grounded in the specific characteristics of the idea.

**A note on the asymmetric treatment:** the three sub-cases above apply different default skepticism. Agent specifications and Mode B evaluations face strong skepticism (the framework is explicitly designed to prevent agent-rationalization). Non-agent specifications face lighter skepticism (the failure mode in the opposite direction — missing a genuine agent opportunity — is rarer and lower-cost than over-applying agent shapes). This asymmetry is intentional. The check on non-agent specifications exists primarily to catch the rare case where the user clearly missed an agent opportunity, not to second-guess every non-agent specification.

### Task 2: Generate candidate form factors

Conditional on mode and Task 1 verdict:

- **Mode B (form factor deferred):** always run.
- **Mode A with agent specified, verdict downgrades to "partial" or "not agent-shaped" after Task 1:** run to identify non-agent alternatives.
- **Mode A with non-agent specified, verdict comes up "partial" or "strong agent fit" after Task 1:** run to identify whether an agent or hybrid form factor should be considered.
- **Mode A where user's specification and the agent-fit verdict align:** skip — the form factor space is set.

When running, generate 2–3 candidate form factors that could address the painpoint. Examples: web app, mobile app, browser extension, internal tool, agent, agent-plus-web-fallback hybrid, WhatsApp-based service, voice interface, embedded widget in existing platforms.

For each candidate, characterize briefly:
- **What it would be:** the form factor in one sentence.
- **User behavior it assumes:** how users would discover, adopt, and use this form factor (e.g., a mobile app assumes app-store penetration; a browser extension assumes desktop-first usage).
- **How it relates to the painpoint:** which aspects of the painpoint this form factor addresses well, which it addresses poorly.

The goal is not to fully analyze each candidate — Task 5 will pick one. Task 2's output is the input range from which Task 5 selects.

### Task 3: Run the wrapper test

The question: *what does this purpose-built product do that a general-purpose LLM (Claude, ChatGPT, Gemini) couldn't do for the user directly?*

The wrapper test is not a yes/no — it's an honest characterization of what general-purpose LLMs already do in this space, and whether the proposed product offers something meaningfully beyond that.

Areas where purpose-built products typically beat general-purpose LLMs:
- **Proprietary data access:** the product has ingested or has rights to data the general LLM cannot access (real-time inventory, specific user transactions, gated APIs).
- **Transactional capability:** the product can complete actions the general LLM cannot (book tickets, transfer money, submit forms with verified identity).
- **Persistent context about the specific user:** the product accumulates preferences, history, and constraints that meaningfully change recommendations over time.
- **Integration with deterministic workflows:** the product orchestrates multi-step processes with state management that the general LLM cannot reliably do alone.
- **Multi-tool orchestration with reliability guarantees:** the product calls specific tools in specific sequences with error handling that the general LLM does ad-hoc.

If none of these (or comparable advantages) apply, the wrapper test fails — a general-purpose LLM can do this adequately for the user, and the proposed product is a thin wrapper.

These five areas of advantage are also primary inputs to the Defensibility dimension score below. The wrapper test asks "does this product offer one or more of these advantages?" — Defensibility scoring asks "how strong and durable are those advantages?" The two questions are related but distinct: a thin proprietary data advantage might pass the wrapper test (general LLMs don't have this data) but score low on Defensibility (the data is easily replicable). The analysis should treat them as connected views of the same underlying properties.

Apply the wrapper test result to the agent-fit verdict per `rubric.md`'s downgrade rule: a failed wrapper test downgrades the verdict by one level. Strong becomes Partial; Partial becomes Not agent-shaped. A failed wrapper test on a "not agent-shaped" verdict is consistent and requires no change.

If the test result is ambiguous (general-purpose LLM does *most* of this but not quite all), document the ambiguity and apply judgment about whether the gap is meaningful. A small gap that users would not notice in practice is closer to a failed test than to a passed one.

### Task 4: Generate the differentiation hypothesis

Draw on Task 4 from template 02 (dimensions of competitive choice) and Task 3 from template 02 (white space). Produce a single sentence: *the sharpest reason a user would choose this over the closest existing alternative.*

Apply default skepticism to your first answer. The first plausible-sounding hypothesis is rarely the sharpest one — work through 2–3 candidate hypotheses and pick the one that best survives the "what's the strongest argument against this?" question.

Examples of sharp differentiation hypotheses (structurally — not topically related to any specific idea):
- "Users would choose this because it surfaces real-time supplier inventory at checkout, eliminating the 'out of stock after I place the order' problem that drives 30% of cancellations in this category."
- "Users would choose this because it connects directly to municipal permit databases, replacing the 2–3 week manual lookup that's currently the bottleneck in their workflow."

Examples of weak hypotheses (avoid these):
- "Better user experience" — not specific
- "AI-powered" — describes the technology, not the user's reason to choose
- "More features" — feature count is not a differentiation
- "Local market focus" — describes the strategy, not the user's reason to choose this product specifically

If you can't write it in one sentence, that's a finding — the differentiation isn't sharp enough yet. Document the best available one-sentence hypothesis and note explicitly that it required generous interpretation to fit one sentence. The weak differentiation will be visible in the section output and the user can review it before the framework continues to section 04.

### Task 5: Recommend a form factor

Produce the form-factor recommendation that feeds execution planning. This is always a documented output, regardless of mode or verdict.

- **If Task 2 was skipped (user's specification confirmed by analysis):** document the recommendation as "[user's specified form factor], confirmed by analysis. No alternatives considered because the agent-fit evaluation aligned with the user's specification."
- **If Task 2 ran and the analysis recommends the user's originally specified form factor:** document the recommendation with reasoning, noting that alternatives were considered and rejected. Name the alternatives and explain briefly why each was rejected.
- **If Task 2 ran and the analysis recommends a different form factor than the user's specification:** document the recommendation, name the alternative considered, and explain why the change. This case requires surfacing to the user (see Recommendation subsection).

Format: a clear named form factor with one-paragraph reasoning.

The recommendation is the input to Section 06 (Solo-buildability), which will scope the build of this form factor. Sections 04, 05, and 07 will also reference the recommendation for their respective analyses.

### Task 6: Local lens application

How does form factor choice interact with the target market? Considerations:

- **Mobile-first markets:** in markets where mobile internet adoption significantly outpaces desktop, web apps face adoption barriers. A web app recommendation in a mobile-first target market should be flagged.
- **Regulatory constraints on form factors:** financial chatbots may face different rules than web apps in some jurisdictions (e.g., regulated advice requirements). Some form factors may be prohibited or face elevated compliance costs in specific markets.
- **Cultural patterns around form factors:** in some markets (especially where messaging platforms are the dominant communication channel), a WhatsApp-based service or chat-bot-on-existing-platform may be a viable form factor that would not appear obvious from a US/Europe-centric lens. The local lens should consider whether the dominant communication and discovery channels in the target market enable form factors that aren't visible from outside.
- **Infrastructure assumptions:** assumed app store penetration, assumed credit card payment flows, assumed broadband availability. Form-factor recommendations relying on any of these implicit assumptions should be flagged.

Flag any US/global defaults the form-factor reasoning has been relying on. If the local lens surfaces a meaningful constraint, document how it affects the form-factor recommendation from Task 5 — either confirming the recommendation, suggesting an adjustment, or surfacing the constraint as a finding for the user to consider.

## Scoring activated in this section

Two outputs from this section feed downstream:

- The **Defensibility dimension score** (numeric, contributes to overall commercial score). Inputs: the wrapper test result (Task 3), plus the broader defensibility picture (other moats identified during the analysis).
- The **Agent-fit verdict** (qualitative, descriptive only). Inputs: the agent-fit evaluation (Task 1), as potentially adjusted by the wrapper test downgrade rule (Task 3).

The two outputs are independent — a strong agent-fit verdict with a failed wrapper test produces a contradiction the analysis should explicitly resolve. The wrapper test downgrade rule from `rubric.md` handles this.

### Defensibility dimension

Score the Defensibility dimension on the 0–10 scale defined in `rubric.md`, with H/M/L conviction label. **This score is provisional** — section 09 finalizes it once sections 04 (regulatory moats) and 05 (data / network / business-model moats) are known. Score what is visible *now* (the wrapper test result and any moats already identifiable); do not guess at downstream moats, but flag any you expect 04/05 to confirm so section 09 can reconcile them.

Apply the Defensibility anchors from `rubric.md` — the **canonical source** (this is a synced copy; the worked examples live there). Keep it in sync if the rubric's anchors change:
- High (8–10): Real moats — proprietary data, transactional capability, network effects, regulatory licenses, or persistent personalization that competitors can't easily replicate.
- Medium (5–7): Some defensibility through execution quality, brand, or first-mover advantage. A determined incumbent could match within 12–18 months.
- Low (0–4): No meaningful moat. A general-purpose AI tool or larger competitor could absorb this as a feature in weeks.

The wrapper test result interacts with Defensibility as follows: a failed wrapper test (general-purpose LLM can do this adequately) means defensibility cannot come from the agent-shape alone. The score still considers other moats — proprietary data, transactional capability, regulatory licenses, network effects — but it cannot rely on "the agent does this" as a defensibility argument. If no other moats are present alongside a failed wrapper test, the score should be Low. If other moats are present, the score reflects those moats.

A 0–2 provisional score does **not** trigger an early-exit here (defensibility may still emerge in 04/05). It carries forward as the provisional Defensibility input to section 09, which finalizes the score and applies the **late veto** if it is still 0–2. Apply the anchor honestly — score the evidence visible now, and note any moats you expect 04/05 to surface.

### Agent-fit verdict (qualitative, not numeric)

Capture the verdict in the format specified in `rubric.md`'s Agent-fit section:
1. **Verdict:** strong agent fit / partial agent fit / not agent-shaped (after any wrapper test downgrade applied).
2. **Reasoning:** one sentence grounded in the specific characteristics of the idea, not generic talking points.
3. **Recommended form factor:** the actual shape the user would build (from Task 5).

If the wrapper test downgraded the verdict, note this explicitly in the reasoning.

The verdict is descriptive — it does not move ideas between matrix quadrants or affect kill recommendations. Its role is to inform execution planning and provide portfolio-level visibility.

## Section-specific content for the four required parts

The four required parts (Analysis, Recommendation, Rationale, Challenge pass) are mandatory in the section file per `SKILL.md`. Below is what each part contains for section 03 specifically.

### Analysis

Subsections in order: Agent-fit evaluation, Candidate form factors (if generated — note "skipped" when Task 2 did not run), Wrapper test, Differentiation hypothesis, Form factor recommendation, Local lens. Then the Defensibility score with conviction label and the qualitative agent-fit verdict.

The Analysis subsections should read as a connected investigation, not disconnected blocks. The agent-fit verdict (and any wrapper test downgrade) flows through to the form-factor recommendation. The differentiation hypothesis builds on template 02's white space and choice dimensions. The local lens may modify the form-factor recommendation.

### Recommendation

For section 03, the recommendation is typically **"Proceed to section 04"** — this section does not produce kill recommendations, and Defensibility is not an early-exit. A low provisional Defensibility score carries forward to section 09, which finalizes it (reconciling 04/05 moats) and applies the late veto only if it is still 0–2.

The recommendation changes to **"Surface to user before proceeding"** in these specific cases:
- Form factor specified in the brief was strongly challenged and the analysis recommends a different one.
- Wrapper test fails decisively, downgrading the agent-fit verdict and significantly affecting Defensibility.
- Differentiation hypothesis cannot be written in one sentence without generous interpretation.
- Defensibility score is very low (0–3) with implications the user should review before the framework continues building on it.
- The agent-fit verdict is "not agent-shaped" for an idea where the user explicitly stated learning interest in agents — worth surfacing as a finding so the user can decide whether to continue.

In these cases, do not stop the framework — surface the concern, get the user's input, then proceed.

### Rationale

The rationale connects the analytical work to the recommendation. It must include:
- The form-factor recommendation in one sentence.
- The wrapper test result and any verdict downgrade applied.
- The differentiation hypothesis as written.
- The Defensibility score with conviction label, and which inputs drove it.
- Any change between the user's specified form factor (if any) and the recommended one, with reasoning.

The rationale is what the user reads to understand why the section landed where it did. It must not just restate the analysis — it must connect analysis to conclusion explicitly.

### Challenge pass

The standard four falsification questions from `SKILL.md` apply, plus the section-specific questions below.

## Challenge pass: section-specific falsification questions

In addition to the standard four questions from `SKILL.md`, apply these to the form-factor and differentiation analysis:

- **Agent-rationalization check:** did we rationalize an agent shape onto a problem that would be better served by a simpler form factor? Look for: agent-fit lenses applied loosely, "could work as an agent" treated as "should be an agent," wrapper test glossed over, evaluation lenses double-counting overlapping characteristics. If the agent-fit verdict came up "strong" but the wrapper test was thin, the verdict may be inflated.
- **Wrapper-test-rigor check:** did we actually probe what general-purpose LLMs do in this space, or did we hand-wave the answer? A rigorous wrapper test names specific capabilities general LLMs have today and shows where this product goes beyond them with concrete examples. "General LLMs can't do this" without specifics is not a passed wrapper test — it's a skipped one.
- **Differentiation-sharpness check:** is the differentiation hypothesis specific enough to be falsifiable? Vague hypotheses ("better UX," "AI-powered," "more features") aren't differentiation; they're aspiration. A sharp hypothesis names what's different (specific capability or feature) and why a user would prefer it (concrete user benefit, not abstract quality).
- **Form-factor-bias check:** did we default to the form factor the user named without genuinely evaluating alternatives? If Task 2 was skipped, check whether the skip was justified (agent-fit verdict genuinely aligned with the user's specification) or just convenient (we accepted the user's framing without testing it).

Document the findings under the Challenge pass heading even if no changes were made to the analysis. If changes were made, note what changed and why.

## Depth calibration for this section

This section's analysis should produce ~600–800 words of substantive content (not counting headers or framework boilerplate). This matches `SKILL.md`'s general check-in threshold — section 03 is medium-weight, heavier than section 01's foundational work but lighter than section 02's research load.

Signs the section is too thin:
- Agent-fit verdict assigned without working through all five lenses.
- Wrapper test reduced to a sentence ("general LLMs can't really do this").
- Differentiation hypothesis vague ("we'd be better").
- Form factor recommendation without reasoning.
- Local lens absent or reduced to "the market is similar."

Signs the section is too thick:
- Detailed feature comparisons between form factors when one is clearly right.
- Wrapper test extended into LLM technical analysis that doesn't affect the verdict.
- Multiple paragraphs on candidate form factors when the agent-fit verdict has already determined the space.
- Defensibility analysis branching into financial projections (those belong in section 08).

If the brief specifies a depth override for this section, honor it and acknowledge it at the top of the output.

## Downstream dependencies

What later sections will consume from section 03:

- **Section 04 (Risk & compliance):** will reference the recommended form factor for jurisdiction-specific regulatory analysis (different form factors face different regulatory pictures — a financial agent and a financial web app may face different licensing requirements), **and will consume the wrapper test's capability findings (Task 3) as an input to its capability-feasibility check** — what general-purpose technology can and cannot do well in this space is exactly what section 04 needs in order to judge whether the idea is technically feasible at all.
- **Section 05 (Business model):** will reference the form factor when evaluating monetization options. Agent products and web apps face different business model constraints (subscription tolerance, transactional friction, user expectations around pricing).
- **Section 06 (Solo-buildability):** will reference the recommended form factor heavily — it determines what the user is actually building and therefore what the build effort looks like. A web app build and an agent build have very different time-to-MVP, skill requirements, and tooling.
- **Section 07 (Investment & GTM):** will reference the form factor for GTM channel selection. Mobile apps require different acquisition (ASO, app stores) than web apps (SEO, content) than agents (which often require novel distribution).
- **Section 09 (Decision):** will **finalize** the provisional Defensibility score (reconciling moats surfaced in sections 04–05) and apply the late Defensibility veto if it remains 0–2, then use the finalized score in the overall commercial average and the matrix; it also references the form-factor recommendation for the final decision artifact.