# TeachingAI

TeachingAI is an AI-independent framework for creating, reviewing, and
continuously improving instructional materials.

It provides a structured repository of:

- pedagogical principles;
- accessibility and data-privacy requirements;
- generation standards;
- review checklists;
- course-level context;
- module source-of-truth documents;
- accepted design decisions; and
- controlled experiments.

The repository is designed to help educators use generative AI without
depending entirely on chat memory, repeatedly rewriting the same prompts,
or silently accepting inconsistent output.

## Why TeachingAI Exists

AI can create slides, quizzes, assignments, rubrics, and autograders
quickly, but generation alone does not guarantee:

- pedagogical alignment;
- technical accuracy;
- accessible visual design;
- reliable answer keys;
- consistency across instructional materials;
- protection of student information; or
- preservation of the reasoning behind instructional decisions.

TeachingAI treats those concerns as a maintainable system rather than a
collection of one-time prompts.

The repository externalizes durable teaching knowledge so that it can be:

- reviewed;
- versioned;
- improved;
- shared;
- reused with different AI systems; and
- preserved independently of any AI vendor.

## Core Model

TeachingAI separates instructional knowledge into several layers:

```text
REQUIRED
    Universal pedagogy, accessibility, privacy, and safety requirements

STANDARDS
    How instructional artifacts are generated and reviewed

COURSES
    Long-lived course-level context and constraints

MODULES
    Topic-specific source-of-truth documents

DECISIONS
    Accepted decisions and their rationale

PROPOSED
    Inactive experimental rules and possible improvements

META
    Governance for maintaining the repository itself
```

These layers combine to guide the generation and review of:

- slides;
- quizzes;
- assignments;
- autograders;
- grading procedures; and
- other instructional materials.

## Getting Started

1. Read `INDEX.md`.
2. Read the files identified as always required.
3. Select the standards relevant to the artifact being created.
4. Add the applicable course context.
5. Add the relevant module source of truth, if one exists.
6. Provide the selected files or the repository to the AI system.
7. Generate, review, correct, and regression-check the artifact.

`INDEX.md` defines the repository’s authority order and tells an AI or
human collaborator which files should be read for a particular task.

## Example AI Instruction

A general starting instruction might be:

> Use the TeachingAI repository as the governing context for this task.
> Read INDEX.md, all required files, the standards applicable to this
> artifact, the relevant course file, and the relevant module source of
> truth. Report conflicts, assumptions, experimental rules, and every
> repository file changed.

The repository is designed so that the entire folder may be provided to
an AI while `INDEX.md` controls which files should enter active context.

## Continuous Improvement

Recurring problems should follow this process:

```text
Problem
-> Diagnose the governing cause
-> Correct the governing source
-> Regenerate or repair affected artifacts
-> Review
-> Prevent recurrence
```

Experimental changes remain in `PROPOSED/` until explicitly enabled and
evaluated. Official standards do not change silently.

## Data Privacy

TeachingAI must not contain student records, submissions, grades,
identifiers, or other student-specific information.

Before using an AI system with student information, educators must verify
that the specific product, account, configuration, and institutional
authorization provide the required protections.

If data handling or authorization is uncertain, stop and consult the
appropriate institutional authority.

See `REQUIRED/data_privacy.md`.

## Current Status

TeachingAI is an evolving framework developed through practical use in
college-level computer science instruction.

Version 1.6.0 includes standards for:

- slide generation and review;
- quiz generation and review;
- assignment design and review;
- autograder development and validation;
- recovery grading;
- accessibility;
- student-data privacy; and
- repository governance.

Programming Fundamentals III includes an approved heaps and priority-queues module plus decision stubs for balanced trees and data-structure selection. Version 1.6.0 also defines how TeachingAI integrates with Matthew's separate C++ Assignment Grading Pipeline without copying its software implementation or release-specific schema. Some course-specific files remain preliminary. Module source-of-truth
documents will be added incrementally as individual units are redesigned.

## Repository Navigation

Begin with `INDEX.md`.

Important locations include:

- `META/repository_philosophy.md`
- `REQUIRED/pedagogy.md`
- `REQUIRED/accessibility.md`
- `REQUIRED/data_privacy.md`
- `STANDARDS/slides/generation.md`
- `STANDARDS/quizzes/generation.md`
- `META/update_process.md`
- `META/experimentation.md`

## Project Status

TeachingAI is currently a public work-in-progress.

The repository is actively used and refined in real instructional
settings, but standards, module documents, and supporting materials
continue to evolve.

Feedback, discussion, and contributions are welcome.

## Contributing

Contributions are welcome.

When proposing a change, please identify:

- the problem being addressed;
- the proposed change;
- benefits and drawbacks;
- assumptions;
- alternatives considered;
- every file affected; and
- how the change was validated.

Proposed changes should preserve the repository's emphasis on durable,
reusable knowledge rather than temporary solutions or one-time fixes.

## License

TeachingAI is licensed under the
Creative Commons Attribution-ShareAlike 4.0 International
(CC BY-SA 4.0) license.

You are free to:

- Share — copy and redistribute the material in any medium or format
- Adapt — remix, transform, and build upon the material for any purpose,
  including commercially

Under the following terms:

- Attribution — appropriate credit must be given
- ShareAlike — derivative works must be distributed under the same license

See the LICENSE file for details.
## Hierarchical context routing

Version 1.3.0 uses `INDEX.md` files at every folder level. Start with the root index, then follow only the branches relevant to the task. Cross-artifact operational rules live in `STANDARDS/global/`; artifact branches add specialized generation and review requirements. Indexes route through immediate children rather than duplicating the full repository tree.
