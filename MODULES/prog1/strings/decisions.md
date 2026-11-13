## Strings and C-strings Decisions

### Status
Decision stub. The direction below is approved, but the complete module has not yet been designed.

### Decision 1: Place strings after arrays
Status: Accepted
Date: 2026-11-12
Arrays provide indexed storage, traversal, bounds, and fixed-capacity prerequisites for understanding character-array representations.

### Decision 2: Include C-strings within the strings module
Status: Accepted
Date: 2026-11-12
Teach std::string and C-strings as two representations of text at different abstraction levels. Keep std::string as the preferred ordinary representation.

### Decision 3: Keep C-string depth introductory
Status: Accepted
Date: 2026-11-12
Future coverage should include char arrays, the null terminator, capacity versus text length, short literal representation, basic traversal, assignment/comparison differences from std::string, limited library use, and why std::string is generally preferable. Do not attempt comprehensive C-string programming.

### Decision 4: Record current material misalignment
Status: Accepted
Date: 2026-11-12
The existing strings slides do not include C-strings. They remain usable for their current std::string coverage, but they do not yet implement the approved final course sequence. Revise them before claiming that the module is aligned.

### Undecided details
Objectives, exact function coverage, input safety depth, slide sequence, assignment scope, quiz scope, and review checklist must be completed before substantial module revision.

#### Decision 5: Fall 2026 temporary assessment exception

Status: Accepted
Date: 2026-11-13

For Fall 2026, the strings quiz must assess only the `std::string` material actually taught in the current slides. It must not assess C-strings, character-array text representation, null terminators, C-string library functions, or related safety rules. Introductory C-string material may appear on the Fall 2026 final examination only after students receive explicit instruction and reasonable practice before that examination.

This is a temporary semester-alignment note, not a change to the durable decision that introductory C-strings belong inside the strings module. Before the next semester in which strings will be taught, an AI working from this repository must explicitly ask Matthew to authorize discarding this temporary note and updating the strings slides, module source of truth, review checklist, quiz, and related materials so C-strings are taught within the module before its assessment. The AI must not silently carry this exception into another semester or remove it without Matthew's approval.
