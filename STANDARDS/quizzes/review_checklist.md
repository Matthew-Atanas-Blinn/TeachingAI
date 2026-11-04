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
- [ ] The correct answer is not uniquely signaled by a comment, label, explanatory annotation, extra specificity, unusual length, or different formatting.
- [ ] Comments or annotations are removed unless they are necessary to the assessed concept and applied without revealing the key.

## F. Formatting and D2L

- [ ] Every code-related occurrence was classified from local meaning as ordinary prose, inline code, or block code.
- [ ] Ordinary English words are not styled merely because they match code words used elsewhere.
- [ ] Complete statements, declarations, parallel code alternatives, function definitions, and multi-line fragments use block panels.
- [ ] Short code embedded in prose uses inline styling.
- [ ] Each meaningful expression, declaration, parameter, or state description remains contiguous within one inline span.
- [ ] Identifiers referenced in prose immediately before or after a code block use inline code styling consistently.
- [ ] Mixed stems were checked in both places: the prose lead-in and the code block.
- [ ] Every stem expected to contain code was verified to contain a block panel; validation did not inspect only already-formatted stems.
- [ ] Every answer choice was checked individually when any option contains code.
- [ ] Parallel code choices use parallel formatting, including malformed code distractors.
- [ ] Function definitions use conventional line breaks and indentation rather than one-line compression.
- [ ] D2L CSV uses HTML formatting rather than Markdown fences.
- [ ] Every formatted `QuestionText` and `Option` record contains the required `HTML` format field.
- [ ] HTML-sensitive C++ characters and CSV quotation marks are escaped correctly.
- [ ] Block panels preserve indentation and line breaks with `white-space: pre-wrap`.
- [ ] Inline code remains inline and does not expand to the full line.
- [ ] No raw Markdown fence characters are visible in the imported student view.
- [ ] Structural validation checked question count, key count, IDs, points, difficulty, ordering, and HTML markers.
- [ ] Semantic validation reviewed every stem and option, not only aggregate counts or regex matches.
- [ ] A known-working D2L CSV was used as the structural reference.
- [ ] A test import or representative student-view inspection was performed when practical.
- [ ] Question titles remain instructor-only where intended.
- [ ] Questions appear in the intended order after import.

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
