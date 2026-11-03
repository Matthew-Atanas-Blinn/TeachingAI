# Programming Fundamentals I: Enums, Namespaces, and Type Aliases

Status: Approved module source of truth
Course: COSC 1436
Last updated: 2026-11-02

## Purpose

This module unifies several small C++ topics through one question:

> How can a program give names the correct meaning in the correct place?

The three tools solve different naming problems:

- an enumeration names the valid values of a categorical type;
- a namespace creates a named scope for related declarations; and
- a type alias gives an existing type another name.

## Prerequisites

Students should understand variables, data types, block and function scope, selection structures, `switch`, functions, parameters, return values, and basic input/output.

## Learning objectives

Students should be able to:

1. distinguish names that are out of scope, shadowed, ambiguous, or qualified;
2. explain qualification as selecting a name from a specified scope;
3. identify when a value represents a fixed categorical set;
4. recognize and use a traditional enum;
5. explain the scope and type-safety limitations of a traditional enum;
6. define and use `enum class` as the preferred form for new code;
7. use enum values in assignments, comparisons, functions, and `switch` statements;
8. validate ordinary input before converting it to an enum value;
9. convert enum values explicitly to display text;
10. explain how namespaces organize names and prevent conflicts;
11. interpret `std::cout` as `cout` from namespace `std`;
12. compare explicit qualification, using declarations, and using directives;
13. define a type alias with `using`;
14. explain that an alias does not create a distinct compiler type; and
15. distinguish a using declaration from a type alias declaration.

## Mental models

### Names live in scopes

- Out of scope: the declaration is not visible from the current location.
- Shadowed: a nearer declaration hides an outer declaration.
- Ambiguous: more than one accessible declaration can match.
- Qualified: the source identifies which scope to search.

Read `std::cout` as `cout` from namespace `std`, and read `Direction::north` as `north` from the scope of `Direction`. The left side of `::` identifies a scope; it is not always a namespace.

### Enums model categories

Use an enum when the choices are fixed, discrete, categorical, and meaningfully named. Use numeric types for quantities and usually use `bool` for a simple yes/no condition.

### Aliases name roles, not new types

`using StudentId = unsigned long long;` makes a role visible, but `StudentId` remains the same compiler type as `unsigned long long`.

## Instructional sequence

1. Begin with an unexplained numeric code, two declarations with the same name, and an underlying type whose role is unclear.
2. Review block and function scope.
3. Contrast out-of-scope, shadowed, and ambiguous names.
4. Introduce traditional enums as a solution to magic values.
5. Expose traditional enumerator collisions.
6. Introduce `enum class` as the scoped solution.
7. Apply enum values to comparison, `switch`, parameters, return values, validated input, and display conversion.
8. Return to familiar code using `using namespace std;`.
9. Reveal namespace `std` and the meaning of `::`.
10. Compare qualification, targeted using declarations, and using directives.
11. Introduce type aliases as role-oriented names for existing types.
12. Contrast aliases with enums and distinct types.
13. Integrate all three tools in one example.
14. End with selection and diagnosis activities.

## Scope boundaries

Include scope review, traditional enums, `enum class`, enum use in functions and `switch`, validated input conversion, display conversion, namespace `std`, scope resolution, using declarations, using directives, type aliases, `typedef` recognition, and comparison of the three naming tools.

Defer namespace aliases, anonymous namespaces, inline namespaces, `using enum`, alias templates, enum underlying storage types, bitmask enums, enum arithmetic, arbitrary enum/integer conversion, reflection utilities, custom stream operators, and enum iteration.

## Future connections

- The arrays module will use an explicit array of enum values. The enum defines valid values; the array defines membership and traversal order.
- Scope resolution reappears with class members in Programming Fundamentals II.
- Type aliases become more useful with containers, iterators, templates, and complicated types.
- Character arrays and C-strings follow raw array fundamentals.

## Assessment guidance

Emphasize representation selection, qualified-name interpretation, enum-based selection tracing, scope diagnosis, namespace-strategy comparison, and the fact that aliases are not distinct types.

Do not emphasize obscure conversion rules, namespace aliases, enum arithmetic, or artificially complicated aliases.

## Unresolved questions

- Final quiz length and weighting.
- Whether the module receives a standalone programming exercise or only integrated practice.
