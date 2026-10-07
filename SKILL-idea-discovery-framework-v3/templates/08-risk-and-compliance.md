# Template: 08 — Risk and compliance

## Purpose of this section in the framework

Section 08 sets out the **structural picture** for one selected idea in its market:
- its regulatory and compliance envelope;
- whether the **data, APIs or partnerships** it needs are available to anyone (data access);
- whether **current technology can do it well** at all (capability feasibility).

It is where the **Structural gate** can fire, on any of three dealbreakers: legal or regulatory, data, or capability.

This section produces:
- The regulatory categories that apply to the idea, and the specific regulations within them
- Order-of-magnitude compliance cost and timeline
- Any partnerships or operational structures compliance requires
- The data-access and capability-feasibility assessments
- A synthesized structural picture, including the **legal envelope** that 09 checks the idea's revenue model against
- An evaluation against the Structural gate, and a recommendation: proceed to 09; proceed to 09 with a partner (a structural veto routed to partner); or a structural veto that ends the idea (kill or park)

**On legal interpretation:** Claude is not a lawyer, and this section is not legal advice. It is a best-effort synthesis of public regulatory information. Where interpretation has material consequences (licensing, structure, enforcement risk), say that professional legal review is needed. Treat the findings as inputs to a legal conversation, not a substitute for one.

Section 08 scores no commercial dimension. It **judges the idea it was handed**: it does not redesign the idea (a different payer, product, side of the market or market entry) to get around a block. Those alternatives already exist in 04 (`SKILL.md`, "No alternatives after the screen").

## Inputs

- **05's handoff:** the idea, who it serves, what is sold and who pays, and the **market**, which sets the jurisdiction. Analysis run against the wrong jurisdiction is structurally wrong.
- **07:** the form factor (different form factors can face different rules) and the wrapper test's capability findings.
- **06:** the regulatory and data-access facts surfaced there.
- **01:** the Constraints findings (law and regulation). Start from these and add only what is specific to this idea.

## Research activated in this section

Web search is **mandatory and heavy**. Regulations are jurisdiction-specific and change often, and training data is unreliable here. It must produce, at minimum:
- the regulations in the idea's market across the categories identified in Task 1;
- the bodies that enforce them, and their enforcement patterns where known;
- recent enforcement actions in this space (last 12–24 months), which show what regulators actually enforce;
- pending legislation or regulatory changes likely within 12–18 months.

Cite regulations by name and number (e.g., "Colombia's Ley 1581 de 2012 on personal data protection", not "Colombia's data protection law").

Deep research is warranted when:
- the regulation is complex (financial services, healthcare, regulated marketplaces, identity or money movement);
- the idea spans several jurisdictions;
- the rules are changing fast.

Follow the pause in `SKILL.md`, "Research and deep research".

**Source quality.** Prefer official sources: regulators' sites, government publications, primary legislation and, where relevant, court decisions. Be strongly skeptical of compliance-vendor "overviews", legal-marketing content, AI-generated summaries and news that summarizes laws without citing them.

**Fact discipline.** Named statutes and enforcement actions, with their numbers and dates, are the archetypal checkable facts. A confidently cited regulation that doesn't exist, or a wrong number or date, can drive a wrong gate call. Cite each at the point of use with its conviction, and add every named regulation to the claims-to-verify list, especially recent changes.

**Local lens (structural here).** The typical failure is defaulting to the most familiar framework (GDPR, US rules) instead of the market's own:
- search with local regulator names and local terms;
- confirm each cited regulation applies in this jurisdiction;
- confirm the local rule directly, rather than reasoning from a famous foreign equivalent;
- refine any search that returns mostly US or EU results.

## Analytical work for this section

### Task 1: Identify the regulatory categories that apply

Derive the categories from what the idea actually does: *what is this product doing that a regulator might care about?* Prompts, not a checklist:
- **Personal data:** data protection and privacy.
- **Money:** financial services, payments, money transmission.
- **Selling to consumers:** consumer protection, advertising, subscription billing, refunds.
- **Specific sectors:** licensing (health, education, transport, food, real estate, legal, financial advice).
- **Workers or marketplace participants:** employment law, gig-work rules, marketplace liability.
- **Revenue:** tax registration and obligations.
- **Third-party content:** IP, copyright, moderation, hosting liability.
- **Digital specifically:** accessibility, age verification, AI-specific rules where they exist.

Hardware brings product-safety and customs rules; marketplaces bring antitrust and listing liability; cross-border products bring export controls.

Output: the categories that apply, one sentence each, flagging any that are non-obvious.

