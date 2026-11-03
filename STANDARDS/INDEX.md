# Standards Index

Standards govern recurring artifact generation and review.

## Loading order

1. Read `global/INDEX.md` and load every global standard whose trigger matches the task.
2. Read the `INDEX.md` inside each applicable artifact branch.
3. Load the generation and review files selected by that branch index.
4. Apply relevant course and module context afterward.

Global standards remain active when a more specific artifact standard is loaded. Specific standards may add detail but must not silently contradict a governing global standard.

## Branches

- `global/`: operational standards that span multiple artifact types.
- `slides/`: slide generation and review.
- `quizzes/`: quiz generation and review.
- `assignments/`: assignment generation and review.
- `autograders/`: autograder generation and review.
- `grading/`: grading workflows and rules.

Read only the artifact branches relevant to the current task.
