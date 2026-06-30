# Template: 01 — Problem & user

## Purpose of this section in the framework

This is the first analytical section of the discovery process. It establishes whether the idea is grounded in a real problem affecting real users in the target market. Without this foundation, every subsequent section (market size, business model, GTM) rests on speculation.

This section produces:
- A precise characterization of the target user and the painpoint
- An honest assessment of the evidence backing the painpoint claim
- A score on the Problem severity dimension of the commercial score
- A recommendation to proceed to section 02 — or, if Problem severity is fatally low (0–2), an early-exit kill recommendation; or, in edge cases, a surface-to-user concern

This section **can** produce a kill. Problem severity is a commercial veto dimension: a score of **0–2** (no real or severe problem) is a fatal flaw that no later section can repair, so it fires here as an **early-exit** — recommend the kill and stop, rather than running sections 02–09 on a non-problem. A score of **3 or above** is survivable; it feeds the commercial average at section 09, and the section recommends proceeding to 02. (See `rubric.md`, "The kill model," for the veto families and routing.)

## Brief fields relevant to this section

Before starting the analytical work, draw on these fields from `00-brief.md`:

- **One-line description:** anchors what the idea actually is.
- **Primary market and why this market:** required for the local lens application.
- **Relevant prior knowledge:** what the user has already observed or learned about the painpoint. Often the most useful evidence for the Problem severity score.
- **Depth overrides (if any):** acknowledge at the top of the section output. Common overrides for this section: "go deeper on user characterization," "skip detailed evidence review — I already have interviews," "focus on the [specific sub-segment] within the target user group."

If any of these fields are missing or unclear, surface the gap to the user before starting analytical work rather than proceeding with assumptions.

## Research activated in this section

Web search is discretionary in this section, not mandatory. Use it when:
- The user's prior knowledge in the brief is thin and the painpoint needs external validation (industry surveys, user behavior research, secondary sources).
- The local lens requires understanding how the painpoint manifests specifically in the target market (cultural patterns, regional behaviors, local solutions in use).
- Identifying analogous painpoints in adjacent markets or industries would sharpen the analysis.

Conviction-label findings using the same categorization as the Identify evidence task below: primary evidence sources → H; secondary evidence sources → M; tertiary or hypothesis-level sources → L. Cite sources directly in the analysis.

Deep research is not warranted by default in this section. If the painpoint turns out to require structured multi-source investigation (e.g., a complex regulated industry where painpoints are not publicly discussed), follow the deep-research escalation protocol in `SKILL.md`.

## Analytical work for this section

These tasks together produce the **Analysis** portion of the section file. The Recommendation, Rationale, and Challenge pass are produced after the analytical work, drawing on it.

### Define the target user precisely

The user is not "people who watch movies" or "businesses with budgets." Precision matters because vague users produce vague painpoints which produce uncheckable claims.

Characterize the target user along these dimensions:
- **Role or identity:** what makes them this user (frequent moviegoer, finance manager at a 50–200 employee company, small business owner with international clients, etc.)?
- **Demographics relevant to the painpoint:** age range, income bracket, geographic concentration, technical literacy — only the demographics that actually affect the painpoint.
- **Frequency of encountering the problem:** weekly, monthly, occasionally, situational.
- **Current behavior:** what they do today when they encounter the painpoint.

Avoid composite users that combine multiple distinct segments ("frequent moviegoers and casual moviegoers"). If the idea genuinely targets multiple distinct user types, characterize each separately and identify the primary.

### Characterize the painpoint

For the user defined above, describe the painpoint with specificity:
- **What goes wrong:** the actual friction, failure, or unmet need.
- **Severity:** what does it cost the user when it happens (time, money, frustration, missed opportunity)?
- **Frequency:** how often does this happen for the typical target user?
- **Workarounds:** what do users do today to avoid or mitigate the painpoint? Are these workarounds tolerable or actively painful?
- **Current solutions:** what tools, services, or behaviors do users currently rely on, and where do those fall short?

A painpoint that has tolerable workarounds is structurally different from one without. Both can be real, but their commercial implications differ.

### Identify evidence

