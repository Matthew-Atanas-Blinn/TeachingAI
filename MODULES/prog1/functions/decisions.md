## Module Decisions: User-Defined Functions

### Decision 1: Organize the module around the function boundary

Status: Accepted
Date: 2026-11-04

Teach functions through the movement of control and information across a controlled boundary rather than as a collection of syntax categories. Use Declare -> Call -> Bind -> Execute -> Produce -> Resume -> Test as the module's integrated model.

This unifies calls, parameters, returns, scope, side effects, and testing. Some textbook terminology appears later than in the original chapter sequence so that terminology follows a usable execution model.

### Decision 2: Explain reference parameters as aliases

Status: Accepted
Date: 2026-11-04

Introduce a reference parameter as another name for the caller's object, not primarily as a received memory address. Students have not yet learned pointers. Later courses may connect aliasing behavior to implementation-level memory concepts.

### Decision 3: Prefer a returned value for one natural result

Status: Accepted
Date: 2026-11-04

When a function conceptually calculates one result, prefer returning that result instead of modifying an output parameter. Reference output parameters remain appropriate when the task intentionally requires multiple outputs or caller modification.

### Decision 4: Treat static locals, overloading, and defaults as extensions

Status: Accepted
Date: 2026-11-04

Teach static local variables, function overloading, and default arguments after students can trace ordinary calls, parameters, returns, and local scope. These language features are assessed with less weight than the core function model.

### Decision 5: Do not retroactively restyle the approved Chapter 6 deck

Status: Accepted
Date: 2026-11-04

The light-neutral code-panel default was approved after the current Chapter 6 deck was generated. The deck does not require immediate restyling solely because the later default differs. Revisit the global implementation choice after comparing several approved decks and projector results.
