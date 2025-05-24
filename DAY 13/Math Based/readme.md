## Problem
Given an integer array `nums`, return the **sign** of the product of all its elements.

- Return `1` if the product is positive.
- Return `-1` if the product is negative.
- Return `0` if any number is `0`.

## Example
**Input:** `[1, -2, -3, 4]`  
**Output:** `1`  
**Explanation:** Product = `1 * -2 * -3 * 4 = 24` → Positive → Return `1`.

**Input:** `[1, 5, 0, 2, -3]`  
**Output:** `0`

## Approach
- Initialize a variable `sign = 1`.
- Traverse the array:
  - If any number is `0`, return `0` immediately.
  - If a number is negative, flip the sign by multiplying by `-1`.
- Return the final value of `sign`.

##
