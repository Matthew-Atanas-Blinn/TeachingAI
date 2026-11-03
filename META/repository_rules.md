# Repository Rules

## Mandatory invariants

1. **Report every repository change.** List every folder or file added, modified, moved, renamed, or deleted. For each, state what changed and why.
2. **No silent policy changes.** An official rule does not become active until Matthew approves it.
3. **Do not invent missing policy.** Mark assumptions and TODOs; ask only when the ambiguity materially affects the result.
4. **Keep experiments separate.** Unapproved behavior belongs in `PROPOSED/` and is inactive unless explicitly enabled.
5. **Protect privacy.** Never store student-identifying information, submissions, grades, or case-specific student feedback in this repository.
6. **Preserve established workflows.** Improve the current workflow rather than creating a parallel workaround unless Matthew explicitly requests one.
7. **Maintain internal consistency.** Update dependent references, checklists, index entries, and decision records when an approved change requires them.
8. **Use plain, portable formats.** Prefer Markdown and other vendor-neutral text formats.
9. **Keep authoritative rules singular.** Avoid copying the same normative rule into many files. The index and authority hierarchy must activate the governing rule before lower-level work begins. Lower-level files may add task-specific implementation details or verification checks, but must not repeat the governing rule or point backward to recover skipped authority.
10. **Separate durable knowledge from artifacts.** This repository stores standards and source-of-truth material, not routine generated decks, student work, grade exports, or temporary schedules.

## Required change report format

```text
Repository Change Report

Status: Proposed | Applied with approval | Experimental only

Added:
- path
  - What was added
  - Why

Modified:
- path
  - What changed
  - Why

Moved/Renamed:
- old path -> new path
  - Why

Deleted:
- path
  - What was removed
  - Why

Dependencies checked:
- references, checklists, indexes, decisions, or artifacts examined

Assumptions/TODOs:
- item
```

Use `None` under categories with no entries. A summary such as “updated several files” is not sufficient.

## Writing rules

- Use direct, testable language: `must`, `should`, or `may` deliberately.
- Put rationale near the rule or link to an accepted decision record.
- Include examples when they clarify application, but do not let an example narrow a general rule accidentally.
- Distinguish requirements from preferences and defaults.
- Date accepted changes in ISO format (`YYYY-MM-DD`).

## Hierarchical navigation invariants

11. **Follow indexes from the top down.** Begin with the root `INDEX.md`. Whenever a selected folder contains an `INDEX.md`, read it before selecting lower-level files.
12. **Index every folder.** Every repository folder must contain an `INDEX.md`, even when the index is only a stub instructing the reader to inspect all current contents.
13. **Keep indexes local.** An index routes only through its immediate folder. Do not recursively catalog descendants owned by a lower index.
14. **Load the smallest sufficient branch.** Do not read sibling branches unless comparison, reuse, or dependency checking requires them.
15. **Do not add lower-level backward pointers into the rules or decisions tree.** Governing upper-level context must already be active through index traversal. Correct routing or governance when that is unreliable.
16. **Maintain the nearest index.** Adding, moving, renaming, or deleting an immediate child requires updating that folder's `INDEX.md` in the same change set. Do not update ancestor indexes for changes fully contained below an already indexed child.
17. **Keep indexes as routers.** Substantive standards, structures, and rationale belong in separately named files; indexes identify when those files should be read.
18. **Keep cross-artifact standards global.** Operational rules spanning multiple artifact types belong in `STANDARDS/global/`, not arbitrarily under one artifact branch.
