# Idea Discovery Framework

A Claude skill that runs a pre-evaluation of a potential problem: whether, and how, a business might solve it. Version 3 follows the double diamond. It researches the problem space, defines the problem worth solving, generates and screens ideas, then evaluates up to three of them against a consistent rubric and ends in a verdict per idea.

## What's in this repository

Everything lives in `SKILL-idea-discovery-framework-v3/`, the folder you install into Claude.

| File | Role |
|------|------|
| `SKILL.md` | The process: how to start, run modes, section flow, standing habits, and the decision and re-run protocols. |
| `rubric.md` | The measurement: the scored dimensions, their anchors, and how section 13 assembles scores into a verdict. |
| `user-profile.md` | The builder's capability profile, used by section 10 (solo-buildability). Calibrated to one user. Edit it for a different builder. |
| `templates/` | One template per section, `00-entry-template.md` through `14-summary.md`. |

## The sections

| # | Section | Position |
|---|---|---|
| 00 | Entry (written by the founder) | Entry point |
| 01 | Discover | 1st diamond, diverge |
| 02 | Define | 1st diamond, converge |
| 03 | Brief (written by 02) | Midpoint |
| 04 | Ideation | 2nd diamond, diverge |
| 05 | Screen | 2nd diamond, light evaluation |
| 06–12 | Evaluation, one subfolder per selected idea | 2nd diamond, evaluation |
| 13 | Decision | Exit point |
| 14 | Run summary | After the exit point |

A run writes its files to `idea-discovery-workspace/projects/<problem-name>/`, with each selected idea's 06–12 in `ideas/<idea-name>/`. The workspace is your data and is not part of this repository.

## Setup

1. **Install the skill.** Upload `SKILL-idea-discovery-framework-v3/` to Claude (in Cowork: Customize → Skills; or place it in your Claude Code skills directory).
2. **Adjust the profile.** Edit `user-profile.md` to reflect whoever is building.
3. **Write an entry.** Copy `templates/00-entry-template.md`, fill it in with a potential problem (not a solution), and save it as `00-entry.md`.
4. **Run it.** Ask Claude explicitly to run the framework on your entry, for example "run idea discovery on this". The skill does not start on exploratory questions or brainstorming.

## License

MIT. See `LICENSE`.
