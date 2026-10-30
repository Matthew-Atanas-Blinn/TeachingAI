# Update Process

## Purpose

Turn useful discoveries into durable improvements without silently destabilizing the repository. The default is to correct the governing source of a problem before repairing dependent artifacts. Expedited artifact repair is available when delivery time makes that impractical.

## Standard workflow

1. **Identify the issue.** State the observed failure or opportunity in concrete terms.
2. **Diagnose the underlying cause.** Determine whether the problem originates in:
   - an artifact-specific implementation error;
   - an unclear, incomplete, or conflicting standard;
   - a course-level policy;
   - a module source of truth;
   - an interaction between multiple rules;
   - an unsupported assumption; or
   - a failure to follow an existing rule.
3. **Prefer an underlying correction.** By default, correct the governing source first and then regenerate or repair affected artifacts. This reduces repeated fixes and keeps future artifacts consistent.
4. **Classify the lesson.** Decide whether it belongs as:
   - a one-time artifact correction;
   - a reusable artifact standard;
   - a universal requirement;
   - a course-wide rule;
   - a module source-of-truth change;
   - an accepted rationale record; or
   - an experiment.
5. **Check existing authority.** Search for an existing rule before adding another. Prefer refining one authoritative rule over creating duplicates.
6. **Assess impact.** Identify affected generation guidance, review checklists, course/module files, decisions, references, and generated artifacts.
7. **Draft the change.** If not already approved, place experimental or uncertain revisions in `PROPOSED/`.
8. **Report all proposed changes.** Use the mandatory report format in `repository_rules.md`.
9. **Obtain approval.** No official standard becomes active without Matthew's approval.
10. **Apply consistently.** Update all approved dependencies in the same change set.
11. **Regenerate or repair affected artifacts.** Use the corrected governing source.
12. **Validate.** Check paths, links, contradictions, privacy, and whether the change is specific enough to guide action.
13. **Record.** Add an entry to `change_log.md`; add or update a decision record when the rationale is consequential.

## Expedited artifact-repair mode

Matthew may explicitly invoke expedited handling when a deliverable is time-sensitive. In expedited mode:

- fix the immediate artifact;
- do not silently modify official policy;
- record the suspected underlying issue;
- place an uncertain reusable change in `PROPOSED/` when appropriate;
- report that the governing issue remains unresolved; and
- return to the standard workflow when time permits.

Urgency does not waive privacy, safety, correctness of answer keys, or disclosure of known blockers.

## Recurring-problem invariant

```text
Problem -> Diagnose governing cause -> Correct governing source
        -> Regenerate/repair artifacts -> Review -> Future prevention
```

Expedited exception:

```text
Urgent problem -> Immediate artifact fix -> Record unresolved cause
               -> Later governing-source correction
```

Not every problem earns a rule. Promote it when recurrence is plausible, impact is significant, or the correction captures an important teaching principle.

## Required reporting invariant

Every modification attempt must report:

- every folder/file added;
- every folder/file modified;
- every folder/file moved or renamed;
- every folder/file deleted;
- the exact nature and rationale of each change;
- dependencies checked;
- assumptions or unresolved issues.

This applies even when Matthew explicitly asks for the modification. Approval to perform work does not waive reporting.

## Versioning

- Patch version: clarification or correction that does not change intended behavior.
- Minor version: new approved capability, standard, course file, or module.
- Major version: incompatible governance or hierarchy change.

`TODO`: Decide whether to maintain a machine-readable version file after the repository begins using automated tooling.