### Task 2: Map each regulation to the idea

For each applicable regulation:
- **Name and identifier:** official name, number and date.
- **Regulator:** who enforces it.
- **What it requires:** registration, licensing, operating practices, disclosure, audit, reporting.
- **When it applies:** to everyone in the category, above a size threshold, or under specific conditions, including meaningful exemptions.

**Interpretive uncertainty.** Where it is unclear how a regulation applies to this idea, say so. Label it L, and note that legal review is warranted. Do not pick one reading and present it confidently.

### Task 3: Estimate compliance cost and timeline

For each requirement, estimate at order of magnitude, with conviction labels:
- **One-time costs:** licences, legal setup, entity formation, initial audits, technical compliance work.
- **Ongoing costs:** renewals, audits, reporting, compliance staff or services.
- **Operational complexity:** how much compliance shapes day-to-day operations (consent flows, data localization, retention rules).

"Setup: low five figures; ongoing: low four figures a year (M, from published compliance-service pricing)" is the right precision. Separate what is expensive from what is merely procedural.

### Task 4: Identify partnership or operational requirements

Some regulations require a partner or a structure: a banking partner or money-transmitter licence, local infrastructure for data localization, licensed professionals on staff or contracted, identity-verification partners, an entity in a specific jurisdiction. For each, note:
- what is needed;
- what it implies for cost and time;
- whether a new entrant building this could realistically obtain it, and, if not, whether an existing licence holder or partner could supply it.

A required licence or partnership that **no one** building this could obtain is functionally a legal block (the canonical condition is in `SKILL.md`, "The kill model"); if an existing holder could supply it, the veto routes to partner (Task 9). Whether **this founder** could hold it is not a gate question: record it for 10, where it shapes the build strategy.

### Task 5: Assess data access (structural veto input)

The question is **market-structure availability**: do the data sources, APIs, integrations or partnerships the idea needs exist, and is access structurally available *to anyone* building this? Whether *this founder* can obtain it is 10's question. Assess and conviction-label:
- **What the idea needs** to work at all (real-time inventory, transaction data, a gated API, a partner feed, scrapable sources).
- **Whether access is available:**
  - available: public or licensable APIs, partnership programmes, scrapable sources with no prohibitive legal barrier;
  - conditional: achievable, but through negotiation, a partnership or a legal grey area;
  - blocked: locked behind gatekeepers with no path for a new entrant, or legally prohibited.

Pull in the data-access facts from 06.

### Task 6: Assess capability feasibility (structural veto input)

Can **current technology do this well at all**? This is an opportunity-level question (can *anyone* build it so it works), distinct from 10's (can *this founder*). Start from 07's wrapper test. Assess and conviction-label:
- **The core capability** the idea depends on (e.g., reliable extraction from messy documents, real-time multi-step orchestration, domain reasoning users would trust).
- **Whether current technology meets that bar:**
  - clearly yes, proven in comparable products;
  - plausibly, with engineering effort;
  - no: the required quality or reliability is beyond current technology.
- **Trajectory:** if it is not there yet but improving fast, say so. That routes to *park*, not *kill*.

### Task 7: Check the local lens

Confirm the analysis is about the idea's actual market:
- Are the cited regulations from that jurisdiction?
- Were frameworks assumed (GDPR-style, US-style) that don't exist there, or exist in a different form?
- Are there local rules a generic search would miss (language requirements, local data localization, national sector rules)?
- What is the enforcement reality: rules on the books but rarely applied, or strict enforcement of minor violations?

Flag any correction the local lens made.

### Task 8: Synthesize the structural picture

In one or two paragraphs, characterize the envelope the idea would operate within:
- the categories that matter most;
- total compliance cost, one-time and ongoing, at order of magnitude;
- required partnerships or structures;
- the data-access position (available / conditional / blocked);
- the capability position (feasible / feasible with effort / not yet / infeasible);
- the realistic time from "decide to build" to "legally allowed to operate";
- material uncertainty: pending changes, interpretive ambiguity, enforcement unpredictability, contested data access, or capability that is improving but not there yet.

This is the **legal envelope** 09 checks the idea's revenue model against.

### Task 9: Evaluate against the Structural gate

Apply the gate's three conditions to the structural picture: **legal or regulatory blocked**, **data access blocked** and **capability infeasible**. Their precise tests (the "obtainable by no one" bar and the disproportionate-cost carve-out) are canonical in `SKILL.md`, "The kill model". Each is a *conclusion from the research above*, never a substitute for it.

