## Heaps and Priority Queues Review Checklist

### Architecture
- The module begins with priority-queue behavior and familiar representations.
- The sublinear-operation challenge appears before the binary heap is introduced.
- The heap performance row appears only after representation and operations are understood.
- STL usage follows internal implementation understanding.

### Terminology and invariants
- Priority queue and heap are not treated as synonyms.
- Complete shape and heap order are stated separately.
- Max-heap and min-heap conventions remain consistent.
- Heap and BST ordering rules are explicitly contrasted.
- No claim implies that a heap is fully sorted.

### Representation
- Every heap diagram is complete.
- Every parent-child pair satisfies the stated order invariant unless the slide intentionally shows a violation.
- Tree and vector representations contain identical values in identical logical positions.
- Zero-based parent and child formulas are correct.
- Root and child-bound checks are handled correctly.

### Operations
- Insertion appends before sifting upward.
- Sift-up follows only the new node's ancestor path.
- Removal moves the last value to the root before popping the final position.
- Sift-down selects the higher-priority child.
- One-child and one-element cases are correct.
- Duplicate priorities do not cause unnecessary swaps or infinite loops.

### Complexity and selection
- top/view-root is O(1).
- insertion and root removal are O(log n).
- arbitrary search is O(n).
- The explanation connects completeness to logarithmic height.
- Comparisons with vectors, queues, BSTs, and hash tables match their supported operations.

### C++ and STL
- Code matches the stated zero-based representation.
- Code checks index validity before child access.
- std::priority_queue operations and default max behavior are accurate.
- Min-priority configuration is presented at an appropriate syntax depth.

### Assessment and testing
- Tracing includes no-swap and multi-swap cases.
- Tests include empty, one-element, duplicate, one-child, and alternating-operation states.
- Insertion and removal are isolated where practical to minimize cascading failure.
- Questions include invariant diagnosis, complexity reasoning, and structure selection.
