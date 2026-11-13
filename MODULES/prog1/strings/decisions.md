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
