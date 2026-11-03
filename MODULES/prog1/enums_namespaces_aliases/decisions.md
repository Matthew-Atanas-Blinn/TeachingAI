# Module Decisions: Enums, Namespaces, and Type Aliases

## Decision 1: Unify the topics through naming

Status: Accepted
Date: 2026-11-02

Teach enums, namespaces, and type aliases in one module organized around giving names appropriate meaning and ownership. Separate decks would be too small and would hide the shared connection.

## Decision 2: Teach scope before namespace syntax

Status: Accepted
Date: 2026-11-02

Connect namespaces and scoped enums to students' prior understanding of block and function scope. Distinguish out-of-scope, shadowed, ambiguous, and qualified names before formal namespace syntax.

## Decision 3: Traditional enum before enum class

Status: Accepted
Date: 2026-11-02

Use a traditional enum to solve magic numeric values, then use collisions and weak type behavior to motivate `enum class`. Prefer `enum class` afterward. This supports legacy-code recognition while explaining why the safer form exists.

## Decision 4: Defer enum iteration to arrays

Status: Accepted
Date: 2026-11-02

Do not teach integer-cast enum loops as the normal technique. After arrays are introduced, iterate over an explicit array of valid enum values. The enum defines the valid category; the array defines membership and order.
