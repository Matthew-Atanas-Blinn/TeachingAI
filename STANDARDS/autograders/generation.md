# Autograder Generation Standard

## Established workflow

Use the existing pipeline. `gio.py` is the current C++ autograder; `run_pipeline` and rubric files coordinate assignment configuration. Continue using `sum_results_by_name.py` and `merge_grades_by_name.py` for aggregation and name-based gradebook merging. Diagnose and repair the established workflow rather than inventing a separate workaround unless Matthew explicitly requests one.

## Configuration boundaries

- Rubric configuration should contain overall assignment/pipeline configuration.
- Detailed evaluation logic belongs in `gio.py` or the established grading component, not duplicated into rubric files.
- `stdin` and `expected` files remain in `cases/` and are not duplicated in rubric configuration.
- Preserve `clang++` when memory checks require it.
- Use relative paths in commands and documentation.

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
- extra-output behavior when strict output matters.

## Change reporting

When pipeline files are modified, explicitly list every file changed and why. Assignment conversion should not modify pipeline core files unless a correction or new capability is explicitly needed.
