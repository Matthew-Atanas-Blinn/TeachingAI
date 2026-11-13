# Change Log

All notable approved repository changes are recorded here. Detailed per-file reports accompany each delivery.

### 1.7.0 - 2026-11-12

#### Added
- Added the approved Programming Fundamentals I arrays module with source of truth, decisions, review checklist, and routing.
- Added per-course sequence files that separate dependency rationale from course context.
- Added a Programming I strings decision stub that places introductory C-strings inside the later strings module.

#### Changed
- Registered the approved Programming I ending sequence: functions, enums/namespaces/aliases, arrays, then strings and C-strings.
- Clarified raw-array parameter behavior relative to genuine reference parameters.
- Strengthened the explicit-array connection for enum iteration.
- Updated current-version declarations to 1.7.0.

#### Assumptions and TODOs
- Earlier Programming I ordering remains to be documented from approved materials.
- Programming II and the full Programming III sequence remain intentionally incomplete.
- Existing strings slides do not include C-strings and must be revised before the strings module is fully aligned.
- Arrays assignment, quiz, parallel-array depth, and exact selection-sort implementation expectations remain unresolved.

## 1.6.0 - 2026-11-09

### Added
- Added a pipeline integration standard defining authority boundaries, required assignment handoff, compatibility checks, evidence review, privacy, and cross-repository maintenance.
- Added an accepted decision to keep TeachingAI and the C++ Assignment Grading Pipeline separate while connecting them through an explicit contract.

### Changed
- Made `STANDARDS/autograders/INDEX.md` the owner of the pipeline-integration loading trigger.
- Corrected autograder guidance so assignment-specific native checks may be configured in supported detailed rubrics while shared evaluation semantics remain in `gio.py`.
- Corrected aggregation guidance to use `run_pipeline.py` as the normal orchestrated path and treat `sum_results_by_name.py` as conditional rather than universally active.
- Added pipeline-release compatibility checks to assignment and autograder generation and review.
- Updated current-version declarations to 1.6.0.

### Assumptions and TODOs
- The Assignment Pipeline remains a separate repository and Matthew's normal C++ grading implementation.
- The pipeline compatibility declaration initially uses Markdown; machine-readable compatibility metadata remains optional until automated checks are implemented.
- Licensing for the separate software repository remains a future decision if it is publicly distributed.

#### 1.5.0 - 2026-11-06

##### Added
- Added the approved Programming Fundamentals III heaps and priority-queues module with source of truth, decisions, review checklist, and routing.
- Added decision-stub branches for balanced trees and data-structure selection.

##### Changed
- Added Programming Fundamentals III rules for recurring invariant analysis, prompt STL connections, algorithm-pattern identification, balanced-tree context, selected student-authored testing, and culminating structure selection.
- Established concise decision stubs as the default for approved decisions affecting undeveloped modules.
- Registered the new Programming Fundamentals III branches and updated current-version declarations.
- Clarified that existing Programming III materials may be revised during future substantial updates but do not require immediate retroactive revision.

##### Assumptions and TODOs
- The heaps and priority-queues module is ready to govern new slides and related artifacts.
- Balanced-trees and structure-selection details remain intentionally incomplete and must be resolved before substantial module materials are generated.
- Exact heap assignment, quiz length, heap-sort depth, and bottom-up heap-construction coverage remain undecided.

### 1.4.1 - 2026-11-05

#### Changed

- Added a normal 18-point minimum target for projected instructional text and code, with dense slides simplified or split instead of shrinking content.
- Added explicit WCAG 2.2 AA local contrast targets and required non-color reinforcement for semantic mappings.
- Prohibited underlining code for semantic emphasis because it can obscure underscores and increase visual clutter.
- Added title-slide hero visuals as the default when established course decks use that convention.
- Added corresponding generation and review checks.

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
