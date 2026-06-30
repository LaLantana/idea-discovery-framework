# Idea Discovery Framework — workspace & user guide

This is where your evaluations live, and the guide for running one. For *why* the framework is designed the way it is, see `design-notes.md`: this README is the how-to, design-notes is the why (they are different documents — design-notes does not replace this guide). For the skill internals, see the skill folder's README.

## What an evaluation produces

For each idea:

- A commercial score (0–10) with conviction
- A solo-buildability score (0–10) with conviction
- A form-factor recommendation (with the agent-fit verdict embedded)
- A matrix-driven decision (pursue immediately / pursue with partnership / pursue as learning project / kill)
- A final decision document with rationale, risks, and next steps

## What's in this folder

```
idea-discovery-workspace/
├── README.md                  ← this file (the how-to)
├── design-notes.md            ← design rationale + maintenance discipline (the why)
├── project-instructions.md    ← project configuration
├── idea-brief-template.md     ← fill this in to start an evaluation
└── projects/                  ← one folder per evaluated idea
```

The skill itself lives separately in `../SKILL-idea-discovery-framework/` and is installed into Claude. It is the reusable engine; this workspace is your data.

## How to start a new evaluation

1. **Fill in the brief.** Copy `idea-brief-template.md` and fill in every required field. The one-line description is mandatory — if you can't write the idea in one sentence, sharpen it first.
2. **Start a chat** in your Idea Discovery Claude project.
3. **Provide the brief** — paste it in, or attach the file.
4. **Confirm the folder name.** Claude derives a kebab-case folder name from the brief's Idea name field and confirms before creating `projects/[idea-name]/`.
5. **Run the framework.** Claude works through sections 01–09, saving each to the project folder as it goes. In autonomous mode (the default), it runs end-to-end and surfaces the complete project folder at the end; set `run mode: checkpoint` in the brief if you want it to pause after each section for review.

## How to revisit an evaluation

To re-evaluate the same idea with a modified brief, start a fresh chat with a new brief. The framework treats it as a new idea, not a re-scope of the prior one — prior evaluations are never re-scored. To re-read a past evaluation, open its files in `projects/[idea-name]/`.

## How to maintain the framework

When an evaluation surfaces a gap (an inconsistent anchor, a kill criterion that misfires), the skill files can be updated. The discipline — when to update, what to document, what not to do — is in `design-notes.md`. Mid-evaluation ad-hoc anchor changes are not maintenance; they are score manipulation. Real maintenance happens between evaluations and is tracked in design-notes.

## Where to look for what

| Question | File |
|----------|------|
| How do I start an evaluation? | this README |
| What does the skill measure? | `../SKILL-idea-discovery-framework/rubric.md` |
| What does Claude do at each step? | `../SKILL-idea-discovery-framework/SKILL.md` and the `templates/` folder (sections `01`–`09`) |
| Why is the framework designed this way? | `design-notes.md` |
| Where are my past evaluations? | `projects/[idea-name]/` |

## What to remember mid-evaluation

- The framework defaults to autonomous mode (Claude runs end-to-end). Checkpoint mode — Claude pauses after each section — is opt-in via the brief's run-mode field.
- Kill recommendations are conviction-gated: in autonomous mode a kill auto-confirms when it rests on solid (High/Medium-conviction) evidence and pauses for your confirmation only when it rests on thin (low-conviction) evidence; in checkpoint mode every kill pauses.
- The framework is expected to evolve — adding entries to `design-notes.md` as gaps surface is the intended workflow, not a sign something is broken.
