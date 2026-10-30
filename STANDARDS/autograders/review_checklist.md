# Autograder Review Checklist

## Workflow integrity

- [ ] Uses the established `run_pipeline`/rubric/`gio.py` workflow.
- [ ] No parallel workaround was introduced without explicit request.
- [ ] Rubric configuration contains only appropriate overall configuration.
- [ ] Detailed grading behavior remains in the established grading component.
- [ ] `cases/` owns stdin/expected data without improper duplication.
- [ ] Required compiler and memory-check behavior are preserved.

## Coverage and independence

- [ ] Every objective maps to one or more tests.
- [ ] Test weights sum correctly.
- [ ] One failure does not unnecessarily eliminate unrelated credit.
- [ ] Normal, boundary, and relevant invalid/state cases are present.
- [ ] Hidden cases discourage hardcoding.
- [ ] Expected outputs and calculations were independently verified.

## Build and file discovery

- [ ] Correct submission files are found under realistic D2L folder names.
- [ ] Multiple files in one part are handled by the existing workflow.
- [ ] Student `main` is excluded when the harness owns `main`.
- [ ] Include directories and instructor files are correct.
- [ ] HTML escapes and `.cpp` includes are preflighted where applicable.
- [ ] Commands use relative paths and work in the supported environment.

## Failure handling

- [ ] Compile errors receive clear feedback.
- [ ] Runtime errors and timeouts are bounded and reported.
- [ ] Memory failures are captured when required.
- [ ] Extra output behavior matches strict/non-strict policy.
- [ ] Near-empty and starter-only submissions score appropriately.

## Output and merging

- [ ] MaxPoints and scaling are correct.
- [ ] Per-category feedback is understandable.
- [ ] Per-student and aggregate feedback files are produced.
- [ ] Name parsing matches D2L submission folders.
- [ ] Gradebook merge uses first/last name and a copy of the original CSV.
- [ ] No student is treated as missing when a required file/export is inaccessible without first stopping for clarification.

## Regression set

- [ ] Reference solution earns full credit.
- [ ] Each prepared defect loses primarily its intended points.
- [ ] Score totals and feedback agree.
- [ ] Re-running is deterministic where expected.
- [ ] All changed pipeline/package files are listed in the delivery report.


## Correction and regression loop

- [ ] Correct every blocker and major issue in the authoritative package or pipeline source.
- [ ] Rerun the full regression set after any scoring, discovery, compilation, or output-handling change.
- [ ] Recheck changed tests plus dependent totals, feedback, and gradebook output.
- [ ] Repeat until no blockers or majors remain, subject to three complete automated review cycles by default.
- [ ] If the cap is reached, report unresolved issues and do not label the grader ready for production use.
