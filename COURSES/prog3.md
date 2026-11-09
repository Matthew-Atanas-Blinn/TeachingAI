# Programming Fundamentals III (COSC 2436)

Status: Preliminary course-level context. Expand through module redesign rather than inventing a complete structure now.

## Learner context

Students have prior programming experience and should connect implementation, invariants, complexity, and appropriate data-structure selection. Materials may include concise reasoning and small proofs when students have the prerequisites.

## Durable approach

- Teach both use and internal representation of data structures.
- Connect operations to invariants and asymptotic cost.
- For each major structure, identify what must remain true, which operations may violate it, how the implementation restores it, and what test could reveal a violation.
- After students understand a major structure's behavior and internal representation, connect it promptly to the corresponding C++ standard-library container or adapter when one exists.
- When an algorithm exemplifies a broader design pattern, name the pattern when doing so improves transfer; do not turn the pattern names into a disconnected memorization list.
- When introducing binary search trees, show how height controls operation cost, demonstrate degeneration, and introduce balanced trees as the solution. Conceptual understanding and rotation tracing are the default depth unless a later module decision requires implementation.
- Include student-designed tests in selected assignments and assessments when test design reveals understanding of boundary cases, state transitions, or structural invariants.
- Use tracing and diagrams to make state changes visible.
- Include implementation practice where it reveals the structure's behavior, not merely syntax.
- Require comparisons and design choices after students understand foundational operations.
- Develop data-structure selection through small comparisons throughout the course, then give it greater weight in a short capstone module and on the final examination.
- For amortized analysis, a small proof may be appropriate when prior Big-O knowledge supports it.

## Assessment context

Quizzes should progress from recognition and tracing through implementation consequences, integration, and structure/algorithm selection. Assignments and harnesses should test operations independently to reduce cascading failures. Quizzes may ask students to identify an invariant, diagnose a violation, choose a test that exposes a defect, compare a structure with its STL equivalent, or identify an algorithmic design pattern. The final examination should include a meaningful group of structure-selection questions requiring a choice, operation-cost justification, and rejection of at least one plausible alternative.

## TODO

- Document the approved data-structure sequence.
- Add current decisions for vectors/sequence containers, stacks/queues, trees, graphs, hash tables, sorting, and related algorithms.
- Add module source-of-truth documents as each unit is redesigned.
