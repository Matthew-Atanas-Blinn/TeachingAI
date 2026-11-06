# Required Accessibility

## Principle

Accessibility is a design constraint, not a final cosmetic pass. Materials should remain understandable across projectors, displays, printouts, color-vision differences, and common assistive technologies.

## Universal requirements

- Do not communicate essential meaning through color alone. Pair color with labels, position, outlines, emphasis, symbols, or wording.
- Maintain readable contrast between text and its immediate background.
- Do not assume that colors that look distinct on one monitor will remain distinct on a classroom projector.
- Use legible font sizes and avoid dense text or code that requires students to read fine detail at a distance. For projected instructional slides, use 18 pt as the normal minimum for supporting text and code, while titles should be substantially larger. Smaller text is reserved for non-instructional metadata or a documented approved exception.
- Verify color contrast on every local background. Target WCAG 2.2 AA contrast: at least 4.5:1 for normal text and 3:1 for large text (at least 18 pt regular or 14 pt bold).
- Do not depend on color alone. Pair semantic color with position, labels, borders, weight, or other non-color cues. Avoid underlining code for semantic emphasis because it can be confused with underscores and adds visual clutter; prefer bold weight, nearby labels, matching borders, or restrained background emphasis.
- Use descriptive headings, logical reading order, and meaningful alternative text where the format supports it.
- Avoid unnecessary motion, flashing, and transitions that interfere with comprehension.
- Preserve visible keyboard focus and semantic structure in interactive materials.
- Do not use images of text when real text is practical, particularly for essential instructions.

## Color and code

- Prefer a light-gray or similarly light neutral code panel with dark base text unless a different treatment has a compelling, verified accessibility advantage.
- When explanatory points and code use matching visual categories, use accessible colors tuned to each local background. Exact hex matches are not required; visibly related color families are acceptable.
- Retain a non-color cue, such as bolding, underlining, boxes, labels, or spatial grouping.
- Verify that syntax highlighting does not make comments, punctuation, or important tokens unreadable.

## Review expectations

Review the final rendered artifact, not only its source representation. Check typical classroom scale and, when possible, the actual projection environment. Automated contrast checks are useful but do not replace checking hierarchy, legibility, or whether meaning depends solely on color.

## Assumption

This file states durable operational requirements rather than claiming exhaustive compliance with every jurisdiction or standard. Institutional accessibility policy and current legal requirements take precedence.
