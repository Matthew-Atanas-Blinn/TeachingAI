# Assignment Pipeline Integration Standard

## Purpose and scope

The C++ Assignment Grading Pipeline is Matthew Atanas's reference implementation for grading assignments in COSC 1436, COSC 1437, and COSC 2436. It remains a separate software repository from TeachingAI.

TeachingAI governs instructional alignment, assignment and assessment design, privacy, evidence requirements, review expectations, and recovery grading. The Assignment Pipeline governs its executable behavior, supported configuration, commands, generated outputs, software architecture, and release compatibility.

The trigger for loading this file is defined in `STANDARDS/autograders/INDEX.md`. This file defines the integration contract after the index selects it; it does not define its own routing trigger.

## Authority boundary

For pipeline-dependent assignment work:

- TeachingAI is authoritative for what the assignment should teach and assess, how evidence should be isolated and weighted, what review is required, and which privacy and fairness requirements apply.
- The assignment specification and instructor-provided starter files are authoritative for the student contract.
- The selected Assignment Pipeline release, its current `AI_CONTEXT.md`, `README.md`, configuration documentation, and executable source are authoritative for supported operational behavior.
- TeachingAI must not duplicate or silently redefine the pipeline's complete configuration schema, command behavior, diagnostic layout, component ownership, or implementation details.
- When TeachingAI requires a capability that the selected pipeline release does not support, report the compatibility gap. Do not invent a parallel grading workflow unless Matthew explicitly approves one.

## Required assignment-to-pipeline handoff

Before packaging or converting an assignment for the pipeline, identify:

- course, module, learning objectives, and prerequisites;
- observable behaviors that provide evidence for each objective;
- required student files and accepted filename tolerances;
- instructor-provided headers, harness code, starter files, and support files;
- public and hidden case strategy;
- authoritative stdin and expected-output files;
- test categories, points, and independence expectations;
- output strictness, numeric tolerances, timeouts, and memory-check requirements;
- hardcoding or source-review policy, including whether a finding is automatic or review-only;
- D2L grade-item metadata and name-based merge expectations;
- human-review checkpoint and recovery-review implications; and
- unresolved assumptions or unsupported requirements.

Do not generate pipeline configuration until the assignment contract and grading evidence are sufficiently defined to resolve these items.

## Compatibility procedure

For every pipeline-dependent assignment package:

1. Identify the exact Assignment Pipeline release being used.
2. Read the pipeline repository's current `AI_CONTEXT.md` and the relevant parts of `README.md`.
3. Inspect current source when modifying or relying on implementation behavior not fully established by the documentation.
4. Use only configuration fields and commands supported by that release.
5. Record the tested pipeline release in the assignment delivery report or package documentation.
6. Test the complete package with the required regression submissions before production use.
7. Report any mismatch between TeachingAI requirements, assignment needs, and implemented pipeline capabilities.

Do not infer current schema or command behavior from an old assignment package or from TeachingAI summaries.

## Configuration and implementation boundaries

- The root `rubric.json` contains assignment-wide configuration and defaults.
- A part-level or otherwise supported detailed rubric may select and configure native checks, points, tolerances, or derivation rules when generated checks are insufficient.
- Shared check types, evaluation algorithms, compilation, execution, timeout handling, sanitizer behavior, and detailed feedback semantics belong in the pipeline implementation, primarily `gio.py` or the component that owns that behavior.
- Raw `stdinX.txt` and `expectedX.txt` data remain in `cases/` unless duplication has a specific documented purpose.
- `run_pipeline.py` remains the normal orchestrated path. Legacy or general utilities are used only when the current pipeline documentation identifies an applicable need.
- Assignment conversion normally changes assignment-specific files only. Shared pipeline files change only for a shared defect or an explicitly approved capability.

## Evidence and review contract

Pipeline use does not replace human review. Before D2L import:

- review `results/grades_review.csv`;
- trace every deduction to detailed evidence;
- investigate compile failures, missing or renamed files, timeouts, sanitizer findings, hardcoding findings, name mismatches, and unusual scores;
- stop when required assignment material or student evidence is inaccessible rather than treating it as absent;
- verify late penalties and score scaling when configured; and
- apply the TeachingAI recovery-grading standard when an automatic score may understate demonstrated understanding.

A successful pipeline run is not proof that grades are correct.

## Privacy boundary

Do not commit student submissions, names, identifiers, grade exports, result files, feedback tied to real students, or other education records to TeachingAI or a public Assignment Pipeline repository. Real student data belongs only in the institutionally approved grading workspace.

## Cross-repository maintenance

When TeachingAI changes a requirement that affects pipeline-dependent assignments, check whether the pipeline already supports it. Update TeachingAI when the requirement or integration contract changes. Update the Assignment Pipeline only when executable behavior, software documentation, or compatibility metadata must change.

When the Assignment Pipeline changes configuration semantics, commands, outputs, responsibility boundaries, or compatibility, update its own documentation and compatibility declaration. Update TeachingAI only if the stable integration contract or TeachingAI guidance becomes inaccurate.
