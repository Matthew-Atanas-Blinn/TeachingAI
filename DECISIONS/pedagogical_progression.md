# Decision: Default Pedagogical Progression

Status: Accepted
Date: 2026-10-30
Scope: Cross-course instruction and assessment

## Context

Programming students must learn terminology and syntax, build accurate execution models, apply techniques, combine them in larger problems, and eventually make or diagnose design decisions. Presenting those demands without progression can overload novices; stopping at recognition or tracing fails to establish transfer.

## Decision

Use this default cognitive progression when it fits the artifact and module:

```text
Foundation -> Tracing -> Application -> Integration -> Design/Diagnosis
```

Map quiz difficulty 1-5 to those categories. Preserve the order by default rather than randomizing it. Not every lesson, slide deck, quiz, or assignment must include every category.

## Evidence-informed rationale

The progression combines several established instructional ideas:

- prerequisite knowledge supports later problem solving;
- worked or guided reasoning can reduce unnecessary novice load;
- tracing helps learners build execution models before constructing larger solutions;
- guidance should fade as learners become capable of independent application;
- integration and design require transfer across concepts rather than isolated recall.

This repository records the practical conclusion rather than claiming that one study proves the exact five labels or their universal order. The labels are a local design model informed by broader research and teaching experience.

## Benefits

- Creates a predictable path from recognition to transfer.
- Makes quiz titles, difficulty, and review more consistent.
- Reduces early overload while preserving advanced reasoning.
- Helps expose whether instruction stops before application or design.

## Drawbacks

- Some topics are too small to justify all five stages.
- Experts or advanced students may not need as much foundation or tracing.
- Strict ordering can become artificial when authentic tasks require iterative movement between tracing, application, and diagnosis.
- A long quiz may overemphasize lower levels if the distribution is applied mechanically.

## Assumptions

- Students are still developing mental models for the target concept.
- Programming assignments provide substantial construction practice.
- The progression is used as a scaffold, not as a prohibition on authentic integrated work.

## Alternatives considered

- **Unstructured mixture:** flexible but makes coverage and cognitive progression harder to inspect.
- **Bloom-style labels alone:** useful at a broad level but less specific to tracing and diagnosis in programming.
- **Application-first discovery for every topic:** motivating in some contexts, but may overload students when prerequisites or execution models are weak.
- **Randomized quiz order:** can reduce sharing but disrupts intended cognitive buildup and dependent context.

## Override conditions

Override or compress the progression when:

- learners have demonstrated prerequisite mastery;
- the module is a brief review rather than first instruction;
- authentic problem-based learning needs application before formalization;
- the artifact assesses only one explicitly defined level;
- accessibility or time constraints require another structure; or
- stronger current evidence or observed course outcomes support a better sequence.

Report consequential overrides and preserve recurring alternatives in `PROPOSED/`, the relevant course/module file, or a new decision record.

## Consequences

- Quiz standards use the five categories and default order.
- For D2L quizzes, progression is normally preserved through question order rather than imported sections or full question randomization.
- Module source-of-truth documents should identify which stages are appropriate.
- Reviews should verify that category labels match actual cognitive demand.

## Files implementing the decision

- `REQUIRED/pedagogy.md`
- `STANDARDS/quizzes/generation.md`
- `STANDARDS/quizzes/review_checklist.md`
- relevant course and module files

## Revisit when

- course outcomes indicate poor transfer despite successful lower-level performance;
- new pedagogy or research supports a materially better progression;
- the programming curriculum changes enough that the assumptions no longer hold.
