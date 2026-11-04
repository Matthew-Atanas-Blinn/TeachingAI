# Change Log

All notable approved repository changes are recorded here. Detailed per-file reports accompany each delivery.

### 1.4.0 - 2026-11-04

#### Added

- Added the approved Programming Fundamentals I user-defined-functions module.
- Added module-specific source-of-truth, review-checklist, local-decision, and routing files.
- Added repository output verification requirements to `META/update_process.md`.
- Added explicit D2L HTML code-panel generation and validation requirements.

#### Changed

- Registered the functions module in the Programming Fundamentals I module index.
- Updated the Programming Fundamentals I course context with the approved module and its quiz emphasis.
- Updated current repository version declarations to 1.4.0.
- Strengthened quiz formatting requirements so code is visually separated from ordinary text in question stems and answer choices.
- Required D2L quiz CSV generation to use the established HTML representation with the corresponding `HTML` format field.
- Required repository completion reports to be verified against Git's actual changed-file inventory.
- Required archive contents to be extracted and checked against the approved change report before delivery.

#### Corrected

- Corrected the root `INDEX.md` version heading to identify the current repository as version 1.4.0.
- Corrected the repository process so a file cannot be reported as modified unless the final Git inventory or packaged output contains that modification.
- Corrected the Chapter 6 quiz formatting approach by replacing unsupported Markdown code fences with D2L-compatible HTML code panels.
- Clarified that structural CSV validation alone does not establish correct student-visible rendering.

#### Assumptions and TODOs

- The Chapter 6 slide deck and D2L quiz CSV remain generated artifacts outside the repository.
- The current Chapter 6 deck predates the newer light-code-panel default and does not require immediate modification.
- The Chapter 6 quiz must be test-imported into D2L before student release.
- Assignment alignment should be reviewed when the corresponding functions programming assignment is revised.

## 1.3.0 - 2026-11-03

### Added

- Added an accepted cross-course decision for D2L quiz import format, instructor-facing metadata, fixed pedagogical ordering, and randomization defaults.

### Changed

- Standardized D2L CSV as the default quiz import format unless a required feature needs another validated method.
- Clarified that instructor-only titles use `<Category>: <Concept>` and should be concise, descriptive, and useful for future revision rather than opaque sequence codes.
- Required D2L Difficulty 1-5 to match Foundation through Design/Diagnosis.
- Clarified that pedagogical progression is normally preserved through question order rather than imported sections or full question randomization.
- Added review checks for title quality, student-view visibility, format exceptions, and unnecessary section/package complexity.

### Assumptions and TODOs

- Revalidate title visibility and CSV behavior if the D2L interface or institutional configuration changes.
- Reconsider package imports only when a concrete unsupported feature justifies the additional complexity.

## 1.2.0 - 2026-11-02

### Added

- Added hierarchical `INDEX.md` routing throughout the repository.
- Added a cross-artifact `STANDARDS/global/` layer.
- Added global C++ instructional rules covering namespace use, enums, aliases, and generated-code validity.
- Added global semantic visual-mapping rules and a cross-artifact review checklist.
- Added accepted decisions for the C++ namespace convention, semantic visual mapping, and hierarchical indexing.
- Added the Programming Fundamentals I enums, namespaces, and type-aliases module source of truth, local decisions, and review checklist.
- Added separate structure guidance for modules, decisions, and proposed experiments.

### Changed

- Made top-down hierarchical index traversal mandatory.
- Required every folder to contain an `INDEX.md`, including temporary stubs until branches grow.
- Prohibited lower-level backward pointers into the rules or decisions hierarchy.
- Required nearest-index maintenance without recursively expanding ancestor indexes.
- Split the former navigation `README.md` files in `MODULES/`, `DECISIONS/`, and `PROPOSED/` into `INDEX.md` routing plus separately named structure files.
- Clarified that `using namespace std;` may be used in short standalone instructional `.cpp` programs but not in instructor-provided headers or reusable interfaces.
- Clarified background-paired semantic colors, non-color reinforcement, and instructional highlighting across artifact types.

### Removed

- Removed superseded `MODULES/README.md`, `DECISIONS/README.md`, and `PROPOSED/README.md`.

### Assumptions and TODOs

- Exact repository-wide visual color tokens remain deferred until several approved final decks are compared.
- Programming Fundamentals II and III module indexes remain stubs until approved module source-of-truth folders are created.
- Quiz length and assignment alignment for the new Programming Fundamentals I module remain unresolved.

## 1.1.0 - 2026-10-30

### Changed

- Clarified that legal and institutional authority does not require external research for every task.
- Made governing-source correction the default update process and added expedited artifact repair.
- Added operational privacy-verification guidance and clearer legitimate-need wording.
- Added rationale and override guidance to required pedagogy.
- Added a cross-course pedagogical-progression decision record.
- Expanded slide visual-system guidance and marked exact style tokens for later extraction from approved decks.
- Added severity-based iterative generation, correction, and regression review with a three-cycle safety cap.
- Expanded quiz answer-position pattern checks.

### Assumptions and TODOs

- Exact slide fonts, sizes, spacing, and palette values require extraction from approved final decks.
- The three-cycle limit is an operational safety cap and may be revised based on observed convergence and runtime.

## 1.0.0 - 2026-10-30

### Added

- Initial repository architecture and governance.
- Universal pedagogy, accessibility, and data-privacy requirements.
- Generation and review standards for slides, quizzes, assignments, and autograders.
- Recovery-grading standard.
- Preliminary course-level files for Programming Fundamentals I, II, and III.
- Guidance placeholders for modules, decisions, and proposed experiments.

### Assumptions

- Course-level files are preliminary and should not be treated as complete curricula.
- Legal and privacy content is operational guidance, not legal advice; current institutional policy controls.
