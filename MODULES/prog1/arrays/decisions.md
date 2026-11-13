## Module Decisions: Arrays

### Decision 1: Organize around array state and traversal
Status: Accepted
Date: 2026-11-12
Teach arrays through Create -> Select -> Change -> Traverse -> Process -> Combine. Repeatedly connect code to the evaluated index, selected element, and resulting state.

### Decision 2: Use raw built-in arrays as the primary representation
Status: Accepted
Date: 2026-11-12
Raw arrays match the current course context and establish the representation needed for later C-string instruction. Modern containers remain future connections.

### Decision 3: Trace before independent implementation
Status: Accepted
Date: 2026-11-12
Use prediction and state tracing before students independently write larger array-processing code.

### Decision 4: Integrate array functions rather than create a separate major section
Status: Accepted
Date: 2026-11-12
Students already know functions. Introduce array-plus-size interfaces, const read-only access, and caller-visible element changes as a short integration movement.

### Decision 5: Distinguish array parameters from reference parameters
Status: Accepted
Date: 2026-11-12
Teach the behavioral model first: no element-by-element copy, access to caller-owned elements, and a separate size. Clarify briefly that int values[] is adjusted to a pointer parameter rather than becoming a genuine reference parameter.

### Decision 6: Use simple processing problems before richer algorithms
Status: Accepted
Date: 2026-11-12
Sum, count, minimum/maximum, linear search, and reversal are core examples. They develop traversal without turning the module into an algorithms unit.

### Decision 7: Keep selection sort as a limited culminating example
Status: Accepted
Date: 2026-11-12
Use selection sort for nested-loop tracing, minimum-index tracking, and swapping. Do not make formal analysis, stability, proof, or comparison among sorting methods core objectives.

### Decision 8: Keep two-dimensional arrays introductory
Status: Accepted
Date: 2026-11-12
Teach row/column indexing, nested traversal, row totals, column totals, and swapped-index diagnosis. Defer general multidimensional theory.

### Decision 9: Use an explicit array for enum traversal
Status: Accepted
Date: 2026-11-12
The enum defines the category; the array defines membership and traversal order. Do not normalize enum arithmetic or integer-cast loops.

### Decision 10: Place strings and C-strings after arrays
Status: Accepted
Date: 2026-11-12
Teach C-strings within the later strings module so students can compare std::string with a null-terminated character-array representation. The existing strings slides do not yet implement this decision.
