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

## Repository output verification gate

Before reporting that a repository update is complete, verify the actual output against the approved change set. Intended changes are not evidence that the final files contain those changes.

### 1. Inspect the final changed-file inventory

Run the following commands from the repository root:

    git status --short
    git diff --name-status
    git diff --check

If changes have already been staged, also run:

    git diff --cached --name-status
    git diff --cached --check

Compare the resulting inventory against the approved Repository Change Report.

### 2. Verify every expected modification

For every file listed as modified in the approved report:

- confirm that the file appears in `git status --short`, `git diff --name-status`, or `git diff --cached --name-status`;
- inspect the relevant diff;
- confirm that the intended content is present;
- confirm that no required section was omitted; and
- do not report the file as modified if the actual working tree contains no modification.

A generation script that attempted to modify a file does not prove that the resulting file differs from the repository version.

### 3. Verify every expected addition

For every added folder or file:

- confirm that the path exists;
- confirm that each new folder contains its required `INDEX.md`;
- confirm that the nearest owning index routes to the new content;
- confirm that the addition appears as untracked or staged before commit; and
- inspect the complete contents of each added file.

### 4. Verify required metadata updates

When a repository version changes, inspect every current-version authority individually.

At minimum, verify:

- the version heading in the root `INDEX.md`;
- the current-version statement in `README.md`;
- the corresponding entry in `META/change_log.md`; and
- any machine-readable version file if one is later adopted.

Do not rely on replacing only one occurrence of the previous version. Search for all current-version declarations and distinguish them from legitimate historical references.

Suggested checks:

    grep -RniE 'TeachingAI Repository v[0-9]+\.[0-9]+\.[0-9]+|Version [0-9]+\.[0-9]+\.[0-9]+' \
        INDEX.md README.md META

Historical references to earlier versions should remain unchanged when they describe earlier repository behavior.

### 5. Verify the change log

Confirm that `META/change_log.md` contains the approved entry.

Then confirm that the file appears in the changed-file inventory if the entry is newly added or revised.

Use:

    git diff -- META/change_log.md
    git diff --cached -- META/change_log.md

If the file does not appear in Git's inventory, do not claim that the change log was modified.

### 6. Validate format-specific reference artifacts

When a generated artifact depends on an import format, inspect a previously imported artifact that is known to work before generating the new artifact.

For a D2L quiz CSV containing code:

- use an approved, successfully imported D2L CSV as the structural reference;
- do not substitute Markdown syntax for HTML merely because both can visually represent code elsewhere;
- store formatted HTML in the question or option text field;
- place `HTML` in the format field required by the D2L CSV record;
- escape HTML-sensitive code characters;
- preserve indentation with `white-space: pre-wrap`;
- verify question stems and answer choices separately; and
- perform a test import when practical.

A structurally valid CSV is not sufficient if D2L renders formatting syntax as literal student-visible text.

### 7. Validate D2L HTML code blocks

Use this established structure for a question containing a code block:

    QuestionText,"<p>Question text</p><div style=""font-family: Consolas, &quot;Courier New&quot;, monospace; white-space: pre-wrap; background-color: #f5f5f5; border: 1px solid #cccccc; padding: 10px; margin-top: 8px;"">int value = 11;
    int* p = &amp;value;
    p = nullptr;</div>",HTML

Use the same styled `<div>` structure for an answer choice that consists of code:

    Option,100,"<div style=""font-family: Consolas, &quot;Courier New&quot;, monospace; white-space: pre-wrap; background-color: #f5f5f5; border: 1px solid #cccccc; padding: 10px; margin-top: 8px;"">double area(double length, double width);</div>",HTML

At minimum, escape:

- `&` as `&amp;`;
- `<` as `&lt;`;
- `>` as `&gt;`; and
- embedded HTML attribute quotation marks according to CSV quoting rules.

Do not use Markdown triple-backtick fences in a D2L CSV unless a verified import test demonstrates that D2L renders them rather than displaying them literally.

### 8. Inspect the packaged output

If the repository is delivered as an archive:

- list the archive contents;
- verify that all expected files are present;
- extract the archive into a temporary directory;
- compare the extracted files against the approved change list;
- verify that the archive contains no unintended temporary or duplicate files; and
- run the repository validation checks against the extracted copy.

### 9. Check for omissions and unexpected changes

Treat either of the following as a failed validation:

- an approved change is absent from the final output; or
- an unreported file is added, modified, moved, renamed, or deleted.

Resolve the discrepancy before reporting completion.

### 10. Report only the verified result

The final Repository Change Report must reflect the actual changed-file inventory, not the intended inventory or a script's planned operations.

A repository update is not complete until the following agree:

- the approved change plan;
- the final file contents;
- `git status --short`;
- `git diff --name-status`;
- `git diff --check`;
- the repository version declarations;
- `META/change_log.md`;
- the packaged output, when applicable; and
- the final Repository Change Report.

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

## Hierarchical index update procedure

For every added, moved, renamed, or deleted file or folder:

1. identify the nearest governing `INDEX.md`;
2. update that index if its immediate child set or routing description changed;
3. do not propagate descendant listings into ancestor indexes;
4. create an `INDEX.md` inside every new folder, even if it initially instructs the reader to inspect all folder contents; and
5. verify that no lower-level file was given a defensive backward pointer into the rules or decisions hierarchy.

During validation:

- verify that every non-`.git` repository folder contains `INDEX.md`;
- verify that every path named by an index exists;
- verify that each immediate child requiring routing appears in the nearest index;
- verify that indexes do not recursively catalog content owned by lower indexes;
- verify that loading instructions do not create cycles;
- verify that global standards are selected before artifact-specific standards; and
- verify that applicability triggers are specific enough to avoid unrelated context loading.

Navigation guidance belongs in the nearest applicable `INDEX.md`. Substantive rules do not belong in indexes.
