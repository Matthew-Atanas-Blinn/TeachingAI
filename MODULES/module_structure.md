# Module Structure Standard

Create a module folder only when that module is being designed, approved, or substantially revised.

Recommended structure:

```text
MODULES/<course>/<module>/
├── source_of_truth.md
├── review_checklist.md
└── decisions.md
```

## Source of truth

`source_of_truth.md` may include:

- purpose and scope;
- objectives and prerequisites;
- vocabulary and mental models;
- misconceptions;
- examples and non-examples;
- instructional sequence;
- slide coverage;
- quiz and assignment mapping;
- autograder implications;
- future connections; and
- unresolved questions.

## Review checklist

`review_checklist.md` contains topic-specific checks. Universal and artifact-wide checks remain in their governing folders and are not copied into the module.

## Decisions

`decisions.md` records only module-local rationale. Course-wide, cross-course, artifact-wide, and repository-wide accepted rationale belongs at the corresponding higher level.

## Decision stubs for undeveloped modules

When an approved decision affects a module that has not yet been developed, create or update a concise module decision stub rather than prematurely designing the entire module. The stub must:
- record the approved decision;
- identify the module as undeveloped or partially designed;
- list the major details that remain undecided; and
- state that those details must be completed before substantial module materials are created.

Do not invent learning objectives, assessment requirements, implementation depth, or other consequential details merely to make the module appear complete. A decision-stub folder may initially contain only INDEX.md and decisions.md. Add source_of_truth.md and review_checklist.md when the module is actually designed or substantially revised.

## Selective loading

Do not read every module. Follow the hierarchical indexes and load only the module or modules necessary for the current task, plus dependencies named by the selected source of truth.

## Index requirement

Each course folder under `MODULES/` has an `INDEX.md`, even when it is only a stub. Add a module to the nearest course index when the module folder is created. A small leaf module folder does not need its own index unless selection inside it becomes nontrivial.
