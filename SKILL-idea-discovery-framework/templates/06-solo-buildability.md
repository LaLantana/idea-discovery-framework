# Template: 06 — Solo-buildability

## Purpose of this section in the framework

This section scores the Solo-buildability dimension of the 2×2 matrix — the second axis of the matrix decision in section 09. Unlike the commercial dimensions scored in sections 01–05, Solo-buildability is never a kill criterion on its own (per `rubric.md`). The score informs strategy:
- High commercial + high solo-buildability → pursue immediately
- High commercial + low solo-buildability → pursue with partnership strategy
- Low commercial + anything → kill (driven by the commercial score, not by solo-buildability)

No process gate fires in this section.

**On scope:** this section independently assesses whether the user (per the profile documented in `user-profile.md`) could ship this MVP solo. It does not influence what the right product is (section 03 handles that), what the right business model is (section 05), or what the right GTM is (section 07). Those sections describe what the idea requires; section 06 assesses whether the user can execute it. **Note the division of labor with section 04:** section 04 asks the *opportunity-level* question — can the data be obtained, and can current technology do this, by *anyone* (its data-access and capability structural vetoes); section 06 asks the *user-level* question — can *this* user obtain that access and build this, given their profile. Same subjects, different question.

This section produces:
- A summary of what's being built (drawn from the cumulative picture across sections 01–05)
- An inventory of required skills and capabilities
- A mapping of those skills against the user profile from `user-profile.md`
- An order-of-magnitude estimate of time and capital required to ship the MVP
- A detailed partnership requirements assessment (if any partnerships are needed)
- A score on the Solo-buildability dimension of the matrix
- A recommendation to proceed to section 07, or in edge cases, to surface concerns to the user

## Brief fields relevant to this section

Before starting the analytical work, draw on these fields from `00-brief.md`:

- **Recommended form factor (from section 03):** the central input. Defines what's being built and therefore what skills the build requires.
- **Partnership/operational requirements (from section 04):** required partnerships are direct solo-buildability constraints. A banking partner requirement caps solo-buildability regardless of the user's technical skill.
- **Synthesized business model picture (from section 05):** some models require infrastructure that affects buildability (e.g., transactional models requiring payment processing, marketplace models requiring two-sided dynamics).
- **Learning value field (from the brief):** relevant for the matrix's learning-project exception applied in section 09.
- **Depth overrides (if any):** acknowledge at the top of the section output. Common overrides: "I've already done [specific component] before — skip detailed assessment," "go deeper on partnership requirements — I want to understand what I'd need."

If any of these fields are missing or unclear, surface the gap to the user before starting analytical work.

## Research activated in this section

Research is mostly discretionary in this section, but warranted for tooling, infrastructure costs, and partnership accessibility.

### Web search (discretionary)

Use web search when:
- Current tooling and frameworks for the recommended form factor need to be confirmed (tooling shifts frequently in some categories — what was best practice 18 months ago may not be now).
- Realistic build-time benchmarks for similar products would sharpen the time estimate.
- Partnership accessibility needs to be evaluated (e.g., what does it actually take to get a banking partner in the target market today?).
- Pricing of infrastructure and services the build requires is uncertain.

### Deep research (user-confirmed)

Rarely warranted in this section. Possible exception: highly novel build challenges where structured investigation across comparable solo builds would inform the assessment. When warranted, follow the deep-research escalation protocol in `SKILL.md`.

### Source quality

Conviction labeling follows the standard categorization from template 01. Be especially skeptical of "I built a [thing] in [short time]" blog posts and developer tutorials — they often skip operational complexity, regulatory work, edge cases, and the long tail of real deployment. Cite sources directly.

## Analytical work for this section

These tasks together produce the **Analysis** portion of the section file. The Recommendation, Rationale, and Challenge pass are produced after the analytical work, drawing on it.

**Reminder of section scope** (full statement in Purpose subsection above): section 06 assesses whether the user can execute the MVP as designed by sections 03–05. If the assessment reveals the user cannot ship this MVP solo, the answer is "pursue with partnership strategy," not "redesign the product to be simpler."

### Task 1: Establish what's being built

Read the recommended form factor from section 03 and the synthesized business model picture from section 05. Produce a short summary of the MVP being scoped:

