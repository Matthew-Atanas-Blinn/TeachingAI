# Decision: TeachingAI and Assignment Pipeline Relationship

Status: Accepted  
Date: 2026-11-09  
Scope: Repository and cross-course C++ assignment grading

## Context

TeachingAI contains durable instructional standards, course and module context, assessment requirements, review processes, and rationale. The C++ Assignment Grading Pipeline is executable software with its own release versions, component responsibilities, configuration semantics, commands, diagnostics, and operating documentation.

The repositories must work together when an assignment is designed, packaged, validated, graded, and imported into D2L. Without an explicit relationship, overlapping guidance can drift. Combining the repositories, however, would couple TeachingAI's general instructional framework to one software implementation and release cycle.

## Decision

Keep TeachingAI and the Assignment Pipeline as separate repositories with an explicit integration contract.

TeachingAI governs pedagogy, instructional alignment, assignment and assessment design, privacy, evidence quality, review expectations, and recovery grading. The Assignment Pipeline governs implemented grading behavior, supported configuration, commands, diagnostics, software responsibilities, and release compatibility.

TeachingAI stores a narrow integration standard describing the required handoff, authority boundary, compatibility checks, and review contract. It does not copy the pipeline's full schema, architecture, command reference, source code, or generated-output details.

The Assignment Pipeline publishes a compatibility declaration identifying the pipeline release, compatible TeachingAI version, integration-contract version, and supported environment.

## Benefits

- Preserves clear separation between instructional governance and software implementation.
- Allows independent TeachingAI and pipeline release cycles.
- Prevents copied schemas and architecture descriptions from becoming stale.
- Keeps TeachingAI useful to educators who use another autograding implementation.
- Keeps pipeline-specific behavior close to the executable source and operating documentation.
- Gives AI systems and human maintainers an explicit route for pipeline-dependent assignment work.
- Supports a separate software-license decision if the pipeline is published.

## Drawbacks

- Some assignment work requires both repositories.
- Compatibility metadata and cross-repository references require maintenance.
- A user can still load only one repository and miss relevant context if index routing or task instructions are ignored.
- Shared concerns such as transparent deductions appear at different levels and require careful authority boundaries.

## Assumptions

- TeachingAI remains documentation-first and implementation-independent.
- The Assignment Pipeline remains Matthew's normal C++ grading implementation.
- Pipeline-dependent work can access the selected pipeline release and its current documentation.
- The integration contract changes less frequently than the pipeline implementation.
- Student data remains outside both public repositories.

## Alternatives considered

### Merge the pipeline into TeachingAI

A single repository would simplify discovery, but it would mix software releases with instructional-governance releases, complicate licensing, couple TeachingAI to D2L and the current MSYS2/clang++ implementation, and encourage implementation details to appear as universal teaching requirements.

### Keep the repositories entirely independent

Complete separation would reduce explicit dependencies, but assignment design could overlook pipeline constraints, overlapping guidance could drift, and compatibility failures would be discovered late.

### Duplicate pipeline documentation inside TeachingAI

Copied guidance would make TeachingAI self-contained temporarily, but schemas, commands, diagnostics, and component responsibilities would become stale as the software changed.

## Consequences

- `STANDARDS/autograders/INDEX.md` selects the integration standard for pipeline-dependent work.
- TeachingAI autograder guidance states stable educational and integration requirements rather than duplicating volatile implementation details.
- Pipeline-dependent assignment deliveries identify the tested pipeline release.
- The Assignment Pipeline contains a compatibility declaration and maintains it with relevant releases.
- Shared pipeline modifications remain exceptional during assignment conversion and must be reported explicitly.

## Revisit when

- TeachingAI becomes a software distribution rather than a documentation-first framework;
- the pipeline becomes generic enough to serve as a native TeachingAI reference implementation;
- maintaining separate repositories causes recurring compatibility failures;
- automated dependency or schema validation makes a stronger integration practical; or
- licensing, institutional deployment, or contribution requirements materially change.
