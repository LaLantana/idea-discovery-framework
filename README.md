# Idea Discovery Framework

A structured framework for evaluating product ideas for commercial viability and solo-buildability. It runs as a Claude skill over a nine-section analysis, scores the idea against a consistent rubric, and produces a kill/proceed decision with explicit, reviewable reasoning.

This repository has two parts.

## 1. `SKILL-idea-discovery-framework/` — the skill (the portable engine)

The reusable analysis engine: `SKILL.md` (process), `rubric.md` (scoring), `user-profile.md` (the builder's capability profile used in the solo-buildability section), and the `templates/` folder (the nine section prompts, `01`–`09`). This folder is what you install into Claude.

## 2. `idea-discovery-workspace/` — the workspace (your data)

Where evaluations live. Contains `idea-brief-template.md` (the kickoff brief you fill in), `project-instructions.md` (project configuration), `design-notes.md` (the maintainer's design rationale and change log), and `projects/` (one folder per evaluated idea). This is personal data, not part of the skill: the skill reads your brief and reads and writes the `projects/` folder during a run, while `design-notes.md` is maintainer-only and is not read while the skill runs.

## Setup

1. **Install the skill.** Upload the `SKILL-idea-discovery-framework/` folder to Claude (in Cowork: Customize → Skills; or place it in your Claude Code skills directory).
2. **Set up the workspace.** Keep `idea-discovery-workspace/` somewhere you'll work from. Edit `user-profile.md` in the skill to reflect whoever is building — it is calibrated to one user by default.
3. **Run an evaluation.** See `idea-discovery-workspace/README.md` for the step-by-step.

## How the two fit together

The skill is portable and shareable; the workspace is yours. The skill reads your filled-in brief, then writes each section's analysis into `idea-discovery-workspace/projects/[idea-name]/`. Design rationale and maintenance discipline live in `idea-discovery-workspace/design-notes.md` — read it before changing rubric anchors, the kill model, or templates.
