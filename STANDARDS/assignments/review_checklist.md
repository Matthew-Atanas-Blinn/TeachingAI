# Assignment Review Checklist

## Alignment

- [ ] Every required behavior maps to a current objective.
- [ ] Required prerequisites were taught.
- [ ] Outdated or removed topics are absent.
- [ ] Difficulty and scope fit the available student time.

## Specification quality

- [ ] Required files and names are clear.
- [ ] Inputs, outputs, interfaces, constraints, and edge cases are defined.
- [ ] Examples agree with the rules.
- [ ] Required versus suggested implementation is distinguishable.
- [ ] No line-by-line solution is inadvertently revealed.
- [ ] Submission instructions match the actual D2L workflow.

## Starter materials

- [ ] Starter code compiles or has clearly marked intentional gaps.
- [ ] Instructor files do not expose hidden solutions.
- [ ] Public tests demonstrate the workflow without covering all hidden cases.
- [ ] README commands work in the supported environment.
- [ ] String literals and file encodings are valid.

## Assessment design

- [ ] Test categories correspond to rubric categories.
- [ ] One defect does not unnecessarily destroy unrelated credit.
- [ ] Hardcoding and filename variation have been considered.
- [ ] Compile, runtime, timeout, output, and memory failures are handled.
- [ ] Expected outputs were independently verified.
- [ ] Recovery grading is possible when automatic scoring is too low to reflect demonstrated understanding.

## Pipeline compatibility
- [ ] If the assignment uses Matthew's Assignment Pipeline, the exact tested release is recorded.
- [ ] Configuration fields and commands are supported by that release.
- [ ] The assignment-to-pipeline handoff is complete and unresolved compatibility gaps are reported.
- [ ] Shared pipeline files were not changed for an assignment-specific need.

## Package preflight

- [ ] All referenced files exist.
- [ ] Case manifests point to the correct `stdin` and `expected` files.
- [ ] No case file is duplicated improperly into rubric configuration.
- [ ] Paths and commands are relative and match the supported shell.
- [ ] Package was test-run against correct, common-defect, compile-error, and near-empty submissions.

## Report

- [ ] All files added or changed are listed.
- [ ] Known limitations and assumptions are disclosed.
- [ ] Student-facing and instructor-only materials are clearly separated.


## Correction and regression loop

- [ ] Correct every blocker and major issue, then rebuild the package.
- [ ] Recheck all modified files and dependent instructions, tests, rubrics, and commands.
- [ ] Rerun package preflight and the regression submission set.
- [ ] Repeat until no blockers or majors remain, subject to three complete automated review cycles by default.
- [ ] Report unresolved issues if the cap is reached; do not label the package ready unless Matthew explicitly accepts expedited delivery.
