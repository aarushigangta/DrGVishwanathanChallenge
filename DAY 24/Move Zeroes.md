## Problem Statement

Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.
Note that you must do this in-place without making a copy of the array.

## Approach

1. Initialize a pointer k = 0 to track the next position for non-zero elements
2. Iterate through the array:
3. If current element is non-zero, place it at position k and increment k
4. If current element is zero, skip it
5. Fill all remaining positions (from k to end) with zeros
