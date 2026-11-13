## Programming Fundamentals I Course Sequence

Status: Partial approved sequence
Course: COSC 1436
Last updated: 2026-11-12

### Purpose

This file records the current topic order and the instructional dependencies that justify it. It is not a weekly calendar and does not replace module source-of-truth documents.

### Current ending sequence

1. User-defined functions
2. Enums, namespaces, and type aliases
3. Arrays
4. Strings and C-strings

Earlier course ordering remains to be documented from approved current materials rather than reconstructed from assumptions.

### Dependency rationale

#### Functions before arrays
Students reuse established function concepts when traversal is moved into reusable functions. Raw arrays add specialized parameter behavior but do not require a second full functions unit.

#### Enums before arrays
Students first learn that an enum defines a categorical set. Arrays then provide an explicit collection that determines which enum values are visited and in what order.

#### Arrays before strings and C-strings
Arrays establish indexed storage, fixed capacity, traversal, and valid bounds. These ideas allow students to understand a C-string as a null-terminated character array rather than memorizing the null terminator as an isolated rule.

#### Strings and C-strings as the final section
The final section compares std::string with the lower-level C-string representation and revisits arrays, loops, functions, input, bounds, and representation choices.

### Known material-alignment gaps
- The existing strings slides do not currently include C-strings.
- The strings module requires substantial revision before it fully implements this sequence.
- Earlier course topics and their approved order remain to be documented.

### Scheduling flexibility
Instructors may adjust dates or combine small topics, but arrays should precede C-string representation unless equivalent prerequisite instruction is provided.

### Unresolved sequence decisions
- Complete the earlier-semester order.
- Determine whether strings and C-strings use one deck or multiple decks.
- Determine assignment and quiz relationships between arrays and strings.
