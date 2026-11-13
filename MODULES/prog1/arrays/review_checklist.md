## Arrays Review Checklist

### Architecture
- The module begins with a collection problem rather than syntax.
- State tracing precedes large independent implementation.
- Functions appear as integration, not a duplicate functions unit.
- Selection sort remains a small culmination rather than an algorithms unit.
- Two-dimensional coverage remains at introductory row/column depth.

### Mental model and initialization
- Array name, element type, capacity, indices, elements, and stored values are distinguished.
- Index and stored value are never used interchangeably.
- State changes are shown explicitly.
- The final valid index is size - 1.
- Diagram indices and code indices agree.
- Uninitialized local elements are not given predictable values.
- Partial and zero initialization are represented correctly.

### Traversal and logical size
- Traversals use the intended valid range.
- i < size is not replaced accidentally by i <= size.
- Accumulators and candidate values are initialized correctly.
- Capacity and logical size are distinguished where both appear.
- Empty-range assumptions are stated when relevant.

### Functions
- Array parameters are not called genuine reference parameters.
- Material states that no element-by-element array copy occurs.
- Caller-visible element modification is represented correctly.
- Size is supplied separately where needed.
- const is used for read-only access.
- Pointer arithmetic remains outside the instructional depth.

### Simple processing
- Linear-search found/not-found behavior is defined.
- Returned indices are distinguished from returned values.
- Reversal avoids duplicate swaps.
- Selection-sort examples distinguish smallest value from smallestIndex.
- Formal sorting analysis is absent unless explicitly approved.

### Two-dimensional arrays
- Row and column order remain consistent.
- Dimensions, initializer layout, and diagrams agree.
- Nested-loop bounds match the correct dimensions.
- Row-total and column-total examples use the correct changing and fixed index.
- Swapped-index diagnosis is technically accurate.

### Boundaries and connections
- Undefined out-of-bounds behavior is not illustrated with a guaranteed output.
- No example reads an uninitialized element.
- Enum traversal uses an explicit array of valid values.
- C-strings are deferred to the later strings module.
