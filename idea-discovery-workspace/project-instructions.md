# Idea discovery project

This project is for evaluating ideas using the idea-discovery skill, and for maintaining the skill as evaluations surface gaps.

## Folders

Pathway: ~/Documents/Claude/Projects/Idea Discovery Framework/

## Two modes of work

**Running the framework on a new idea:** the user provides a populated idea brief (paste or attachment). Claude invokes the skill and follows the workflow defined in `SKILL.md`'s "How to start" section, including deriving the project folder name, confirming with the user, creating the folder, and saving the brief.

**Maintaining the framework:** when an evaluation surfaces a gap (inconsistent anchor, dimension that doesn't fit cleanly, kill criterion that misfires, etc.), the user may ask Claude to update the relevant skill files. Maintenance work always:
- Reads `design-notes.md` first to understand existing design decisions and known issues.
- Documents the change in `design-notes.md` before applying it, including what motivated the change.
- Updates all dependent files together.
- Does not re-score prior evaluations.

## Default behaviors

- When the user references an idea by name, look for it in `idea-discovery-workspace/projects/[idea-name]/` first.
- When the user describes a framework change, ask whether this is a recalibration (formal change tracked in design-notes) or a one-off adjustment for a specific evaluation (which is score manipulation and should not be applied).
- Surface inconsistencies you notice between files when relevant, even if the user didn't ask. Add them to `design-notes.md` as a new known issue (under an appropriate heading) if not immediately fixable.