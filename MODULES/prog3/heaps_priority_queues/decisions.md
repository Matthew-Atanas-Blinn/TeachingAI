## Module Decisions: Heaps and Priority Queues

### Decision 1: Motivate the ADT before naming the heap

Status: Accepted  
Date: 2026-11-06

Begin with priority-queue behavior and compare familiar implementations students already understand. Ask whether viewing the highest-priority item can remain O(1) while insertion and removal both become sublinear. Do not show the binary-heap performance row until students understand the heap representation and operations. Return to the comparison afterward.

### Decision 2: Use a vector-backed max-heap first

Status: Accepted  
Date: 2026-11-06

Use a zero-based vector-backed binary max-heap as the primary implementation. Introduce min-heaps afterward as a comparison-rule variation.

### Decision 3: Organize operations around invariants

Status: Accepted  
Date: 2026-11-06

Explain insertion and removal as preserving the complete-shape invariant and restoring the heap-order invariant.

### Decision 4: Implement before using the standard adapter

Status: Accepted  
Date: 2026-11-06

Students should first understand the representation, sift-up, and sift-down. Connect the implementation promptly to std::priority_queue afterward.

### Decision 5: Keep balanced trees comparative

Status: Accepted  
Date: 2026-11-06

Ordinary BST concepts are a prerequisite. Balanced trees may appear in comparisons but are not a prerequisite for learning heaps.

### Decision 6: Treat heap sort as a connection

Status: Accepted  
Date: 2026-11-06

Heap sort is a future connection unless schedule and artifact alignment justify expanding it into a core objective.