**If any condition is met, the gate fires.** Route per `rubric.md`:
- **Partner:** a partner can supply the missing piece (a licensed partner for legal, a data partner for data, a specialized-capability partner for capability). This is the same idea with a partner, not a different idea. Monetization (09) is not scored yet and Defensibility is still provisional, so state that the partner route is **conditional on the commercial case holding up**. The evaluation **continues to 09 with the partner built in**: 09–12 price it, and the rest of the evaluation is what tests that condition.
- **Kill:** the missing piece is unavailable to anyone.
- **Park** (capability only): the technology isn't there yet but is improving.

A veto applies the challenge pass to itself and is confirmed per the conviction-gated rule. A kill or park resting on a Low-conviction finding (a contested regulatory reading, a disputed data block) escalates rather than auto-confirming; a partner route continues, with that finding carried to 13's validation layer. A kill or a park ends **this idea's** evaluation: 13 records the stop-point, the route and the sections not run (a park is recorded as **parked**, not killed, with the capability change that would reopen it), and the run continues with the next selected idea, if any.

**If no condition is met, the gate does not fire.** That is the expected outcome and **not a health signal** ("Gates are rare by design", `SKILL.md`). The research is still the load-bearing output.

## Section-specific content for the four required parts

The four required parts are mandatory per `SKILL.md`.

### Analysis

Labelled subsections, in order: Regulatory categories; Regulations and requirements; Compliance cost and timeline; Partnership and operational requirements; Data access; Capability feasibility; Local lens; Structural picture; Structural gate evaluation. Then a **Moat candidates** line (regulatory moats, if any) and the claims-to-verify list.

### Recommendation

One of three:
- **"Proceed to 09."**
- **"Structural veto — [legal / data / capability], routed to partner: proceed to 09 with a [type] partner"**, conditional on the commercial case.
- **"Structural veto — [legal / data / capability], routed to [kill / park]."**

Findings that the founder should weigh but that do not fire the gate are **recorded, not surfaced mid-run**: a required partnership, a material but not disproportionate compliance cost, conditional data access, capability that needs effort or time, regulatory uncertainty, or rules the idea's framing did not anticipate. Name them in the Rationale; 09, 10, 11 and 12 use them, and 13 reports them.

### Rationale

**For a proceed**, cover:
- the regulations that apply;
- the compliance cost at order of magnitude;
- required structures or partnerships;
- any of the recorded findings above.

**For a veto**, cover:
- which condition fired, and the specific finding that triggered it;
- the route (with the conditional note for a partner route);
- the challenge pass applied to the veto;
- a note that it is confirmed per the conviction-gated rule.

### Challenge pass

The judging form from `SKILL.md` (06–13 omit the "non-obvious option" question), plus the section-specific questions below. For a veto, the challenge pass asks what would make the veto wrong. Each finding uses the fixed short format: what changed and why, or "no change".

## Challenge pass: section-specific questions

- **Jurisdiction check:** were the right jurisdiction's regulations applied? Re-verify any doubtful citation.
- **Interpretation check:** has enforcement intent (what regulators care about) been confused with the text (what the law says)?
- **Structural workaround check** (for vetoes): could a different **legal structure for the same idea** change the picture? Consider a different entity type, or running the regulated function through a licensed partner's infrastructure. Changing who pays, what is sold or the market entry (e.g., B2B2C instead of direct) is a different idea, not a workaround. If 04 has no such idea, flag that gap for 13 (`SKILL.md`, "Upstream/downstream dependencies").
- **Enforcement realism:** is the regulation actually enforced here? Use this only to calibrate cost realism; never advise ignoring a regulation because it is rarely enforced.

## Word cap

**Hard maximum (provisional), by regulatory load, excluding citation markers and the source list:**
- low-regulation ideas (B2B SaaS, content and productivity tools): **600 words**;
- moderately regulated (consumer products, marketplaces, data-heavy products): **1,000 words**;
- heavily regulated (fintech, health, regulated marketplaces, identity or money movement): **1,500 words**.

State the tier at the top of the section.

## Downstream dependencies

What later sections consume from section 08:
- **09** checks the idea's revenue model against the legal envelope (Business-model gate, cause a), and prices a partner route's cut or fees into the unit economics.
- **10** uses the partnership and operational requirements when assessing what the founder can build alone.
- **11** uses the compliance cost and timeline in the initial investment.
- **12** carries ongoing compliance costs as a line item.
- **13** uses the structural picture, the gate evaluation and the recorded findings (including anything needing legal review), and reconciles any regulatory or data moats into the final Defensibility score.
