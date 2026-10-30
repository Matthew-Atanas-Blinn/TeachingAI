# TeachingAI Repository v1.1.0

## Purpose

TeachingAI is an AI-independent repository of durable teaching standards, course architecture, assessment practices, grading rules, review procedures, and pedagogical rationale. It converts knowledge that would otherwise remain scattered across memory, conversations, and one-time corrections into reusable institutional knowledge.

The repository is intended to improve student learning while making course development more consistent, transparent, portable, and sustainable. It should be useful to a human collaborator or any future AI system, not only the system that created it.

## Operating philosophy

- Store durable and reusable knowledge, not temporary task notes.
- Prefer principles that prevent classes of problems over isolated corrections.
- Preserve the reason for consequential decisions.
- Separate established standards from experiments.
- Treat generated materials as drafts until the required review is complete.
- Optimize educational value per unit of instructor time without sacrificing correctness, accessibility, privacy, or assessment fairness.
- Use AI to accelerate drafting, checking, comparison, and revision. The instructor remains responsible for final instructional and grading decisions.

## Authority and precedence

Apply relevant files in this order unless an explicitly enabled experiment says otherwise:

1. Applicable legal, privacy, safety, and institutional requirements, as operationalized by `REQUIRED/` and any institution-provided policy files supplied with the task. Do not independently research every possible requirement for every task. Perform external verification only when a material compliance question exists, the local guidance is incomplete or potentially outdated, institution-specific authorization is unknown, or Matthew explicitly requests verification.
2. `REQUIRED/` universal principles.
3. Approved `STANDARDS/` for the artifact being produced.
4. Relevant `COURSES/` constraints.
5. Relevant `MODULES/` source-of-truth documents.
6. Explicit instructions for the current task.
7. Explicitly enabled `PROPOSED/` overrides.

A lower-level file may specialize a higher-level rule, but it must not silently contradict it. Conflicts must be reported before proceeding. Privacy and safety rules cannot be overridden by experiments.

## Folder guide

- `META/`: governance for the repository itself, including its philosophy, update rules, experimentation rules, and change history.
- `REQUIRED/`: universal requirements that should be read for every substantive task.
- `STANDARDS/`: how recurring artifacts are generated and reviewed.
- `COURSES/`: course-wide constraints and durable design decisions for Programming Fundamentals I, II, and III.
- `MODULES/`: topic-specific source-of-truth documents. Read only the module relevant to the current task.
- `DECISIONS/`: accepted architecture-decision records explaining important choices and alternatives.
- `PROPOSED/`: experimental rules or changes that are not official standards.

## Files to read

### Always read

- `META/repository_rules.md`
- `REQUIRED/pedagogy.md`
- `REQUIRED/accessibility.md`
- `REQUIRED/data_privacy.md`

### Read when changing this repository

- `META/repository_philosophy.md`
- `META/update_process.md`
- `META/experimentation.md`
- `META/change_log.md`

### Read by task

- Slides: `STANDARDS/slides/generation.md` and `STANDARDS/slides/review_checklist.md`
- Quizzes: `STANDARDS/quizzes/generation.md` and `STANDARDS/quizzes/review_checklist.md`
- Assignments: `STANDARDS/assignments/generation.md` and `STANDARDS/assignments/review_checklist.md`
- Autograders: `STANDARDS/autograders/generation.md` and `STANDARDS/autograders/review_checklist.md`
- Recovery grading: `STANDARDS/grading/recovery_grading.md`
- Course-specific work: the relevant file in `COURSES/`
- Module-specific work: the relevant folder in `MODULES/`

## Information flow

```text
REQUIRED universal constraints
          |
          v
STANDARDS for the artifact + COURSES constraints
          |
          v
MODULE source of truth + current task requirements
          |
          v
Generate slides / quizzes / assignments / autograders
          |
          v
Review with artifact checklist and module checklist
          |
          v
Instructor accepts or requests changes
          |
          v
Recurring issue? -> Fix immediate artifact
                 -> Draft reusable change in PROPOSED
                 -> Test explicitly
                 -> Accept into repository or reject
                 -> Record accepted rationale and change log
```

## Updating the repository

All changes must follow `META/update_process.md`. Every change must be reported with every file and folder added, modified, moved, renamed, or deleted, plus what changed and why. No official standard becomes active without instructor approval.

## Experimentation

Experiments live in `PROPOSED/` and are inactive by default. They may override an established rule only when explicitly enabled for a named task. The AI must announce the experiment before using it, list every overridden rule, and identify the experiment in the resulting artifact or delivery report. See `META/experimentation.md`.

## Assumptions and current scope

Version 1.1.0 captures the best-established practices from prior work. Course files are intentionally preliminary, and `MODULES/`, `DECISIONS/`, and `PROPOSED/` begin with guidance rather than invented content. Assumptions are marked `ASSUMPTION`, and unresolved matters are marked `TODO`.
