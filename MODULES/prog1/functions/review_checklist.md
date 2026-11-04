## User-Defined Functions Review Checklist

### Architecture
- [ ] The module begins with a problem, repeated operation, or decomposition need.
- [ ] Declaration, call, and definition are distinguished.
- [ ] Students trace a complete call before designing complex interfaces.
- [ ] Parameters and return values appear before scope extensions.
- [ ] Overloading and default arguments appear after the core model.

### Terminology and mental models
- [ ] `void` is described as a return type indicating no returned value.
- [ ] Arguments belong to calls; parameters belong to declarations and definitions.
- [ ] A value-returning call is described as an expression.
- [ ] References are described as aliases rather than address containers.
- [ ] Scope and lifetime are distinguished when both are discussed.
- [ ] Control resumes in the caller immediately after a function returns.

### Parameter behavior
- [ ] Value parameters use a distinct-copy model.
- [ ] Reference parameters use a shared-object or alias model.
- [ ] Const-reference parameters are read-only through that parameter.
- [ ] Small built-in inputs generally use value parameters.
- [ ] Non-const references communicate intentional caller modification.
- [ ] A returned value is preferred for one natural result.
- [ ] Multiple-output examples state that output references create side effects.

### Scope and state
- [ ] Parameters and local variables are scoped correctly.
- [ ] Shadowing examples use genuinely distinct variables.
- [ ] Mutable global state is presented as a hidden dependency.
- [ ] Static locals are described as local in scope but retained across calls.
- [ ] Static-local traces account for every prior call.

### Testing and design
- [ ] Drivers contain meaningful typical and boundary cases.
- [ ] Stubs are clearly temporary and incomplete.
- [ ] Expected values are independently verified.
- [ ] Calculation and interaction are separated when it improves responsibility and testing.
- [ ] One defect does not unnecessarily invalidate unrelated evidence.

### Extensions
- [ ] Overloads differ in their parameter lists.
- [ ] No item implies that return type alone can distinguish overloads.
- [ ] Defaulted parameters are trailing parameters.
- [ ] Calls using defaults are unambiguous at the students' level.
- [ ] Advanced overload conversions and binding rules remain outside scope.

### Artifact alignment
- [ ] Slides, quizzes, assignments, and examples assess only current module content.
- [ ] Core parameter and call behavior receives more emphasis than extension topics.
- [ ] Pointer mechanics, raw addresses, recursion, and advanced multi-file rules are absent unless explicitly introduced as future connections.
- [ ] Quiz titles, difficulties, order, and import format follow the active quiz standards.
