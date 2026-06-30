# Idea brief: [IDEA NAME]

This file is the kickoff document for a discovery evaluation. Populate every field before running the discovery skill. Fields marked OPTIONAL can be left blank; all others must be filled.

When populated, save this file as `00-brief.md` inside the idea's project folder (e.g., `idea-discovery-workspace/projects/[idea-name]/00-brief.md`). The discovery skill reads this file first and uses it to configure the analysis.

---

## Idea

**Idea name:**
[A short name for the idea — used to derive the project folder name in kebab-case, e.g., "Fandango Colombia" → `fandango-colombia`.]

**One-line description:**
[A single sentence describing the idea. If you can't write it in one sentence, the idea isn't sharp enough yet — clarify before proceeding.]

**Longer description (OPTIONAL):**
[2–4 sentences expanding on the one-liner, if useful context isn't captured by the one-line description alone.]

---

## Target market

**Primary market:**
[Country or region the idea is initially targeted at. Examples: "Colombia", "Italy and Colombia", "open — recommend".]

**Why this market:**
[Why is this the natural starting point? Painpoint observation, personal network, language, regulatory environment, existing relationships, market gap. One paragraph.]

**Market expansion question:**
[Choose one:
- "This market only" — evaluate the primary market; do not consider expansion.
- "Primary plus suggest 2–3 expansion candidates" — evaluate the primary market in depth, then suggest the next 2–3 markets that fit.
- "Open search" — primary market is unclear or geography-agnostic; find the best starting market for this idea.]

---

## Solution hypothesis

**Form factor (initial hypothesis):**
[Choose one:
- A specific form factor, e.g., "agent", "web app", "mobile app", "browser extension", "marketplace", "internal tool". This will be acknowledged and actively challenged in framework section 03.
- "Evaluate form factor as part of analysis" — explicitly defer the form factor decision to section 03. Use this if you genuinely don't know what shape this should be.]

**Why this form factor (if specified):**
[One paragraph on why you think this is the right shape. Will not be taken as justification; the verdict in section 03 is independent. But explains your starting hypothesis.]

---

## Commercial threshold

**Make-money threshold:**
[The minimum revenue this idea would need to produce to be worth pursuing. Used by the rubric's market size dimension anchor (see `rubric.md`). Suggested format: "$X ARR by year 3" or "$Y annual gross revenue by year N". This is your threshold for "worth the time."]

**Why this threshold (OPTIONAL):**
[One sentence on what this threshold represents — opportunity cost of your time, lifestyle target, scale needed to justify the effort, etc. Helps Claude apply the threshold sensibly when SOM estimates are uncertain.]

**Runway / available capital (OPTIONAL):**
[How much out-of-pocket capital you can put into this idea before it needs to sustain itself — the ceiling sections 07 and 08 check the initial investment and the cumulative capital required against. Suggested format: "$X total" or "$Y over N months." Leave blank if you'd rather just see the capital the idea requires — sections 07/08 will report it and note that no runway ceiling was given.]

---

## Learning value (OPTIONAL)

**Skill areas you actively want to build:**
[Examples: "building AI agents", "full-stack development", "data engineering", "B2B sales motion", "regulated industries", "marketplace dynamics". Leave blank if there's no specific learning agenda for this idea.]

**Why this matters:**
[This field activates the "learning project" exception in the rubric's matrix (low commercial / high solo-buildability quadrant). Without a stated learning interest in the relevant skill area, the default for that quadrant is kill with no exception. Be specific — "I want to learn agents" enables the exception only for genuinely agent-shaped ideas.]

---

## Context

**Relevant prior knowledge:**
[What do you already know about this space? Have you used the existing solutions? Do you have relationships with target users? Have you observed the painpoint directly or heard about it secondhand? One paragraph.]

**Why now (OPTIONAL):**
[Is there a timing factor — new technology, regulatory change, shift in user behavior, competitor failure — that makes this a better idea today than it would have been two years ago? Or is this a timeless painpoint? One paragraph.]

---

## Run configuration

**Run mode:**
[Choose one — leave blank to use the default (Autonomous):
- "Autonomous" (default) — Claude runs end-to-end without intermediate pauses, surfacing the complete populated project folder at the end. Kills are conviction-gated: they auto-confirm on solid (High/Medium-conviction) evidence and escalate to you only when they rest on thin (low-conviction) evidence; the high-commercial / weak-financial contradiction at section 09 always pauses.
- "Checkpoint" — Claude pauses after every section for your review before proceeding, and every kill pauses. Use this when you want to watch the framework work step by step.]

**Depth overrides (OPTIONAL):**
[Any section-specific depth instructions. Examples:
- "Go deeper on regulatory analysis — fintech compliance is the main risk."
- "Skip detailed competitive analysis on the Italian market; I know it well, just confirm the picture."
- "Spend more time on solo-buildability — I want a realistic plan, not just a score."

Leave blank to use the rubric's default depth heuristics. Overrides are acknowledged at the top of the relevant section's output.]

**Other instructions (OPTIONAL):**
[Anything else that affects how this idea should be evaluated but doesn't fit the fields above. Examples:
- "I have an existing relationship with [specific potential partner] — factor that into the solo-buildability assessment."
- "Do not consider partnership strategies that require external capital."
- "This is a follow-up to [prior idea name] — reference that evaluation for context."]

---

## Sign-off

**Brief completed by:** [Your name or initials]
**Date:** [YYYY-MM-DD]
**Brief version:** [If you revise the brief mid-evaluation, increment this. v1 for initial.]