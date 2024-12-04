# F# Mutable Variable Swap Bug

This repository demonstrates a common misunderstanding in F# regarding mutable variables and their behavior within functions.  The `swap` function attempts to swap the values of two mutable variables, but due to how F# handles mutable variable references, it unintentionally modifies the original variables.

The `bug.fs` file contains the problematic code, while `bugSolution.fs` provides a corrected version.

## Problem:
The original `swap` function modifies the original variables directly because of pass-by-reference semantics.  This is unexpected for developers unfamiliar with this aspect of F#.

## Solution:
The solution uses tuples to return the swapped values, preventing unintended side effects on the original variables.