# F# Stack Overflow Bug

This repository demonstrates a common error in F# involving mutable variables and uncontrolled recursion leading to stack overflow exceptions.  The original code (`bug.fs`) uses mutable variables `x` and `y`, incrementing them recursively until `x` reaches 1,000,000.  This approach causes a stack overflow because the recursive calls consume stack space without a proper termination condition that is easily met.

The solution (`bugSolution.fs`) showcases a more efficient and safer approach using tail recursion and avoiding mutable variables when possible. This ensures the code executes without exceeding stack limitations. This example highlights the importance of understanding F#'s memory management and the potential issues with uncontrolled recursion.