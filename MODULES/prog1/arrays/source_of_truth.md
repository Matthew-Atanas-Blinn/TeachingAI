## Programming Fundamentals I: Arrays

Status: Approved module source of truth
Course: COSC 1436
Last updated: 2026-11-12

### Purpose
How can a program store and process a fixed collection of related values without creating a separate named variable for each value?

### Central mental model
An array is a fixed-size sequence of same-type elements. Each element is a separate variable selected by an index.

Create -> Select -> Change -> Traverse -> Process -> Combine

### Prerequisites
Students should understand variables, types, expressions, assignment, selection, loops, user-defined functions, value/reference parameter behavior, scope, and basic enums.

### Learning objectives
Students should be able to:
- explain why an array is preferable to many separately named variables;
- identify element type, array name, capacity, indices, elements, and stored values;
- declare and initialize a built-in array;
- distinguish an index from the value stored at that index;
- read, modify, and trace individual elements;
- identify valid indices from 0 through size - 1;
- traverse an array safely with an index-based loop;
- input, output, total, average, count, and find extrema;
- distinguish capacity from logical size when partially filled arrays are used;
- pass an array and its logical size to a function;
- use const for read-only access through an array parameter;
- explain caller-visible element modification without calling the parameter a genuine reference parameter;
- perform and trace a linear search and reversal;
- trace selection sort at an introductory integration depth;
- use a range-based for loop when an index is unnecessary;
- iterate over an explicit array of valid enum values; and
- trace row/column indexing, nested traversal, row totals, and column totals in a two-dimensional array.

### Mental models
#### Element selection
Evaluate the index expression, verify it is valid, select one element, then read or change that element.

#### Traversal
A complete traversal visits each valid index exactly once. For size elements, the ordinary valid range is [0, size), expressed by i < size.

#### Capacity and logical size
Capacity is the number of elements the array can hold. Logical size is the number currently treated as meaningful. Traversal must use the intended logical size.

#### Array parameters
Required behavioral model: passing a raw array does not copy every element. A function can access caller-owned elements, so changing an element can change the caller's array. The function normally receives the size separately.

Brief technical clarification: in a parameter list, int values[] is adjusted to int* values. The pointer is passed by value and provides access to the original elements. This differs from a genuine reference parameter such as int& value. Pointer arithmetic and advanced reference-to-array syntax are deferred.

### Instructional sequence
- Motivate a collection with many related values and repeated operations.
- Establish the fixed-size, same-type, indexed mental model.
- Declare, initialize, select, and change elements.
- Trace array state before independent implementation.
- Establish valid indices and safe traversal.
- Apply traversal to input/output, total, average, count, minimum, and maximum.
- Distinguish capacity and logical size with partially filled arrays.
- Reuse familiar traversals in short array-processing functions.
- Apply arrays to linear search and reversal.
- Use selection sort as a limited culminating nested-loop example.
- Compare index-based and range-based traversal.
- Revisit enum iteration with an explicit array of valid values.
- Introduce two-dimensional row/column indexing, nested traversal, row totals, column totals, and index-order diagnosis.
- Transition to the later strings and C-strings module.

### Core scope
Raw one-dimensional arrays; declaration; full, partial, and zero initialization; element access and assignment; zero-based indexing; valid bounds; index-based traversal; input/output; accumulation; counting; extrema; capacity and logical size; array-plus-size functions; const read-only access; linear search; reversal; and introductory two-dimensional arrays.

### Secondary scope
Range-based for; explicit enum-value arrays; parallel arrays as a fragile grouping strategy if time permits; and selection sort as a guided integration example.

### Deferred scope
Pointer arithmetic; explicit dereference notation as an array objective; references to arrays; templates for array size; std::array; std::span; dynamic arrays; vector internals; formal algorithm analysis; binary search; sorting comparisons; stability; proofs; arbitrary multidimensional arrays; detailed memory-layout calculations; and comprehensive C-string coverage.

### Misconceptions
- The last valid index equals the number of elements.
- An index and the value at that index are interchangeable.
- Declaring a local array gives every element a predictable zero value.
- i <= size visits only valid elements.
- An array parameter receives a complete array copy.
- int values[] is a genuine reference parameter.
- A function automatically knows the array's size.
- Returning the found value is always equivalent to returning its index.
- smallestIndex should store the smallest value.
- row and column indices may be swapped without changing meaning.

### Slide coverage
A complete deck should include the approved optional expansions: capacity versus logical size, row totals, column totals, and swapped row/column diagnosis. Functions remain a short integration movement. Selection sort remains limited to motivation, one-pass tracing, a small complete trace, and guided code reading or completion.

### Assessment guidance
Emphasize tracing, prediction, valid ranges, traversal, accumulator initialization, index/value distinctions, caller-visible element changes, simple search/reversal, and diagnosis. Use selection sort sparingly and do not assess formal sorting analysis. Avoid undefined behavior except when identifying an invalid access.

### Future connections
- The strings module will compare std::string with C-strings as null-terminated character arrays.
- Programming II will connect arrays to pointers, dynamic storage, classes, and vectors.
- Later courses will study algorithm design and analysis in greater depth.
- Arrays underlie matrices, heaps, hash tables, and graph representations.

### Unresolved questions
- Final assignment and quiz scope.
- Whether parallel arrays appear in the final deck or only as a future connection.
- Whether students complete or only trace the full selection-sort implementation.
