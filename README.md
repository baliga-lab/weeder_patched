# Weeder 1.4.2 Patched

## Description

This is a refactored version of Weeder 1.4.2

## Compiling and Installation

make

This will build the executables

weederlauncher
weederTFBS
adviser
locator

For running the unit tests, type

make test


## Modifications

### Refactored weeder:

#### Cleanup of code
  - eliminated majority of copy-paste code
  - generalized repetitive code into functions
  - generalized linked list mergesort
  - renamed variables
  - removed unused code and variables
  - replaced magic numbers with symbolic constants
  - added makefile
  - code now compiles with significantly stricter settings and ISO C90
    without warnings

#### Optimizations
  - all base-4 power computations are replaced with a
    symbolic constant or a specialized base 4 power 4 function
  - replaced majority of malloc() based allocations with
    stack-based allocations, results in up to 100% improvement
    on the 12mer computation

#### Bug fixes
  - hamming distance

#### Customizations
  - MAX_SEQ and executable names can be changed in one central place
    in the makefile


## Open Questions
  - hamming distance
