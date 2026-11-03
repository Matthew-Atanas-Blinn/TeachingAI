# Enums, Namespaces, and Type Aliases Review Checklist

## Architecture

- [ ] The module begins with naming problems rather than disconnected syntax.
- [ ] Scope review precedes namespaces and scoped enums.
- [ ] Out-of-scope, shadowed, and ambiguous names are distinguished.
- [ ] Enums, namespaces, and aliases are presented as different tools.

## Enumerations

- [ ] A categorical problem motivates the enum.
- [ ] Category, quantity, and yes/no values are distinguished.
- [ ] Traditional enum appears before `enum class` when the comparison is taught.
- [ ] Traditional enumerator collisions are demonstrated accurately.
- [ ] `enum class` becomes the preferred form afterward.
- [ ] Type, variable, scope, operator, and enumerator are distinguished.
- [ ] Input is validated or mapped before becoming an enum value.
- [ ] Display text is produced explicitly.
- [ ] Enum arithmetic and arbitrary integer casting are not normal designs.
- [ ] Enum iteration is deferred to arrays or uses an explicit array of valid values.

## Namespaces

- [ ] `std::cout` is explained as `cout` selected from namespace `std`.
- [ ] `::` is not described as exclusively a namespace operator.
- [ ] `Direction::north` uses the same scope-resolution model.
- [ ] Qualification, using declarations, and using directives are accurately distinguished.
- [ ] At least one ambiguity example shows why qualification can be necessary.

## Type aliases

- [ ] Modern `using` syntax is taught.
- [ ] `typedef` remains recognition-level.
- [ ] The material explicitly states that an alias does not create a new type.
- [ ] At least one example demonstrates compatibility between aliases with the same underlying type.
- [ ] Alias examples communicate meaningful roles.
- [ ] A using declaration is distinguished from a type alias declaration.
