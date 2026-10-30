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
9. **Keep authoritative rules singular.** Avoid copying the same normative rule into many files. Cross-reference the authoritative location and put task-specific checks in the applicable checklist.
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
