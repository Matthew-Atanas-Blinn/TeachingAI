# C++ Instructional Content Standard

## Scope

This standard applies across Programming Fundamentals I, II, and III whenever slides, quizzes, assignments, starter code, demonstrations, autograders, grading guidance, or examples contain C++.

## Namespace convention

Short standalone instructional `.cpp` programs may use:

```cpp
using namespace std;
```

Use this convenience when it reduces incidental syntax and keeps attention on the current learning objective.

Students must still learn:

- that standard-library names belong to namespace `std`;
- that `std::cout` selects `cout` from the `std` namespace;
- what the scope-resolution operator means;
- the difference between explicit qualification, a using declaration, and a using directive; and
- why broad namespace imports become riskier as codebases and dependencies grow.

Do not place `using namespace std;` in:

- instructor-provided headers;
- reusable library interfaces;
- shared framework code; or
- examples whose objective is explicit qualification or namespace ownership.

Larger or reusable examples should prefer explicit qualification or appropriately scoped targeted using declarations.

Do not deduct points solely because a student uses `using namespace std;` in a short standalone `.cpp` file unless namespace discipline is an explicit requirement. A deduction may be appropriate when the directive appears in a submitted header, violates an explicit specification, causes a conflict, or is unsuitable for a reusable interface.

## Enum convention

- Teach traditional enums when needed for recognition or to motivate the safer scoped form.
- Prefer `enum class` in new instructional code after the comparison has been established.
- Do not imply that enums are automatically iterable.
- Do not teach arbitrary integer casting or enum arithmetic as the normal design.
- When iteration is needed after arrays have been introduced, prefer an explicit array of valid enum values unless another representation has a clear instructional purpose.

## Type aliases

- Prefer `using` for new aliases.
- Teach `typedef` only when recognition is needed.
- State explicitly that an alias does not create a distinct compiler type.
- Use aliases when the name communicates a meaningful domain role or simplifies a genuinely complicated type.

## Generated-code validity

- Keep examples valid for the stated toolchain and language level.
- Do not place literal newline characters inside C++ string literals. Use escaped `\n` or `std::endl` as appropriate.
- Do not depend on undefined behavior or an unmentioned compiler extension.
- Preserve required filenames, function signatures, and interfaces exactly when they are part of an assignment or test contract.
