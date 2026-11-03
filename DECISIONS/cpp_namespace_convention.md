# Decision: Namespace Convention for Instructional C++

Status: Accepted
Date: 2026-11-02
Scope: Cross-course

## Context

Short instructional C++ programs repeatedly use standard-library names. Explicit `std::` qualification makes ownership visible but adds syntax that may compete with the concept currently being taught.

## Decision

Short standalone instructional `.cpp` programs may use `using namespace std;` when the reduced syntax supports the current learning objective.

Students must still learn what the directive does, what `std::` means, and why broad imports become riskier as codebases grow.

Instructor-provided headers, reusable interfaces, and shared framework code must not contain `using namespace std;`. Larger code should prefer explicit qualification or narrowly scoped using declarations.

Do not deduct points solely for course-approved use in a short standalone `.cpp` file unless namespace discipline is an explicit objective.

## Benefits

- Reduces repeated syntax in short examples.
- Supports concise live coding.
- Preserves attention for the current objective.
- Matches established classroom practice.

## Drawbacks

- Can hide where names originate.
- Can create ambiguity as dependencies grow.
- May be overgeneralized without an explicit boundary.

## Assumptions

- The programs are short and standalone.
- Namespace ownership is taught explicitly.
- Header and reusable-interface rules remain stricter.

## Alternatives considered

### Require `std::` everywhere

Clearer ownership, but more repeated syntax in novice examples.

### Use targeted declarations everywhere

More controlled, but adds setup lines when namespace behavior is not the objective.

## Consequences

- The convention applies across all three programming courses.
- Individual tasks may impose a stricter rule when stated explicitly.
- Header safety is a cross-artifact review concern.

## Revisit when

- examples become substantially larger;
- header/source separation becomes a primary objective; or
- namespace misconceptions persist after explicit instruction.