- **The form factor** and its core technical components.
- **The business model's infrastructure implications:** payment processing, integrations, partnerships, billing systems if applicable.
- **The data access requirements** identified across sections (proprietary data, APIs, scraping, partnerships for data). Section 04 assessed whether this access is *structurally* available to anyone building this (the data-access structural veto — opportunity-level); here the question is whether *this user* can actually obtain it, given their resources and relationships (user-level) — assess that as part of the skill and partnership mapping in Tasks 2–3.
- **The compliance infrastructure required** (per section 04's partnership/operational requirements).

This is the "what" being built. The subsequent tasks evaluate whether the user can build it.

### Task 2: Inventory required skills and capabilities

For the MVP being built, identify the skills and capabilities required:

- **Technical skills:** specific frameworks, languages, infrastructure, AI/LLM integration, payment integration, mobile/web/agent-specific skills, data engineering if applicable.
- **Operational capabilities:** customer support setup, legal/compliance work, business operations, billing and finance operations.
- **Partnership capabilities:** the ability to identify, negotiate, and maintain partnerships if any are required by section 04 or section 05.
- **Domain expertise:** specialized knowledge required to build something credible in this category (e.g., financial domain knowledge for fintech, healthcare for health products, supply chain for logistics products).

For each, note whether it's a common-to-most-builders capability, something requiring specific learning, or something specialized that typically requires either deep expertise or partnership. The output is a structured inventory ready for mapping against the user profile in Task 3.

### Task 3: Map required skills against the user profile

This is the section's central work.

**Before starting this task, read `user-profile.md`.** The profile documents the user's capabilities, learning trajectory, and typical gaps. The mapping in this task is against whatever that profile says — the template does not assume any particular profile content.

For each required skill/capability from Task 2:

- **Profile already has it:** the skill is within the documented capability range in `user-profile.md`.
- **Profile can reasonably learn it within the build window:** the skill is adjacent to documented capabilities and learnable within a realistic action window (per `rubric.md`'s anchor language).
- **Profile would need a partner for it:** the skill sits beyond the profile's documented range — specialized, slow to learn, or requires credentials/relationships the profile doesn't have.
- **Profile would need to hire or contract for it:** specialized but obtainable through paid services.

The mapping runs against the default profile. If the user notes at the section 06 checkpoint that their actual situation differs from the documented profile — e.g., they have specific experience in an area the profile doesn't assume, or they have an existing partnership that fills a gap — Claude revises this task's output based on the user's input. Note the revision explicitly so the assessment is traceable.

**On honesty:** the profile is calibrated to a specific capability range. Assessments that consistently produce "the profile can learn anything" are not honest mappings — they ignore the profile's calibration. The point of having a profile is to make solo-buildability assessments consistent across ideas and across users; honoring the profile's actual content is what enables that consistency.

### Task 4: Time and capital estimate

Estimate, at order-of-magnitude:

- **Time to MVP solo:** how many weeks or months to ship a credible MVP at the profile's assumed commitment (~20 h/week — see `user-profile.md`'s build-speed baseline) once the learning gaps identified in Task 3 are addressed?
- **Time to MVP with partnership:** if Task 3 surfaced partnership requirements, how does the time picture change with the right partner?
- **Capital required for MVP solo:** out-of-pocket costs to ship — tooling, infrastructure, AI tokens, paid services, anything that requires money rather than time.
- **Capital required for MVP with partnership:** how partnership changes the capital picture (it may reduce or shift it depending on whether the partner brings capital, technical resources, or specialized labor).
- **Against the brief's runway:** if the brief gives a runway (available capital) and the build capital alone would exceed it, flag it here — the user cannot fund even the build as scoped. If the brief gives no runway, just report the capital figure (section 07 builds the fuller investment-vs-runway picture).

**Scope of this task:** this is an order-of-magnitude estimate from the build perspective. Specifically *not* included here:
- GTM costs (customer acquisition, marketing) — covered in section 07.
- Operational costs beyond the build (ongoing infrastructure beyond MVP, ongoing compliance) — covered in section 07.
- Multi-year capital planning — covered in section 08.

The question this task answers: *how long does the user need to build the MVP, and how much capital does the build itself require?* The fuller investment and operational picture is built in section 07.

Conviction labels apply. Time estimates with thin evidence get L conviction.

**On time-estimate optimism:** time estimates are notoriously optimistic — apply default skepticism. Specifically, consider whether the estimate accounts for the long tail of real shipping: testing across realistic conditions, deployment work, edge cases, security review, integration debugging, the things-that-go-wrong tail. "Two weeks" estimates from developer blog posts almost always exclude this tail. Build the estimate from realistic assumptions, not best-case ones.

### Task 5: Partnership requirements detailed assessment

If Task 3 surfaced any "profile would need a partner" gaps, evaluate each:

- **What kind of partner:** technical co-founder, domain expert, data partner, capital partner, licensed professional, operational partner.
- **Realistic accessibility:** how hard is it to find this kind of partner? What does the partnership market look like in the target market specifically?
- **What the partnership requires from the user:** equity, revenue share, salary, project fee, advisor share.
- **Timeline to secure:** weeks, months, or longer to identify and bring on a partner.
- **Risk if the partnership doesn't materialize:** what happens to the idea if the user cannot find this partner within a reasonable window?

If no partnerships are required (Task 3 found no gaps requiring partner), this task is brief — note that the MVP is buildable without partnership and move on.

### Task 6: Apply the local lens

How does the target market shape solo-buildability? Considerations:

- **Local talent and partnership availability:** is the kind of partner the user might need accessible in the target market? Some technical specializations are concentrated geographically; some kinds of partnership are more or less culturally common in different markets.
- **Infrastructure costs in the target market:** hosting, services, and tooling can have meaningfully different costs in different markets. Some markets have local alternatives that change the capital picture significantly.
- **Regulatory operational complexity:** beyond compliance costs from section 04, what's the operational complexity of running a business in this market? Some markets have simpler vs. more complex business operations regardless of regulatory category (entity formation friction, tax administration burden, banking friction for new businesses).
- **Local norms around solo founding vs. team founding:** some markets have stronger cultural expectations of team founding, which can affect partnership availability, customer credibility, and investor reception (if external capital becomes relevant).

Flag any cases where the local lens revealed a meaningful constraint on solo-buildability that the user may not have anticipated.

### Task 7: Synthesize the solo-buildability picture

Pull together findings from Tasks 1–6 into a coherent picture:

- Can the user (per the profile, with any noted adjustments) ship this MVP solo? With what learning required?
- If not solo, what specific partnership(s) would be needed?
- What's the realistic timeline and capital required, in both the solo and partnership scenarios?
- What are the main risks in the build that could extend timeline or block shipping?

The synthesis should produce a clear picture that section 07 can use to estimate full investment and section 09 can use for the matrix decision.

## Scoring activated in this section

### Solo-buildability dimension

Score the Solo-buildability dimension on the 0–10 scale defined in `rubric.md`, with H/M/L conviction label. Apply the anchor descriptions from `rubric.md`'s Solo-buildability section directly — do not paraphrase the anchors.

The score is based on the synthesis from Task 7. Conviction label reflects the evidence behind the assessment:
- **High (H):** the profile (per `user-profile.md`) has documented capability with the kind of work this MVP requires, and the build is structurally similar to work the profile covers.
- **Medium (M):** the work is adjacent to documented profile capabilities — reasonable inference, but no direct match.
- **Low (L):** novel territory for the profile — the assessment is based on reasoning about what the profile probably can or cannot do, without documented capability as anchor.

**Reminder:** per `rubric.md`, Solo-buildability is never a kill criterion on its own. A 0–2 score moves the idea to the "Pursue with partnership strategy" or "Kill" quadrant depending on commercial score — but the kill is driven by commercial, not solo-buildability.

## Section-specific content for the four required parts

The four required parts (Analysis, Recommendation, Rationale, Challenge pass) are mandatory in the section file per `SKILL.md`. Below is what each part contains for section 06 specifically.

### Analysis

Subsections in order: What's being built, Required skills and capabilities, Profile mapping (with any user-noted adjustments), Time and capital estimate, Partnership requirements detailed assessment (or "Not applicable — no partnerships required"), Local lens, Synthesized solo-buildability picture. Then the Solo-buildability score with conviction label.

The Analysis subsections should read as a connected investigation, not disconnected blocks. The skill inventory feeds the profile mapping; the profile mapping feeds the time and capital estimate and the partnership requirements; the local lens may modify the partnership requirements and capital estimate; the synthesis pulls everything together.

### Recommendation

Two possible recommendations from this section — no kill option:

- **Proceed to section 07** — the standard case. The solo-buildability picture is clear and section 07 can use it to estimate full investment and design GTM that fits the available execution capacity.

- **Surface to user before proceeding** — when the analysis surfaced findings the user should see:
  - Significant gap between profile capabilities and required skills that may extend the time-to-MVP beyond what the user expected.
  - Partnership requirements that materially change what executing this idea looks like (e.g., the brief implied solo-build, the analysis surfaced an unavoidable partnership requirement).
  - Time or capital estimates that look very different from what the user assumed.
  - Local lens surfacing constraints the user didn't anticipate.
  - **Solo-buildability score of 0–2** — the user is in "Pursue with partnership strategy" or potentially "Kill" territory, and section 07 will scope investment under the assumption of partnership or team requirements. The user should confirm this before section 07 starts that work.
  - **The user's actual situation likely differs from the documented profile in ways that materially affect the assessment** — surface to give the user a chance to adjust the profile mapping before the score is finalized.

In all cases, do not stop the framework — surface the concern, get the user's input, then proceed.

### Rationale

For a proceed recommendation, the rationale must include:
- The synthesized solo-buildability picture in one or two sentences.
- The Solo-buildability score with conviction label.
- Key time and capital estimates (solo and, if relevant, partnership).
- Partnership requirements if any.
- Any profile adjustments applied based on user input at the checkpoint.

For a surface recommendation, the rationale includes the above plus the specific concern being surfaced and what the user is being asked to weigh.

### Challenge pass

The standard four falsification questions from `SKILL.md` apply, plus the section-specific questions below.

## Challenge pass: section-specific falsification questions

In addition to the standard four questions from `SKILL.md`, apply these to the solo-buildability analysis:

- **Time-estimate-realism check:** does the time estimate account for the long tail of real shipping — testing, deployment, edge cases, security review, integration debugging, the things-that-go-wrong tail? Optimistic time estimates are the most common failure mode in solo-build assessments. If the estimate sounds clean and short, it almost certainly excludes this tail.

- **Profile-honesty check:** is the mapping in Task 3 honest about what the profile (per `user-profile.md`) can do, or has it been stretched to include "things the profile could probably learn" without realistic assessment? The profile is calibrated to a specific capability range — assessments that consistently produce "profile can learn anything" are not honest mappings. They ignore the profile's calibration and produce inflated solo-buildability scores.

- **Operational-complexity check:** did the analysis account for ongoing operational requirements (customer support, payments operations, content moderation if applicable, regulatory reporting), or only the build itself? A product that's quick to build but operationally heavy is a different solo-buildability picture — the build estimate may be honest while the ongoing operational picture is missed.

- **Partnership-realism check:** if partnerships are required, is the partnership market realistic? Some kinds of partners (technical co-founder for a niche specialization, licensed professional in regulated industries, capital partner for a specific stage) are genuinely hard to find — assessing their availability honestly affects the time and feasibility picture. A "we need a banking partner" finding without honest assessment of how hard banking partnerships are to get for new entrants is incomplete.

Document the findings under the Challenge pass heading even if no changes were made to the analysis. If changes were made, note what changed and why.

## Depth calibration for this section

Section 06 is moderate weight. The work is largely structured (skill inventory, mapping, estimates), and the depth scales with the complexity of what's being built.

Normal depth range: ~600–900 words of substantive content (excluding headers and framework boilerplate). Heavier when partnership requirements are substantial; lighter when the MVP is straightforward and partnership-free.

`SKILL.md`'s general ~600–800 word check-in threshold applies as a self-check signal — at that point, confirm the additional depth is contributing to the solo-buildability score or downstream sections, not optimizing past the decision threshold.

Signs the section is too thin:
- Skill inventory reduced to one or two items.
- Profile mapping skipped or done without referencing `user-profile.md`.
- Time and capital estimates without basis.
- Partnership requirements glossed over when Task 3 surfaced gaps.
- Local lens absent.

Signs the section is too thick:
- Detailed technical architecture that belongs in execution planning, not discovery.
- Exhaustive tooling comparison across many frameworks.
- Step-by-step build plans rather than order-of-magnitude estimates.
- GTM execution planning that belongs in section 07.

If the brief specifies a depth override for this section, honor it and acknowledge it at the top of the output.

## Downstream dependencies

What later sections will consume from section 06:

- **Section 07 (Investment & GTM):** will consume the **Time and capital estimate** subsection and the **Partnership requirements detailed assessment** subsection when estimating initial investment. The build cost picture from section 06 plus GTM cost in section 07 plus operational and compliance costs build the full investment picture.
- **Section 08 (Financial projections):** will consume the time estimates for the launch timeline assumptions in the multi-year projections.
- **Section 09 (Decision):** will consume the **Solo-buildability score** (with conviction label) as the second axis of the 2×2 matrix. Will also reference the **Synthesized solo-buildability picture** for the final decision artifact, particularly when the matrix lands in the partnership-strategy quadrant.
