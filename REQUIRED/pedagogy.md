# Required Pedagogy Principles

## Core objective

Optimize durable student understanding and transfer, not merely content coverage or artifact polish.

## How to use these defaults

The principles below are evidence-informed defaults and established teaching preferences, not timeless laws. Apply them unless the course, module, learners, or stronger current evidence justifies an alternative. When overriding a consequential default, state the reason and preserve it in the appropriate course, module, proposal, or decision record.

## Required principles

### Align objectives, instruction, practice, and assessment

Students should not be assessed on material that was removed from instruction or not reasonably introduced and practiced. When a source-of-truth change affects slides, quizzes, assignments, rubrics, or autograders, identify and update the dependent artifacts.

**Rationale:** Alignment improves the validity and fairness of assessment. It also prevents downstream artifacts from silently preserving outdated curriculum.

### Scaffold complexity

Move from prerequisite knowledge toward increasingly independent application. The default progression is:

```text
Foundation -> Tracing -> Application -> Integration -> Design/Diagnosis
```

This is a default, not a demand that every artifact contain all five stages.

**Rationale:** Novice programmers must coordinate syntax, program state, control flow, domain concepts, and problem decomposition. Early scaffolding reduces interacting demands; tracing and guided application build mental models; later integration and design require independent transfer. Guidance should fade rather than remain permanent.

See `DECISIONS/pedagogical_progression.md` for the decision rationale, alternatives, assumptions, and override conditions.

### Motivate before formalizing

When practical, begin with a problem, limitation, question, or misconception that makes the new concept useful. Then introduce the concept as a solution and connect it to prior knowledge.

**Rationale:** A motivating problem gives students a retrieval structure for the new idea and reduces the chance that syntax is memorized without understanding when or why to use it.

### Manage cognitive load

- Introduce one important novelty at a time when possible.
- Avoid examples whose incidental syntax obscures the target concept.
- Use consistent terminology and representations.
- Segment complex processes into meaningful steps, then reintegrate them.
- Remove decorative or redundant content that competes with learning.

**Rationale:** Working memory is limited, especially for novices who have not yet organized programming concepts into reusable schemas. Instruction should reserve attention for the intended concept while still reassembling parts into authentic tasks.

### Use examples and non-examples

Show correct use, likely mistakes, boundaries, and consequences. Examples should match the claims made about them and should be verified by tracing or execution when applicable.

**Rationale:** Contrasting cases helps students distinguish defining features from superficial ones and supports diagnosis of common misconceptions.

### Preserve productive struggle

Do not reveal line-by-line solutions when the learning objective is implementation or design. Provide behavior, constraints, interfaces, and targeted scaffolding while leaving meaningful decisions to students.

**Rationale:** Complete solutions can improve immediate performance while reducing the independent retrieval and decision-making students need for transfer. Scaffolding should support the target skill without performing it for the student.

### Assess understanding, not avoidable wording traps

Questions should be difficult because of the concept, not because of hidden assumptions, unnecessary prose, or ambiguous grammar. Distractors should represent plausible misconceptions.

**Rationale:** Assessment evidence is more useful when wrong answers diagnose conceptual difficulty rather than reading ambiguity or accidental formatting problems.

### Minimize cascading failure

In assignments and autograders, isolate concepts when practical so one defect does not erase unrelated credit. Each test or rubric category should primarily measure the functionality assigned to it.

**Rationale:** Independent evidence produces more accurate grades and more actionable feedback. Integration still matters, but it should be assessed intentionally rather than emerging accidentally from fragile tests.

### Prefer transparent feedback

Students and instructors should be able to determine what was correct, what failed, why points were lost, and how the score was produced.

**Rationale:** Reproducible feedback supports learning, appeals, consistency, and maintenance of the grading system.

### Use evidence and professional judgment

When evaluating an idea:

1. state benefits;
2. state drawbacks;
3. state assumptions;
4. compare viable alternatives;
5. endorse only after comparison.

Challenge both the instructor's reasoning and the AI's reasoning constructively. When evidence is weak or context-sensitive, say so.

**Rationale:** Educational choices involve tradeoffs. Explicit assumptions and alternatives prevent preferences from being presented as universal facts and make later revision easier.

## AI-assisted teaching

AI may draft, inspect, compare, generate variants, and run preflight checks. It must not imply that a generated artifact is verified when it has not been checked. Human review may be prioritized by risk, but correctness, privacy, assessment validity, and severe presentation failures require attention before release.

**Rationale:** AI can reduce production time, but generated artifacts may contain plausible conceptual, visual, formatting, or answer-key errors. Responsibility remains with the instructor and the approved process.