For the painpoint characterization above, state honestly what evidence supports each claim. Categorize:
- **Primary evidence:** direct user observation, interviews, transactional data, observed behavior. Highest conviction.
- **Secondary evidence:** industry reports, academic research, journalistic accounts, third-party data. Medium conviction.
- **Tertiary evidence:** reasoning from analogous markets, anecdotal reports, secondhand observation. Low conviction.
- **Hypothesis:** the user's own intuition or pattern-matching, without external validation.

A painpoint characterized entirely from hypothesis is not invalid, but it must be labeled honestly. The Problem severity score will reflect the evidence quality through its conviction label.

### Local lens application

Apply the geographic lens specified in the brief to the painpoint analysis:
- Is the painpoint present in the target market at the severity and frequency described, or does it manifest differently there?
- Are there local solutions (incumbents, workarounds, cultural adaptations) that change how the painpoint is experienced?
- Are there market-specific factors (regulatory, infrastructural, behavioral, demographic) that amplify or dampen the painpoint?

Common defaults that often don't transfer across markets: assumed credit card penetration, assumed app-store-first discovery, assumed English-language content, assumed urban infrastructure. Flag any of these if the analysis is relying on them implicitly.

If the brief specified "open search" or "primary plus expansion candidates" for the market expansion question, evaluate the painpoint in the primary market in depth here, and defer the expansion-market analysis to section 02 where the comparative work belongs.

## Scoring activated in this section

### Problem severity dimension

Score the Problem severity dimension on the 0–10 scale defined in `rubric.md`, with H/M/L conviction label.

Apply the Problem-severity anchors from `rubric.md` — the **canonical source** (this is a synced copy; the worked examples live there). Keep it in sync if the rubric's anchors change:
- High (8–10): Multiple signals of acute pain present — users pay for inadequate workarounds *and* the painpoint is both frequent (weekly or more) and material (costs significant time, money, or friction). Users may also complain about the problem unprompted, but unprompted complaints alone are not enough.
- Medium (5–7): Users acknowledge the painpoint when prompted; one or two signals present but not all. Workarounds exist and are imperfect but tolerable.
- Low (0–4): Painpoint is hypothesized but not validated, or users don't recognize it as a problem when asked.

Conviction label reflects evidence quality from the "Identify evidence" task above. A score backed by primary evidence is H; a score backed by secondary evidence is M; a score from hypothesis alone is L.

A 0–2 score on this dimension is a **fatal commercial veto**: it triggers the **early-exit** — recommend the kill and stop (see the Recommendation section below). The 2/3 line is a cliff (a 2 ends the evaluation; a 3 continues it), so apply the anchor honestly and score the evidence, not the consequence.

## Section-specific content for the four required parts

The four required parts (Analysis, Recommendation, Rationale, Challenge pass) are mandatory in the section file per `SKILL.md`. Below is what each part contains for section 01 specifically.

### Analysis

Structure the Analysis as four labeled subsections corresponding to the four analytical tasks, in order: Target user, Painpoint, Evidence, Local lens. Each subsection contains the output of that task as developed in the analytical work above.

After the four subsections, include the Problem severity dimension score and its conviction label, with one or two sentences explaining how the analytical work produced the score (which anchor it matches, what the conviction reflects).

The Analysis subsections should read as a connected investigation, not four disconnected blocks — later subsections may reference findings from earlier ones (e.g., the Evidence subsection refers back to specific painpoint claims; the Local lens subsection notes which user characteristics or painpoint features change in the target market).

### Recommendation

For section 01, the recommendation is one of three:

**"Proceed to section 02"** — the standard case, when Problem severity is **3 or above**. The score feeds the commercial average later; this section does not resolve the full commercial picture.

