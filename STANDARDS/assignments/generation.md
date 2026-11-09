# Assignment Generation Standard

## Goal

Create assignments that produce meaningful practice, can be explained clearly, and can be assessed reliably without revealing the implementation.

## Design sequence

1. Identify current learning objectives and prerequisites.
2. Define observable behaviors that demonstrate each objective.
3. Decide what students must design versus what the instructor will provide.
4. Design assessment and autograder strategy before finalizing the prompt.
5. Identify likely shortcuts, hardcoding, file-name variation, compile failures, and cascading-failure risks.
6. Produce starter materials, public tests, README, rubric, and hidden-test plan as applicable.

## Prompt design

- State behavior, interfaces, constraints, required files, input, output, and submission expectations.
- Avoid line-by-line pseudocode when implementation is an objective.
- Use examples to clarify contracts without exposing the complete solution.
- Distinguish required behavior from suggested implementation.
- Define edge cases that are part of the specification.
- Require individual files rather than a student-created ZIP when that is the established submission workflow.

## Starter-code defaults

- Prefer minimal starter code and prototypes unless scaffolding is instructionally necessary.
- For harness-based tasks, instructor-supplied interface headers and student `.cpp` implementations may simplify grading.
- Starter packages should include per-function comments, a stdin-driven harness when appropriate, a subset of public tests, and local compile/run instructions.
- Avoid accidental newline characters inside C++ string literals; use `\n` or `std::endl`.

## Pipeline handoff

When the assignment will use Matthew's Assignment Pipeline, load the pipeline integration standard through `STANDARDS/autograders/INDEX.md`. Define the student files, instructor files, cases, rubric weights, filename tolerance, output strictness, numeric tolerances, timeout, memory checks, source-review policy, D2L metadata, review checkpoint, recovery implications, and tested pipeline release before packaging. Do not infer current pipeline configuration from an old assignment.

## Autograding-aware design

- Design independent tests to minimize cascading losses.
- Use varied multi-operation cases when that deters hardcoding without creating unnecessary dependencies.
- Keep expected input/output files in `cases/`; do not duplicate them in rubric configuration.
- Tolerate reasonable filename variation using established auto-discovery only when it does not create ambiguity.
- Preserve `clang++` where required for memory checks.
- Use strict-output mode only when extra output violates the learning target or contract.

## Alignment

Assignments must not require concepts removed from the current slides/module. If an assignment intentionally extends beyond direct instruction, label the extension and provide sufficient scaffolding.

## Deliverables

A completed assignment design should identify:

- objectives;
- student-facing specification;
- required submission files;
- starter/instructor files;
- public and hidden test strategy;
- rubric/weights;
- likely misconceptions;
- local validation steps;
- D2L grade-item/import implications;
- assumptions and TODOs.
