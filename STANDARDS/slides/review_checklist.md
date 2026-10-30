# Slide Review Checklist

Use this checklist on the final rendered deck. The AI should perform and report a preflight review before instructor review. The instructor may skim based on risk, but the AI must not claim perfection.

## Severity

- **Blocker:** privacy exposure, corrupt/unusable file, materially false instruction, missing required content, or content outside the approved source of truth.
- **Major:** overlap/clipping that impairs comprehension, inaccessible required content, incorrect code/diagram/output, code-explanation mismatch, or substantial inconsistency.
- **Minor:** wording or cosmetic refinement that does not affect correctness, accessibility, comprehension, consistency, or professional usability.

## A. Architecture and pedagogy

- [ ] The deck follows the relevant module source of truth.
- [ ] Prerequisites appear before dependent concepts.
- [ ] The sequence moves coherently from motivation/foundation toward application.
- [ ] Each slide has one identifiable instructional purpose.
- [ ] Examples and activities support stated objectives.
- [ ] Important misconceptions or boundaries are addressed where appropriate.
- [ ] Removed or outdated content is not still implied by summaries or examples.

## B. Code and explanation mapping

- [ ] Every bullet or callout that references code clearly maps to the relevant token, line, or region.
- [ ] Teaching categories use matching visual families across bullets and code.
- [ ] Essential relationships have a non-color cue.
- [ ] Syntax highlighting does not compete with instructional highlighting.
- [ ] Code panel colors remain readable against the panel background.
- [ ] Code text is sufficiently large for classroom projection.
- [ ] Line numbers, if present, match the narration.

## C. Code correctness

- [ ] Code is syntactically valid or clearly marked as pseudocode/incomplete.
- [ ] Output and traces match the code.
- [ ] Types, values, indices, scopes, and object states are accurate.
- [ ] C++ string literals use escaped newlines or `std::endl`, not accidental literal line breaks.
- [ ] Examples do not depend on an unmentioned compiler extension or undefined behavior.

## D. Diagrams and visuals

- [ ] Each visual has a clear instructional role.
- [ ] Arrows point to the intended object and do not cross ambiguously.
- [ ] Labels match both the graphical element and the narration.
- [ ] Data-structure state and transitions are technically correct.
- [ ] Visual encodings are consistent across the deck.
- [ ] No important component is hidden behind another object.
- [ ] No generated visual contains misleading or malformed pseudo-text.

## E. Layout integrity

- [ ] No text, code, image, diagram, citation, or shape overlaps unintentionally.
- [ ] Nothing is clipped, off-slide, or outside safe margins.
- [ ] Reading order is obvious.
- [ ] Related items are spatially grouped.
- [ ] Text density is reasonable.
- [ ] Titles, body text, labels, and code use consistent sizing and alignment.
- [ ] The slide remains readable in presentation view, not merely when zoomed in for editing.

## F. Accessibility and projection

- [ ] Meaning does not rely on color alone.
- [ ] Text and code have sufficient local contrast.
- [ ] Similar categories remain distinguishable under common color-vision differences.
- [ ] The light-gray code panel default is used unless an alternative has a documented reason.
- [ ] Thin lines, pale labels, and small annotations remain visible on a projector.
- [ ] Images and diagrams have appropriate descriptions when needed.
- [ ] Motion and transitions do not impede understanding.

## G. Cross-slide consistency

- [ ] Terminology and notation stay consistent.
- [ ] Colors retain the same meaning when reused.
- [ ] Examples do not contradict earlier rules.
- [ ] Agenda, objectives, section dividers, summaries, and conclusion agree on coverage.
- [ ] References to previous or next slides are correct after reordering.

## H. Sources and disclosure

- [ ] External facts, images, and quotations are appropriately cited.
- [ ] AI-generated images are disclosed as required.
- [ ] No student information appears in examples, notes, filenames, or metadata.

## I. Delivery report

Report:

- slides inspected;
- issues found and fixed;
- unresolved issues and their slide numbers;
- assumptions;
- experimental rules used;
- changes from the reference deck, including removed topics that appeared in the reference.


## J. Correction and regression loop

- [ ] Every blocker and major issue was corrected.
- [ ] The deck was rendered again after corrections.
- [ ] Every modified slide was rechecked.
- [ ] Neighboring and dependent slides were checked for regressions.
- [ ] Global checks for overlap, clipping, terminology, colors, references, and file validity were rerun.
- [ ] The process repeated until no blockers or majors remained, or the three-complete-cycle safety cap was reached.
- [ ] If the cap was reached, unresolved issues and the reason for non-convergence were reported; the deck was not labeled complete.
- [ ] Deferred minor issues were reported.
