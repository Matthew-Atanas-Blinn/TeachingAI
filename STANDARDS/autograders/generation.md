# Autograder Generation Standard

## Established workflow

Use the existing pipeline. `run_pipeline.py` is the normal orchestrated path, `gio.py` owns low-level C++ grading, and rubric files provide supported assignment configuration. The current orchestrator performs normal multipart consolidation. Use `sum_results_by_name.py` only when the selected pipeline release documents an applicable legacy or general aggregation workflow. Use the pipeline's supported D2L merge path for name-based gradebook merging. Diagnose and repair the established workflow rather than inventing a separate workaround unless Matthew explicitly requests one.

For pipeline-dependent work, the selected Assignment Pipeline release and its current documentation govern operational details. Follow `assignment_pipeline_integration.md` and record the tested pipeline release.

## Configuration boundaries

- Rubric configuration should contain overall assignment/pipeline configuration.
- Shared check semantics and evaluation algorithms belong in `gio.py` or the established grading component. Assignment-specific selection and configuration of supported checks, points, tolerances, and derivation rules may belong in a part-level or otherwise supported detailed rubric when generated checks are insufficient.
- `stdin` and `expected` files remain in `cases/` and are not duplicated in rubric configuration.
- Preserve `clang++` when memory checks require it.
- Use relative paths in commands and documentation.

### Student-observable output formatting
- Do not deduct for output-format distinctions that students could not reasonably perceive or infer from the assignment materials.
- By default, ignore trailing horizontal whitespace, whitespace on otherwise empty lines, platform line endings, trailing blank lines, and the presence or absence of a final newline.
- Grade invisible whitespace exactly only when the distinction is visibly represented, explicitly defined, instructionally relevant, and demonstrated in student-facing material.
- Ordinary exact-output credit must use the selected pipeline release's student-visible canonical comparison. Raw-output matching requires a documented justification.

### Execution reliability
- A single timeout is not sufficient evidence for a deduction when the selected pipeline supports timeout confirmation.
- Require the timeout to be reproduced by the pipeline's retry behavior before it affects the score.
- A recovered timeout is diagnostic evidence, not a grading failure.
- Timeout status, captured output, failed-case status, and score must be internally consistent. Contradictory evidence requires review rather than a silent deduction.

## Test design

- Map every test to an objective and rubric value.
- Minimize cascading failures by testing operations independently where practical.
- Weight tests by educational importance, not implementation convenience.
- Include normal, boundary, invalid-input, state-transition, and integration cases as appropriate.
- Use multi-command stdin harnesses to exercise constructors, destructors, static state, and object interactions without requiring class methods to print.
- Deter hardcoding with varied hidden cases while keeping public tests understandable.
- Verify expected results independently.

## Compilation and file handling

- Support established student-file discovery options when filenames vary.
- Prefer instructor-provided headers and student implementation files where that improves reliability and matches the assignment design.
- Add compatibility shim headers only when they represent an intentional, documented tolerance.
- Flag HTML-escaped source and source files that `#include` `.cpp` files during preflight.
- Separate the student's `main` when the harness must supply its own entry point.

## Scoring and feedback

- Keep MaxPoints explicit and correctly scale results to the grade item.
- Make per-test or per-category points transparent.
- Use strict output only when extra output violates the contract.
- Apply filename penalties only according to the assignment's approved rule.
- Produce per-student feedback and aggregate failure summaries through the established output structure.
- Merge gradebook results by first and last name according to the established D2L workflow.

## Recovery compatibility

Automatic grading should make it possible to identify low-scoring submissions for manual recovery review. Recovery may raise but never lower the automatic score. Do not design tests so opaquely that an instructor cannot determine what the student understood.

## Validation set

Before release, test at least:

- a correct reference solution;
- a solution with each major isolated defect;
- a compile-error submission;
- a runtime-error or timeout case when relevant;
- a near-empty/starter-only submission;
- filename variations the assignment intends to tolerate;
- extra-output behavior when strict output matters;
- a correct trailing-whitespace and line-ending variant;
- a correct final-newline variant;
- a correct alternate-control-flow implementation;
- transient-timeout recovery when supported by the selected pipeline;
- a confirmed timeout or infinite-loop submission; and
- a visibly wrong output that must remain distinguishable after canonicalization.

Use only synthetic names and identifiers in reusable validation fixtures. Do not derive fixture labels from real students or incidents.

## Change reporting

When pipeline files are modified, explicitly list every file changed and why. Assignment conversion should not modify pipeline core files unless a correction or new capability is explicitly needed.
