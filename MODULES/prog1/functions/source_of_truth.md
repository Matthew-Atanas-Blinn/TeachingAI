## Programming Fundamentals I: User-Defined Functions

Status: Approved module source of truth
Course: COSC 1436
Last updated: 2026-11-04

### Purpose

This module is organized around one question:

> How can a program solve a larger problem by building and testing smaller, reusable functions?

The central mental model is:

> Declare -> Call -> Bind -> Execute -> Produce -> Resume -> Test

A function exposes an interface to its caller while keeping local implementation details inside a controlled boundary.

### Prerequisites

Students should understand:
- variables and common C++ types;
- expressions and assignment;
- basic input and output;
- selection structures;
- loops;
- blocks and braces; and
- basic testing and boundary values.

Students are not assumed to understand pointers, raw memory addresses, classes or structures as returned result objects, recursion, advanced overload resolution, or multi-file program organization in depth.

### Learning objectives

Students should be able to:
- explain how functions support decomposition, reuse, independent testing, and readable organization;
- distinguish a function declaration, definition, and call;
- distinguish arguments from parameters;
- trace argument evaluation, parameter initialization, body execution, return, and caller resumption;
- explain that a value-returning function call is an expression;
- explain that `void` is a return type indicating that no value is returned;
- predict the effects of value and reference parameters;
- use const-reference parameters for read-only access when appropriate;
- prefer a returned value when a function naturally calculates one result;
- recognize intentional side effects and hidden dependencies;
- apply local, parameter, block, and static-local scope rules;
- explain why mutable global state can make functions harder to test;
- design a function declaration from a behavioral description;
- create boundary-oriented function tests using a driver;
- explain the temporary purpose of a stub;
- recognize valid and invalid overloads; and
- interpret calls that use default arguments.

### Mental models

#### Function boundary

Caller arguments -> parameter binding -> local execution -> returned value or intentional effect -> caller resumes.

The function interface states what crosses the boundary. Local implementation details remain inside.

#### Value parameter

A value parameter is a new local variable initialized with a copy of an argument's value. Changing the parameter does not change the caller's variable.

#### Reference parameter

A reference parameter is an alias for the caller's existing object. Do not introduce it primarily as receiving a memory address because pointers are not a prerequisite for this module.

#### Const-reference parameter

A const-reference parameter aliases an existing object but does not permit the function to modify that object through the parameter. Small built-in inputs generally remain clearer when passed by value.

#### Returned value

In an expression, a value-returning function call evaluates to the returned value. Prefer a returned value when a function naturally computes one result.

#### Scope and lifetime

Scope answers where a name can be used. Lifetime answers how long an object exists. These ideas interact but are not identical.

### Instructional sequence

- Motivate functions through repeated code or a larger task that needs decomposition.
- Refactor repetition into one named operation.
- Identify return type, function name, parameters, local work, and returned value.
- Distinguish declaration, call, and definition.
- Distinguish arguments and parameters.
- Trace a complete function call.
- Use value-returning calls as expressions.
- Introduce `void` as a return type that produces no returned value.
- Contrast value and reference parameters.
- Introduce const-reference parameters for read-only object access.
- Compare returning one result with modifying an output argument.
- Introduce multiple outputs and side effects.
- Teach local scope, nested block scope, shadowing, mutable global state, and static locals.
- Separate calculation from interaction when that improves responsibility and testing.
- Test functions with drivers, stubs, and boundary cases.
- Diagnose common declaration, parameter, return, and hidden-state defects.
- Introduce overloading.
- Introduce default arguments.
- Reassemble the complete chapter mental model.

### Scope boundaries

#### Core assessed material

- motivation and decomposition;
- declarations, definitions, and calls;
- arguments and parameters;
- value-returning and `void` functions;
- value and reference parameters;
- const-reference parameters;
- return values versus output parameters;
- side effects;
- local and block scope;
- shadowing;
- avoiding mutable global state;
- driver programs and boundary testing; and
- common interface and return defects.

#### Secondary assessed material

- static local variables;
- function overloading; and
- default arguments.

#### Deferred material

- pointers and pointer parameters;
- returning structs, classes, tuples, or other aggregate results;
- recursion;
- function pointers and lambdas;
- templates;
- advanced overload resolution;
- rvalue references and move semantics;
- full header/source build architecture;
- `extern` and namespace-level linkage rules; and
- the comma operator in return statements.

### Assessment guidance

- Give substantial weight to tracing calls and predicting caller state.
- Assess interface selection and intent, not merely vocabulary.
- Include diagnosis of declaration-definition mismatches, missing return paths, inappropriate parameter modes, and hidden global dependencies.
- Treat static locals, overloading, and default arguments as smaller extension topics.
- Do not assess pointer mechanics or raw addresses.
- Do not present reference output parameters as the universal best method for multiple results.
- Avoid obscure conversion or overload-resolution rules.
- Quizzes should complement programming assignments by emphasizing foundations, tracing, application, integration, and diagnosis rather than duplicating full program construction.

### Slide coverage

A complete slide implementation should include motivation, the function-boundary mental model, declarations/calls/definitions, argument and parameter tracing, return values, `void`, value/reference/const-reference comparison, side effects, scope and state, drivers and stubs, boundary testing, common bugs, overloading, default arguments, retrieval practice, and a final integrated model.

### Quiz mapping

A substantial quiz may use the established 16-8-8-6-2 distribution:
- 16 Foundation;
- 8 Tracing;
- 8 Application;
- 6 Integration; and
- 2 Design/Diagnosis.

Core parameter and call behavior should receive more weight than extension topics.

### Future connections

- Arrays passed to functions will complicate the copy-versus-alias model.
- Classes will allow related results to be returned together as one object.
- Header/source separation will expand the declaration-versus-definition model.
- Recursion will require tracing multiple active calls.
- Function templates will generalize compatible operations across types.
- Member functions will place behavior inside class scope.

### Unresolved questions

- Assignment alignment should be reviewed when the corresponding functions programming assignment is revised.
- The final global light-versus-dark code-panel convention should be reconsidered only after comparing multiple approved decks; the current Chapter 6 deck predates the newer visual default and does not require immediate modification.
