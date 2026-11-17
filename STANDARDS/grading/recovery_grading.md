# Recovery Grading Standard

## Purpose

Recovery grading handles submissions whose automatic score may understate demonstrated understanding, especially compile failures or localized defects. It is selective manual review, not a replacement for the autograder.

## Score rule

```text
final score = max(automatic score, recovery score)
```

Recovery may raise but never lower the automatic score.

## When to review

Perform recovery review only when the automatic score is low enough to justify the time or when a known grader limitation may have caused broad loss. Do not manually regrade every successful submission by default.

## Assignment-relevance gate

Before assigning recovery points, verify that the submitted files and code belong to the assignment currently being graded.

- Identify the current assignment's required files, interfaces, behaviors, and rubric.
- Inspect the submission for evidence addressing those requirements.
- Grade only evidence relevant to the current assignment.
- Do not award credit for meaningful or correct work that belongs to a different assignment.
- If the student clearly submitted work for another assignment, report the mismatch explicitly and apply the established near-zero wrong-assignment score, typically 1/100, unless the assignment or course policy specifies another result.
- Do not reinterpret the submitted file as though the unrelated assignment were the active grading task.
- If assignment identity is genuinely ambiguous because required materials are unavailable, stop and obtain the missing assignment specification before grading.

## Required evidence and reporting

For every reviewed student, state:

- confirmation that the evaluated files and code belong to the current assignment and provide evidence for its objectives;
- the rubric used;
- points available, earned, and deducted in every category;
- the exact reason for every deduction;
- what the code demonstrates the student understood;
- major defects or missing work;
- automatic score, recovery score, applicable late penalty, and final calculation;
- an overall summary suitable for instructor verification.

Do not invent inaccessible evidence. If a required source link, attachment, or file is missing or inaccessible, stop and ask Matthew to provide or verify it before assigning that student's grade.

## Scoring principles

- Award by correct function or independently demonstrated concept when practical.
- Give partial credit for meaningful attempts and demonstrated understanding.
- Avoid repeated deductions for the same root defect unless it independently violates separate rubric objectives.
- Apply late penalties after determining the underlying earned score unless an approved course rule says otherwise.
- Use the same rubric across comparable students.

## Compile failures

A nearly complete and otherwise correct program that does not compile, or contains an obvious defect that basic test-running should have exposed, should receive no more than 80% through recovery. The cap recognizes demonstrated work while preserving the requirement that students submit a working program.

A lower score is appropriate when compilation failure masks substantial missing or incorrect behavior.

## Minimal-effort submissions

A submission containing only starter code, a provided header, or almost no original implementation should receive near-zero recovery, typically about 1 point when the submission demonstrates essentially no relevant work. Do not grant large rubric credit merely because supplied interfaces or comments are present.

## Transparency and consistency

Feedback must make the score reproducible. Avoid vague statements such as “mostly correct.” Name the implemented and missing behaviors. If professional judgment changes the score, explain the evidence and rationale.

## Assumptions

- The assignment-specific rubric controls category values.
- Any approved course or institutional late policy supersedes examples here.
- Recovery caps are pedagogical standards, not institutional policy.
