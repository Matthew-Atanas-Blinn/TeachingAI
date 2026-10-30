# Slide Generation Standard

## Goal

Create presentation materials that help students follow a coherent explanation in class. Slides are instructional supports, not self-contained textbooks and not decorative summaries.

## Before generation

1. Read the relevant module source of truth and course file.
2. Identify the motivating problem, objectives, prerequisites, likely misconceptions, examples, and assessment connections.
3. Plan the conceptual sequence before designing individual slides.
4. For every content slide, decide what visual form best supports that slide: code, diagram, comparison, worked example, image, process, or text. Do not add a visual merely to fill space.
5. Identify facts, code, calculations, and diagrams that require verification.

## Instructional sequence

- Prefer motivation or a concrete problem before terminology and syntax.
- Build from prior knowledge toward use, tracing, integration, and design.
- Explain why a construct is useful, how it works, and where it can fail.
- Include misconceptions and boundary cases when they are instructionally important.
- Keep a slide focused on one coherent instructional purpose.

## Default visual system

Use a consistent base style across Programming Fundamentals I, II, and III. Course-specific accents may vary, but typography, semantic colors, code treatment, spacing, and component behavior should remain recognizable.

### Canvas and structure

- Use standard widescreen 16:9 unless an existing approved delivery environment requires another ratio.
- Maintain consistent safe margins and a fixed title region.
- Prefer one primary content region and, when needed, one supporting region rather than many competing panels.
- Keep recurring elements such as section labels, footers, slide numbers, and source notes in consistent positions.
- Do not shrink content below readable sizes merely to avoid restructuring a slide.

### Typography

- Use one approved sans-serif family for titles and body text and one approved monospaced family for code.
- Use consistent title, section, body, annotation, and code size tiers.
- Preserve a clear weight hierarchy. Avoid using many font sizes or styles on one slide.
- Exact fonts and point sizes are `TODO` pending extraction from approved final decks. Until then, match the current approved reference deck and preserve projector readability.

### Color system

- Use a stable neutral background and high-contrast primary text.
- Use the light-gray code panel default with dark base code text.
- Reserve semantic accent families for recurring meanings such as instructional categories, warnings, correct states, and neutral structure.
- The same color should retain the same instructional meaning within a deck.
- Course accents must not redefine semantic colors or reduce contrast.
- Exact palette values are `TODO` pending extraction and accessibility checking from approved final decks.

### Components

Use consistent treatments for:

- code panels;
- prediction or discussion prompts;
- callout boxes;
- comparisons;
- diagrams and labels;
- section dividers;
- summaries and takeaways;
- citations and speaker-note sources.

A reference deck may add styling only after its readability, accessibility, and component consistency are checked.

## Code and explanation correspondence

When bullets, callouts, or narration discuss parts of code, the styling must make the relationship visible.

Example categories for:

```cpp
int x = 5;
char y = 'A';
```

- `Types` corresponds to `int` and `char`.
- `Variables` corresponds to `x` and `y`.
- `Values` corresponds to `5` and `'A'`.

Use matching visual families between explanatory points and the relevant code. Exact shades may differ because the bullet area and code panel have different backgrounds. The relationship must remain obvious. Add a non-color cue when the mapping is essential.

Do not color unrelated syntax in ways that compete with the teaching categories. If ordinary syntax highlighting conflicts with instructional highlighting, simplify it.

## Code panel styling

- Default to a light-gray or light neutral panel with dark base text.
- Use a monospaced font and sizes readable from the back of a classroom.
- Avoid horizontal scrolling, excessive line length, tiny text, or code that is too large for the slide.
- Show only enough surrounding code to understand the target concept.
- Use line numbers only when the narration or activity refers to them.
- Verify code syntax, output, and trace results.

## Visuals and diagrams

- Every visual must support a stated instructional purpose.
- Labels, arrows, highlights, and narration must refer to the correct objects.
- Preserve spatial logic. Processes should flow consistently; data-structure diagrams should accurately show ownership, links, indices, and state.
- Avoid decorative complexity and invented details.
- Use consistent visual encodings across slides unless a change is explicitly explained.
- Do not reuse the same large image repeatedly when a new visual is needed.

## Layout and hierarchy

- Establish a clear reading order.
- Keep titles, key ideas, explanation, example, and takeaway visually distinct.
- Use whitespace deliberately, but do not leave a slide looking unfinished.
- Prevent overlaps, clipping, off-slide content, tiny footnotes, and ambiguous arrows.
- Keep related objects close and unrelated objects separated.
- Maintain consistent margins, alignment, and component styles.

## Accessibility and projection

Follow `REQUIRED/accessibility.md`. In particular:

- do not rely on color alone;
- tune colors for their local backgrounds;
- use projector-readable contrast and text size;
- avoid dark low-contrast text on dark code panels;
- use concise alternative text or speaker-note description when appropriate.

## Cognitive load

- Remove ornamental elements that compete with the point.
- Avoid placing a full paragraph, complex diagram, and large code sample on the same slide.
- Reveal a complex process in meaningful stages only when the final state remains understandable.
- Keep terminology stable.
- Use worked examples whose incidental difficulty does not exceed the target concept.

## Speaker notes and sources

- Use speaker notes for explanation, prompts, likely misconceptions, and transitions that do not need to appear on the slide.
- Cite external facts and visuals in the required source-note format.
- Mark AI-generated visuals according to the active slide-production requirements.

## Common AI failure modes to prevent

- code highlighting that does not match the explanation;
- inaccessible colors on local backgrounds;
- labels or arrows attached to the wrong component;
- diagrams whose state contradicts the code or narration;
- overlapping, clipped, or off-canvas objects;
- output that does not match the code;
- repeated or generic visuals with no instructional role;
- plausible but incorrect examples;
- topic order that assumes an unintroduced prerequisite;
- headings or summaries that overstate what the slide demonstrates;
- visual polish that hides conceptual ambiguity.

## Iterative generation and review

Generation means producing, rendering, reviewing, correcting, and regression-checking the deck, not merely creating the editable file.

1. Generate and render the full deck.
2. Perform one complete checklist review.
3. Fix every blocker and major issue.
4. Render again.
5. Recheck every modified slide, neighboring or dependent slides, and global structural checks such as overlap, clipping, terminology, colors, and references.
6. Repeat while blockers or major issues remain, subject to the safety cap below.

Default safety cap: three complete automated review cycles. Targeted post-fix checks do not count as a complete cycle. If blockers or major issues remain after the cap, stop, report them, explain why convergence failed, and do not describe the deck as complete. Matthew may authorize more cycles or expedited delivery.

Minor issues may be deferred only when they do not affect correctness, accessibility, comprehension, consistency, or professional usability, and they must be reported.

## Final generation requirement

Generation is not complete until the deck has passed `review_checklist.md` with no unresolved blockers or majors, or Matthew explicitly accepts an expedited delivery with disclosed unresolved issues.
