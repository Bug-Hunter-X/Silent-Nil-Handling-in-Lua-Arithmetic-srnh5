# Silent Nil Handling in Lua Arithmetic

This repository demonstrates a subtle bug in Lua related to how nil values are handled during arithmetic operations.  When a nil value is encountered in an arithmetic expression, Lua doesn't raise an error; instead, it silently returns nil. This can make debugging challenging as there's no immediate indication of the issue.

## The Bug

The `bug.lua` file contains a simple function that adds 1 to a given number. However, it lacks explicit checks for nil input. This allows nil to propagate through the calculation, producing unexpected nil results without any warnings.

## The Solution

The `bugSolution.lua` file demonstrates a fix for this problem.  By explicitly checking for nil values before performing arithmetic operations, we can prevent unexpected behavior and make the code more robust.