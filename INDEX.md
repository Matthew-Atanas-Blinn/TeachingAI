# TeachingAI Repository v1.6.0

## Purpose

TeachingAI is an AI-independent repository of durable teaching standards, course architecture, assessment practices, grading rules, review procedures, and pedagogical rationale. It converts knowledge that would otherwise remain scattered across memory, conversations, and one-time corrections into reusable institutional knowledge.

The repository is intended to improve student learning while making course development more consistent, transparent, portable, and sustainable. It should be useful to a human collaborator or any future AI system, not only the system that created it.

## Authority and precedence

Apply relevant authority in this order unless an explicitly enabled experiment says otherwise:

1. Applicable legal, privacy, safety, and institutional requirements.
2. `REQUIRED/` universal principles.
3. Triggered cross-artifact standards in `STANDARDS/global/`.
4. Applicable artifact-specific standards in `STANDARDS/`.
5. Relevant `COURSES/` constraints.
6. Relevant `MODULES/` source-of-truth documents.
7. Explicit current-task instructions.
8. Explicitly enabled experimental overrides from `PROPOSED/`.

A lower-level instruction may specialize a higher-level default, but it must not silently contradict a higher-authority requirement.

## Mandatory hierarchical traversal

The repository uses hierarchical `INDEX.md` files to route context.

For every substantive task:

1. begin with this root index;
2. read `REQUIRED/INDEX.md` and all universal files it selects;
3. read `STANDARDS/INDEX.md`, then load every triggered global standard and each applicable artifact branch;
4. read `COURSES/INDEX.md` and select only the relevant course context;
5. for module-specific work, read `MODULES/INDEX.md`, then follow the applicable course and module indexes;
6. use each selected index to identify the smallest branch that fully governs the task; and
7. do not read unrelated siblings unless comparison, reuse, or dependency checking requires them.

When entering any folder, read its `INDEX.md` before selecting other files from that folder. Every folder has an index, even if the index currently says to inspect all files in that folder.

Indexes route only through their immediate folder. The root index does not enumerate every module, decision, proposal, or artifact subtype.

Lower-level files must not point backward into the rules or decisions hierarchy. Required upper-level authority must already be active through top-down traversal. If governing context is likely to be skipped, correct the routing indexes or repository governance rather than adding defensive backward pointers below it.

## Top-level branches

- `META/INDEX.md`: repository governance, maintenance, experimentation, and history.
- `REQUIRED/INDEX.md`: universal pedagogy, accessibility, and privacy requirements.
- `STANDARDS/INDEX.md`: global and artifact-specific operational standards.
- `COURSES/INDEX.md`: course-level context.
- `MODULES/INDEX.md`: topic-level source-of-truth branches.
- `DECISIONS/INDEX.md`: accepted rationale to load when a decision is reconsidered or changed.
- `PROPOSED/INDEX.md`: inactive experiments and proposal structure.

## Information flow

```text
Root INDEX
    -> REQUIRED universal constraints
    -> triggered STANDARDS/global rules
    -> applicable artifact STANDARDS
    -> relevant COURSE context
    -> relevant MODULE source of truth
    -> current task instructions
    -> generation or analysis
    -> global + artifact + module review
    -> instructor acceptance or revision
```

## Decision records

Accepted decision records preserve rationale. They are not automatically loaded for routine generation when their operational conclusion is already present in governing standards or source-of-truth files. Use `DECISIONS/INDEX.md` when reconsidering a choice, changing an implementing rule, comparing alternatives, checking assumptions, or evaluating revisit conditions.

## Updating the repository

Repository-maintenance work must load all files selected by `META/INDEX.md`. Every applied change must report every file and folder added, modified, moved, renamed, or deleted, plus the reason. Immediate-child changes update the nearest owning `INDEX.md`; ancestor indexes do not recursively catalog descendants owned by lower indexes.

## Experimentation

Experiments live in `PROPOSED/` and are inactive by default. They may vary an established standard only when explicitly enabled for a named task. Privacy, safety, institutional policy, and explicit current-task instructions remain authoritative.

## Operating principles

- Store durable, reusable knowledge rather than temporary task notes.
- Prefer changes that prevent a class of problems over isolated corrections.
- Preserve rationale for consequential choices.
- Keep established standards separate from experiments.
- Treat generated materials as drafts until the required review is complete.
- Optimize educational value per unit of instructor time without sacrificing correctness, accessibility, privacy, or assessment fairness.
- Keep authoritative rules singular.
- Use plain, portable formats.
- Store source-of-truth knowledge rather than routine generated artifacts.

## Current scope

Version 1.7.0 adds the approved Programming I arrays module, per-course sequence files, and a strings/C-strings decision stub that records the current slide-alignment gap.
