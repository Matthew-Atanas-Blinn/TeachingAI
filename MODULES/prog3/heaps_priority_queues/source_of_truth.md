## Programming Fundamentals III: Heaps and Priority Queues

Status: Approved module source of truth  
Course: COSC 2436  
Last updated: 2026-11-06

### Purpose

This module is organized around one question:

How can a program repeatedly obtain the most important remaining item without performing O(n) work for every operation?

A priority queue defines the required behavior. A binary heap provides an efficient vector-backed implementation by maintaining partial order rather than fully sorting every value.

### Prerequisites

Students should understand vectors, linked lists, queues, binary trees, zero-based indexing, functions, classes, and foundational Big-O notation.

### Learning objectives

Students should be able to:
- distinguish stack, queue, and priority-queue removal rules;
- distinguish the priority-queue ADT from a heap implementation;
- compare familiar priority-queue implementations;
- state the complete-shape and heap-order invariants;
- distinguish a heap from a binary search tree;
- map between a complete binary tree and a zero-based vector;
- calculate parent and child indices;
- trace and implement insertion with sift-up;
- trace and implement root removal with sift-down;
- handle empty, one-element, duplicate, and one-child cases;
- analyze top, insertion, removal, and arbitrary search;
- use std::priority_queue as a max-priority queue and recognize min-priority configuration; and
- select a priority queue for an appropriate workload.

### Central mental model

Priority-queue behavior -> familiar implementation trade-off -> performance challenge -> complete shape + heap order -> vector representation -> local repair -> complexity -> STL use -> structure selection.

### Invariants

#### Complete-shape invariant
Every level is full except possibly the last, and the last level fills from left to right. Completeness keeps the height O(log n) and permits vector storage without child pointers.

#### Max-heap order invariant
Every parent has priority at least as great as each child. This guarantees that the maximum is at the root but does not fully order siblings or subtrees.

### Representation

For zero-based index i:
- left child = 2i + 1;
- right child = 2i + 2;
- parent = (i - 1) / 2 using integer division for non-root nodes.

Calculated child indices must be checked against size before access.

### Instructional sequence

- Motivate priority queues through a next-most-important workload.
- Contrast stack, queue, and priority-queue removal rules.
- Compare unsorted vector, sorted vector, and sorted linked-list implementations.
- Ask whether view-highest can be O(1) while insertion and removal are both sublinear.
- Identify that a priority queue needs partial order rather than full sorting.
- Introduce the binary heap as the solution.
- Teach complete shape and heap order as separate invariants.
- Contrast heaps with BSTs.
- Map the complete tree to a vector.
- Derive and practice index formulas.
- Trace insertion as append plus sift-up.
- Trace removal as move-last plus sift-down.
- Emphasize selecting the higher-priority child during sift-down.
- Address boundary cases and invariant-focused tests.
- Return to the implementation comparison and derive O(log n), O(1), O(log n).
- Introduce std::priority_queue and min-priority configuration.
- End with applications and structure selection.

### Complexity expectations

For a binary heap:
- view root/top: O(1);
- insertion: O(log n);
- remove root: O(log n);
- arbitrary search: O(n);
- storage: O(n).

Students should explain that the complete shape controls height and that each repair follows one root-to-leaf path.

### Misconceptions and boundaries

- A priority queue is not synonymous with a heap.
- A heap is not a BST.
- Heap order does not fully sort the vector.
- The left child is not automatically the swap target during sift-down.
- O(1) top does not imply O(1) arbitrary lookup.
- The heap's completeness is not the same as AVL or red-black balancing.
- Full bottom-up heap construction and heap sort are extensions unless later approved as core.

### Testing expectations

Selected assignments or assessments should include empty state, one element, no-swap insertion, multi-swap insertion, one-element removal, no-swap removal, multi-swap removal, duplicate priorities, a node with only a left child, and alternating insert/remove sequences. Tests should isolate insertion and removal evidence when practical to reduce cascading failure.

### Slide coverage

A complete deck should include motivation, familiar implementation trade-offs, the sublinear-operation challenge, both invariants, heap-versus-BST comparison, vector mapping, index formulas, sift-up, sift-down, boundary cases, complexity return, std::priority_queue, applications, structure selection, retrieval practice, and summary.

### Assessment guidance

Emphasize invariant recognition, tree/vector mapping, operation tracing, complexity explanation, defect diagnosis, boundary-test selection, and ADT/implementation selection. Avoid obscure comparator syntax or advanced template details unless explicitly taught.

### Assignment and autograder implications

A BinaryHeap implementation with vector storage is appropriate because implementation reveals the structure. Test empty/size, top, insertion, removal, duplicates, and alternating operations independently where possible. A standard-library-use assignment may follow, but should not replace internal implementation when implementation is an objective.

### Future connections

- heap sort;
- Dijkstra and Prim using a priority queue;
- event simulation and scheduling;
- top-k streaming problems; and
- the data-structure-selection capstone.

### Unresolved questions

- Final assignment scope and points.
- Whether bottom-up heap construction is added later.
- Whether heap sort receives a separate lesson.
- Quiz length and weighting.
