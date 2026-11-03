# Global Standards Review Checklist

## Applicability

- [ ] Every applicable global standard was loaded before artifact-specific standards.
- [ ] Standards whose triggers did not match the task were not applied mechanically.

## C++ instructional material

When the artifact contains C++:

- [ ] Namespace use matches the instructional context.
- [ ] No instructor-provided header contains `using namespace std;`.
- [ ] Any stricter namespace requirement is an explicit learning objective or specification.
- [ ] Harmless course-approved namespace style is not penalized unless namespace discipline is assessed.
- [ ] Examples are valid for the stated language level and toolchain.
- [ ] C++ string literals contain escaped newlines or `std::endl`, not accidental literal line breaks.
- [ ] Required interfaces, filenames, and signatures remain exact.

## Semantic visual mapping

When explanatory visuals map categories to targets:

- [ ] Every descriptor maps to the intended token or region.
- [ ] Related elements use one recognizable semantic family.
- [ ] Dark- and light-background variants were evaluated separately.
- [ ] Each target remains readable against its immediate background.
- [ ] Important meaning has a non-color cue.
- [ ] Unrelated syntax or visual detail does not compete with the mapping.
- [ ] The rendered artifact was inspected at likely delivery scale.
