# Modules

Create one folder per course/module only when that module is being designed or revised.

Recommended structure:

```text
MODULES/prog1/enums_namespaces_aliases/
├── source_of_truth.md
├── review_checklist.md
└── decisions.md
```

`source_of_truth.md` should be detailed and may include objectives, prerequisites, vocabulary, mental models, misconceptions, scope boundaries, examples and non-examples, instructional sequence, slide coverage, quiz mapping, assignment mapping, autograder implications, future connections, and unresolved questions.

`review_checklist.md` contains topic-specific checks. Artifact-wide checks remain in `STANDARDS/`.

`decisions.md` records module-local rationale. Course-wide or cross-course accepted rationale belongs in `DECISIONS/`.

Do not read all modules for every task. Use only the relevant module and dependencies named by its source of truth.
