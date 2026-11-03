# Quiz Generation Standard

## Goal

Produce valid, readable assessments aligned with what students were taught and expected to practice. Difficulty should come from the concept, not formatting defects or ambiguity.

## Source and alignment

Use the applicable module source of truth, current slides, assignment expectations, and course rules. Do not preserve outdated behavior merely because it appeared in an old quiz. Use prior quizzes primarily for length, tone, and import-format reference unless instructed otherwise.

Create a coverage map before final generation:

```text
Objective -> Questions -> Difficulty/category -> Points
```

No important assessed concept should be absent from instruction, and no key objective should be unintentionally unassessed.

## Pedagogical order

Default order:

1. `Foundation` (Difficulty 1)
2. `Tracing` (Difficulty 2)
3. `Application` (Difficulty 3)
4. `Integration` (Difficulty 4)
5. `Design/Diagnosis` (Difficulty 5)

This order is intentional. Do not randomize question order by default when later questions depend on concepts or cognitive buildup from earlier ones.

Instructor-only question titles should use:

```text
<Category>: <Concept>
```

Examples: `Tracing: Reference Aliasing`, `Diagnosis: Destructor Behavior`.

Titles should be concise, descriptive, and useful for future revision. They should identify the assessed concept rather than use opaque sequence-only labels such as `F01`, `T03`, or `Q12`. Keep the category visible while using the remaining title space for an accurate concept label.

## Default type distribution

For a substantial programming quiz where students also complete programming assignments, use approximately:

```text
Foundation 16
Tracing 8
Application 8
Integration 6
Design/Diagnosis 2
```

Scale proportionally for shorter quizzes. This is a default, not a requirement when the module's objectives justify another distribution.

## Question construction

- Ask one primary thing per question unless integration is the stated objective.
- Provide all assumptions needed to determine an answer.
- Use minimal code that still measures the concept.
- Verify traces, outputs, calculations, and answer keys independently.
- Avoid undefined behavior unless diagnosis of undefined behavior is the point.
- Make distractors mutually exclusive, grammatically parallel, and rooted in plausible misconceptions.
- Avoid trick distractors based on incidental punctuation or wording unless syntax precision is the objective.
- Do not use `all of the above` or `none of the above` when they obscure diagnosis.
- Avoid answer-position patterns when practical.

## Code formatting

- Preserve indentation and monospaced presentation.
- For D2L CSV, use the proven formatting supported by the current import method. Do not assume arbitrary HTML will render correctly.
- Ensure line breaks survive import.
- Keep code readable without horizontal scrolling.
- Do not place literal unescaped newlines inside C++ string literals.

## D2L defaults

- Prefer D2L CSV import unless a required feature cannot be represented reliably in CSV.
- Import directly into the target quiz when Question Library reuse is not needed.
- Keep questions in pedagogical order; do not depend on imported sections to preserve progression.
- Do not enable question randomization by default.
- Use concise instructor-only titles in the format `<Category>: <Concept>`.
- Populate D2L Difficulty 1-5 according to the five pedagogical categories.
- Use Blackboard/IMS QTI-style packages, sections, pools, or manual grouping only for a concrete feature need and only after validating the workflow in the active D2L environment.
- Verify import structure against a known-working example when format details matter.

## Key verification

For every question:

1. solve it independently;
2. verify the keyed answer;
3. test plausible alternative interpretations;
4. check distractors for accidental correctness;
5. confirm code formatting after export/import representation;
6. confirm stated category and difficulty.

## Student-facing transparency

Do not promise an error-free quiz. If a defect is discovered during use, correct it consistently and communicate the correction. AI assistance does not transfer responsibility away from the instructor.


## Iterative generation and review

1. Generate the quiz and answer key.
2. Perform a complete review using `review_checklist.md`.
3. Correct all blockers and majors.
4. Regenerate the export when corrections affect ordering, formatting, points, or keys.
5. Re-solve changed questions and rerun global checks for totals, category counts, answer-position patterns, escaping, and import structure.
6. Repeat until no blockers or majors remain, subject to a default cap of three complete automated review cycles.

If the cap is reached, stop and report unresolved issues. Do not label the quiz ready for students. Matthew may authorize more cycles or expedited delivery, but known incorrect keys, privacy failures, or unusable imports remain blockers.
