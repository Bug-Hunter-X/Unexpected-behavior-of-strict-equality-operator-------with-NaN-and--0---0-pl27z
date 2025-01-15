# Unexpected behavior of strict equality operator (===) with NaN and +0, -0

This code demonstrates an uncommon bug in JavaScript related to the strict equality operator (===) when comparing NaN (Not a Number) values and +0 and -0 values.

## Bug

The strict equality operator (===) is not reflexive for NaN.  This means that NaN !== NaN, which is counterintuitive. It also treats +0 and -0 as strictly equal.

The `bug.js` file shows this behavior.  The function `foo` is designed to check for equality, but it produces incorrect results in these edge cases.

## Solution

The solution involves using `Number.isNaN` to check for NaN and explicitly checking for +0 and -0 if necessary. 

The `bugSolution.js` file demonstrates the corrected function.