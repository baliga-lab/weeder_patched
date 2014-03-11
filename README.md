# Weeder 1.4.2 Patched

## Description

This is a refactored version of Weeder 1.4.2

Find the original version here:

http://159.149.160.51/modtools/downloads/weeder.html

## Compiling and Installation

see INSTALL for compilation instructions

This will build the executables

weederlauncher
weederTFBS
adviser
locator

## Remarks

The directory python contains re-implementations of adviser and weederlauncher
in Python.
weederlauncher.py provides an way to define the location of the FreqFiles directory
through it --ffdir option

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

#### Enhancements/Customizations

  - Build with autotools
  - MAX_SEQ and executable names can be changed in one central place
    in the makefile
  - Location of FreqFiles can be specified for weederTFBS

## Open Questions
  - hamming distance
