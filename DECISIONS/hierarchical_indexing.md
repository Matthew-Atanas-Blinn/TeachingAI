# Decision: Hierarchical Repository Indexing

Status: Accepted
Date: 2026-11-02
Scope: Repository

## Context

A single root index cannot sustainably list every module, decision, standard, proposal, and future branch. A fully expanded catalog would duplicate the directory tree, require frequent maintenance, increase context load, and encourage unrelated files to be read.

## Decision

Use hierarchical `INDEX.md` files throughout the repository.

The root index routes to major areas. Each subfolder index routes only through its immediate contents. Readers follow indexes from the top down, select the smallest branch that fully governs the task, and avoid unrelated sibling branches.

Every folder has an `INDEX.md`, even when the initial index is only a stub instructing the reader to inspect all files in that folder until more selective routing becomes useful.

Lower-level files do not point backward into the rules or decisions hierarchy. Governing upper-level context must already be active through required index traversal.

## Benefits

- Keeps the root index concise and stable.
- Supports selective context loading.
- Places navigation near the content it describes.
- Scales as branches grow.
- Makes routing failures visible instead of hiding them with backward pointers.

## Drawbacks

- Adds small navigation files throughout the repository.
- Requires maintenance when immediate children change.
- Overly detailed indexes could themselves become burdensome.

## Assumptions

- Folder names remain descriptive.
- Readers obey mandatory top-down traversal.
- Indexes remain routing documents rather than substantive policy files.

## Alternatives considered

### List everything in the root index

Rejected because it would grow indefinitely and duplicate the repository tree.

### Use directory names only

Rejected for the long term because names alone do not always explain triggers or exclusions.

### Use `README.md` for navigation

Rejected because `INDEX.md` has an explicit routing role, while structural guidance belongs in separately named files.

### Add lower-level backward pointers

Rejected because they duplicate architecture and conceal skipped governing context.

## Consequences

- Every folder gains an index.
- Immediate-child changes update the nearest owning index only.
- Existing navigation READMEs are split into indexes and structural guidance.
- Index validation becomes part of repository maintenance.

## Revisit when

- repository tooling generates indexes automatically;
- index maintenance exceeds its navigation value; or
- retrieval systems reliably provide equivalent selective traversal.
