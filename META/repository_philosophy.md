# Repository Philosophy

## Why this repository exists

High-quality teaching materials form a connected system. A change to slides can alter what a quiz should assess; a change to an assignment can require a new autograder; a grading rule can affect test design. When the standards behind these artifacts exist only in memory or chat history, the same issues must be rediscovered and explained repeatedly.

TeachingAI externalizes those standards. Its purpose is not to replace professional judgment. Its purpose is to preserve decisions, reduce repeated specification work, and make AI-assisted development more dependable.

## Core goals

1. **Student learning:** improve clarity, sequencing, practice, feedback, and valid assessment.
2. **Consistency:** make artifacts created at different times follow compatible standards.
3. **Continuous improvement:** convert recurring problems into durable prevention rules.
4. **Sustainability:** reduce avoidable instructor rework while preserving meaningful review.
5. **Traceability:** make it possible to determine what changed, why, and under which rules an artifact was created.
6. **Portability:** remain usable across AI products, authoring tools, and learning-management systems.
7. **Privacy:** protect student information and stop when a tool's data handling is not approved or understood.

## Design principles

- **Separate concerns.** Universal requirements, artifact standards, course constraints, module content, accepted rationale, and experiments belong in different locations.
- **Prefer authoritative sources.** A module source of truth should govern module coverage; generated slides or quizzes should not independently redefine it.
- **Make review explicit.** Generation instructions describe how to build. Review checklists describe how to verify.
- **Generalize carefully.** Record a reusable rule when it prevents likely future failures. Do not elevate a one-time preference into a universal standard without evidence.
- **Preserve judgment.** Rules should support rather than conceal instructor decisions. When reasonable alternatives exist, state benefits, drawbacks, assumptions, and the selected option.
- **Avoid false completeness.** Mark unknowns and TODOs instead of inventing requirements.

## Success criteria

The repository succeeds when it reduces repeated corrections, catches foreseeable failures before the instructor sees them, keeps related artifacts aligned, and allows a future AI or human collaborator to understand both the rules and their rationale.

It fails when it becomes a dumping ground, silently changes policy, accumulates contradictory rules, obscures experimental behavior, or creates more maintenance work than it saves.