**"Early-exit kill"** — when Problem severity is **0–2**. This is the Problem-gate commercial veto (defined in `SKILL.md`'s kill model); it fires here rather than at section 09. Follow the **kill protocol in `SKILL.md`** — write all four parts (the Analysis still does the complete user / painpoint / evidence / local-lens work that justifies the 0–2), apply the challenge pass to the kill itself, confirm per the conviction-gated rule, then write `09-decision.md` noting the early-exit and which sections were skipped — with two section-specific notes:
- The challenge-pass-on-kill uses the section-specific falsification questions below (bubble, frequency, workaround, articulation) — they're the ones that test a weak-problem kill.
- Route per `rubric.md`: a commercial veto routes to a **clean kill** or a **pivot** (a re-brief targeting a different user segment that genuinely has the pain) — never "needs a partner."

**"Surface to user before proceeding"** — when the issue is an ambiguity to resolve rather than a clean score:
- Brief fields were missing or unclear and could not be reasonably inferred from context.
- The target user described in the brief and the painpoint as analyzed don't align (e.g., the brief targets SMB finance managers but the painpoint as described is consumer-facing).
- The analysis surfaced findings that contradict the user's stated prior knowledge in a way that materially affects the score.
- A borderline score sits right on the early-exit cliff (a 2 that could defensibly be a 3) at low conviction — surface it rather than auto-killing on thin evidence (the validation layer applied at the boundary).

In the surface-to-user cases, do not stop the framework — surface the concern, get the user's input, then proceed (or early-exit, if the resolved score is 0–2).

### Rationale

The rationale connects the analytical work to the recommendation. For the standard "proceed" recommendation, the rationale states:
- What the user looks like and what the painpoint is, in one or two sentences.
- The Problem severity score and conviction label.
- The key evidence supporting the score (or the explicit absence of it, for low-conviction scores).
- Any local-lens findings that materially affected the score.

The rationale is what the user reads to understand *why* the section landed where it did. It must not just restate the analysis — it must connect analysis to conclusion explicitly.

### Challenge pass

The standard four falsification questions from `SKILL.md` apply, plus the section-specific questions below.

## Challenge pass: section-specific falsification questions

In addition to the standard four questions from `SKILL.md`, apply these to the Problem & user analysis:

- **Bubble check:** is this painpoint experienced primarily by people in the user's own demographic or professional bubble? Would the painpoint look different (or disappear) for users outside that bubble?
- **Frequency check:** is the painpoint actually frequent for the target user, or has its severity been confused with its frequency? An acute but rare painpoint produces a different product than a mild but constant one.
- **Workaround check:** are the workarounds described actually painful, or are they tolerable enough that users don't actively seek a better solution? "I do this manually" is not the same as "I would pay to avoid doing this manually."
- **Articulation check:** would the target user, in their own words, describe this as a painpoint? If the painpoint requires the user to first understand a framing they don't currently have, the demand may be lower than the analysis suggests.

Document the findings under the Challenge pass heading even if no changes were made to the analysis. If changes were made, note what changed and why.

## Depth calibration for this section

This section's analysis should produce ~400–600 words of substantive content (not counting headers or framework boilerplate). This is lighter than the general ~600–800 word check-in threshold from `SKILL.md` because section 01 characterizes the problem rather than analyzing markets or modeling outcomes — the foundational work is naturally less prose-heavy than the analytical sections.

Signs the section is too thin:
- Target user is described in one demographic dimension only (e.g., "Colombians" with no further specificity).
- Painpoint is characterized in a single sentence with no severity, frequency, or workaround analysis.
- Evidence section says "we believe" or "it seems" without categorizing the evidence type.

Signs the section is too thick:
- Multiple paragraphs on demographic segmentation when the segments don't actually affect the painpoint.
- Speculation about user motivations beyond what's needed to characterize the painpoint.
- Detailed competitive comparisons (those belong in section 02).

If the brief specifies a depth override for this section, honor it and acknowledge it at the top of the output.

## Downstream dependencies

What later sections will consume from section 01:

- **Section 02 (Market & competitive landscape)** will reference the target user characterization when sizing the SOM (market size depends on how the target user is defined — a narrow user definition produces a smaller SOM than a broad one).
- **Section 03 (Form factor & differentiation)** will reference the painpoint characterization when evaluating whether the idea is agent-shaped. The agent-fit verdict depends on properties of the painpoint (dialogue, multi-source synthesis, persistent context) that section 01 surfaces.
- **Section 05 (Business model)** will reference the painpoint severity and the workarounds analysis when evaluating monetization clarity. A painpoint without painful workarounds is structurally harder to monetize.
- **Section 07 (Investment & GTM)** will reference the target user definition when evaluating acquisition channels. Different user segments are reached through different channels.
- **Section 09 (Decision)** will reference the Problem severity score (with conviction label) when assembling the overall commercial score and applying the matrix.
