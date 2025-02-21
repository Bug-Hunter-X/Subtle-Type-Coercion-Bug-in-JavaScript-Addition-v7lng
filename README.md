# Subtle Type Coercion Bug in JavaScript Addition

This repository demonstrates a common, yet subtle, bug in JavaScript related to type coercion when performing addition with `null` values.  The `foo` function intends to return `null` if either input is `null`, but it might not behave as expected due to JavaScript's loose typing and automatic type conversions. 

The `bug.js` file contains the buggy code, while `bugSolution.js` provides a corrected version.

## Bug
The original code uses strict equality (`===`) to check for `null` values. This is generally good practice; however, when combining this check with the `+` operator, JavaScript's type coercion system can unexpectedly convert `null` to `0`.

## Solution
The corrected code explicitly checks for `null` before attempting addition, preventing unintended type coercion.  This makes the function's behavior more predictable and consistent.