# Idea Discovery Skill

The portable engine of the Idea Discovery Framework. It evaluates a product idea across nine analytical sections and produces a kill/proceed decision plotted on a commercial × solo-buildability matrix.

This README is for someone **installing or maintaining the skill**. To *run* an evaluation, see the workspace guide at `../idea-discovery-workspace/README.md`.

## What's in this folder

| File | Role |
|------|------|
| `SKILL.md` | The process: how to start, run modes, standing habits, the nine-section flow, the kill model, and the deep-research and downstream standing protocols. |
| `rubric.md` | The measurement: the three scores, the four commercial dimensions and their anchors, the veto-and-arithmetic-average scoring, the 2×2 matrix, the consolidated kill model, and calibration discipline. |
| `user-profile.md` | The builder's capability profile, used by section 06 (solo-buildability). Calibrated to one user — edit it for a different builder. |
| `templates/` (`01`–`09`) | The nine section-by-section analytical prompts, `01-problem-and-user.md` through `09-decision.md`. One per framework section. |

## Installing

Upload this folder to Claude as a skill (in Cowork: Customize → Skills; or place it in your Claude Code skills directory). The skill triggers on requests to "run discovery on" or "evaluate" an idea, or to work through an `00-brief.md`.

## Customizing for a different user

`user-profile.md` is the single calibration point for who is building. The solo-buildability anchors in `rubric.md` are also tuned to one user's skill level — read the workspace `design-notes.md` for the recalibration discipline before changing anchors.

## Maintaining the framework

Design rationale, the record of deliberate changes, and the maintenance discipline live in `../idea-discovery-workspace/design-notes.md` (kept in the workspace because it is maintainer-only and not read while the skill runs). Read it before changing rubric anchors, the kill model, or templates: changes must be applied across dependent files together, and prior evaluations are never re-scored.
