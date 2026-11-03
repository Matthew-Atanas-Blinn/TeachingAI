# Decision: Semantic Visual Mapping Across Backgrounds

Status: Accepted
Date: 2026-11-02
Scope: Cross-course

## Context

Instructional artifacts often use color to connect a descriptor with code, a diagram component, a formula element, a state, or a process step. One exact color may be readable on a light background but inaccessible on a dark one.

## Decision

Related elements use the same semantic color family, with a higher-luminance variant on dark backgrounds and a lower-luminance variant on light backgrounds. Exact hexadecimal identity is not required.

Every important mapping also uses a non-color cue. Instructional mapping takes priority over generic syntax highlighting, and final rendered artifacts are reviewed at likely delivery scale.

## Benefits

- Preserves explanatory correspondence.
- Maintains local contrast.
- Supports classroom projection.
- Reduces reliance on color alone.
- Creates a reusable visual language across courses.

## Drawbacks

- Requires multiple values for one semantic family.
- Adds generation and review work.
- Can produce visual noise if too many categories appear at once.

## Assumptions

- Color supports meaning rather than decoration.
- Final rendering is available for review.
- Backgrounds may vary within an artifact.

## Alternatives considered

### Use the same exact color everywhere

Rejected because contrast changes by background.

### Use unrelated accessible colors

Rejected because correspondence becomes harder to perceive.

### Remove color mapping entirely

Useful in some cases, but not accepted as a universal limitation.

### Use ordinary syntax highlighting only

Rejected when conceptual categories do not align with lexical syntax categories.

## Consequences

- Visual standards map meaning before colors are selected.
- Local contrast is evaluated separately for each background.
- A stable semantic palette is preferred over arbitrary per-slide choices.
- Exact global color tokens remain separate implementation choices.

## Revisit when

- a repository-wide token palette is approved;
- projection testing reveals inadequate contrast; or
- accessibility review identifies a more effective encoding.
