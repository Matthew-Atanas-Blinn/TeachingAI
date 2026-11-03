# Decision: Quiz Import and Metadata Convention

Status: Accepted
Date: 2026-11-03
Scope: Cross-course quizzes using D2L Brightspace

## Context

Quiz imports were tested through D2L CSV files and Blackboard/IMS QTI-style packages. CSV reliably imported the required programming-quiz question types, points, feedback, titles, ordering, and difficulty metadata. Attempts to use package imports to create useful quiz sections or subsections were unreliable, while CSV section-like records were ignored or became ordinary questions.

The original reason for quiz sections was to permit shuffling within cognitive stages while preserving an easier-to-harder progression. In practice, full question shuffling offered limited academic-integrity value and disrupted the intended cognitive buildup. D2L question titles are instructor-facing in the tested quiz view, so they can carry maintainable pedagogical metadata without exposing generation artifacts to students.

## Decision

Use D2L CSV as the default quiz import format unless a required feature cannot be represented reliably in CSV.

Preserve the default pedagogical progression through question order rather than LMS section structures:

Foundation -> Tracing -> Application -> Integration -> Design/Diagnosis

Map D2L Difficulty values 1 through 5 to those categories in the same order.

Use concise, descriptive instructor-only titles in this format:

`<Category>: <Concept>`

Examples:

- `Foundation: Virtual Functions`
- `Tracing: Constructor Order`
- `Application: Rule of Three`
- `Integration: Dynamic Dispatch`
- `Diagnosis: Memory Leak`

Titles should identify the assessed concept and support later maintenance. Avoid opaque sequence-only labels such as `F01`, `T03`, or `Q12` unless a specific workflow requires them.

Do not randomize question order by default. Use quiz sections, pools, package formats, or randomization only when they have a specific instructional or operational purpose that outweighs their added complexity.

## Benefits

- Uses a tested, inspectable D2L import format.
- Preserves intentional cognitive progression without manual section creation.
- Makes quiz coverage and revision easier for future instructors.
- Retains useful D2L difficulty metadata.
- Reduces package-generation and import failures.
- Avoids exposing internal numbering artifacts to students.

## Drawbacks

- CSV does not create D2L quiz sections or Question Library sections in the tested workflow.
- Some advanced LMS features may require another format or manual configuration.
- Fixed order provides less variation between student attempts.
- The title-visibility assumption must be rechecked if the D2L interface or quiz configuration changes.

## Assumptions

- Students do not see the instructor-only title field in the active D2L quiz experience.
- Programming assignments provide substantial independent construction practice.
- Full question-order randomization provides limited deterrence compared with its cost to scaffolding.
- The current D2L CSV importer continues to preserve question order and Difficulty values.

## Alternatives considered

### Blackboard or IMS QTI packages

Potentially support richer structures, but tested packages did not reliably create useful sections or subsections and were harder to generate and validate.

### Manual D2L sections

Can preserve group-level ordering and shuffling, but add recurring setup work without enough demonstrated benefit for one quiz per module.

### Encoded titles such as F01 or T03

Compact and sortable, but less useful to future instructors revising coverage and more likely to look like generation artifacts.

### Full question randomization

May make simple answer-position sharing less convenient, but does little against broader collaboration and disrupts intentional cognitive progression.

## Consequences

- Quiz generation and review standards implement CSV, title, difficulty, ordering, and randomization defaults.
- Category names in titles must reflect actual cognitive demand, not merely topic order.
- A non-CSV format requires a concrete feature need and validation against the active D2L environment.
- Course or module rules may vary question distributions without changing the shared progression model.

## Revisit when

- D2L adds reliable CSV support for sections or groups;
- a required question type or feature cannot be represented in CSV;
- students begin seeing instructor-only titles;
- evidence shows fixed ordering materially harms assessment validity or integrity; or
- a validated package workflow creates sections reliably with acceptable maintenance cost.
