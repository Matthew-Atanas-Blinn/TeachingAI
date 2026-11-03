# Quiz Review Checklist

## Severity

- **Blocker:** incorrect key, privacy exposure, unusable import, or assessment of material outside the approved source.
- **Major:** ambiguity, accidental multiple correct answers, broken code formatting, substantial coverage gap, or misleading difficulty/category.
- **Minor:** wording or formatting refinement that does not affect validity or usability.

## A. Coverage and alignment

- [ ] Every question maps to a current objective.
- [ ] Every assessed concept was introduced and reasonably practiced.
- [ ] Removed or superseded slide content is absent.
- [ ] Coverage and points reflect the intended emphasis.
- [ ] The quiz complements rather than duplicates programming assignments unnecessarily.

## B. Progression

- [ ] Questions follow Foundation -> Tracing -> Application -> Integration -> Design/Diagnosis unless a documented reason says otherwise.
- [ ] Instructor titles follow `<Category>: <Concept>`.
- [ ] Titles concisely and accurately identify the assessed concept for future revision.
- [ ] Titles avoid opaque sequence-only labels unless a documented workflow requires them.
- [ ] Difficulty labels match actual cognitive demand and the category-to-difficulty mapping.
- [ ] Question order has not been randomized when dependencies or progression matter.
- [ ] Category counts approximately match the intended distribution.

## C. Correctness

- [ ] Each question was solved independently.
- [ ] Every answer key is correct.
- [ ] Code compiles or is clearly intended as a snippet/pseudocode.
- [ ] Output and traces are correct.
- [ ] No question accidentally relies on undefined, unspecified, or implementation-dependent behavior.
- [ ] Numerical and logical boundary cases were checked.

## D. Wording and ambiguity

- [ ] The stem asks one clear question.
- [ ] Necessary assumptions are explicit.
- [ ] No irrelevant wording changes the answer.
- [ ] Pronouns and references have clear antecedents.
- [ ] Terminology matches instruction.
- [ ] More than one answer cannot reasonably be defended unless multiple answers are intentionally allowed.

## E. Distractors

- [ ] Distractors are plausible misconceptions, not random noise.
- [ ] Distractors are mutually exclusive.
- [ ] Distractors are grammatically parallel with the stem.
- [ ] No distractor is accidentally correct under a reasonable interpretation.
- [ ] Correct-answer positions do not form an obvious sequence or block pattern, including all/nearly all one letter, long runs, repeated cycles such as A-B-C-D, blocks such as questions 1-10 = A and 11-20 = B, or a strong concentration in one position.
- [ ] Changing answer positions has not altered the keyed answer or broken grammatical consistency.
- [ ] Answer-position balancing did not take priority over correctness or distractor quality.

## F. Formatting and D2L

- [ ] Code indentation and line breaks survive the selected import format.
- [ ] Question titles are instructor-only where intended.
- [ ] Point values and answer indicators are valid.
- [ ] Special characters, quotes, commas, and newlines are correctly escaped.
- [ ] A test import or structural validation was performed when practical.
- [ ] Questions appear in the intended order after import.
- [ ] D2L CSV is used by default, or the concrete need for another format is documented and validated.
- [ ] Instructor-only titles remain hidden in the active student quiz view when that behavior is relied upon.
- [ ] No section, pool, or package complexity was added without a specific instructional or operational benefit.

## G. Final report

Report:

- question count by category and difficulty;
- objectives covered;
- key corrections made during review;
- unresolved ambiguities;
- import validation performed;
- assumptions and experimental rules used.


## H. Correction and regression loop

- [ ] Every blocker and major issue was corrected.
- [ ] Every changed question was solved again independently.
- [ ] Answer totals, points, category counts, answer-position patterns, escaping, and import structure were rechecked globally.
- [ ] The export was regenerated and structurally validated when applicable.
- [ ] Review repeated until no blockers or majors remained, or the three-complete-cycle safety cap was reached.
- [ ] If the cap was reached, unresolved issues were reported and the quiz was not labeled ready.
