**Problem Statement**

Given a positive integer num, write a function that returns true if num is a perfect square, otherwise false.

**Approach**

This solution uses binary search to efficiently determine whether a number is a perfect square.

Steps

Initialize Binary Search:

Set left = 1 and right = num.

Perform Binary Search:

Calculate mid = (left + right) / 2.

Compute mid * mid and store it in midSquare (cast to long to prevent overflow).

If midSquare == num, return true.

If midSquare > num, search the left half.

If midSquare < num, search the right half.

Return false if no perfect square is found.
