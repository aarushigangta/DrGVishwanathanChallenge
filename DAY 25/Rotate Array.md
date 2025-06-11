## Problem Statement

Given an integer array nums, rotate the array to the right by k steps, where k is non-negative.

Example 1:

Input: nums = [1,2,3,4,5,6,7], k = 3

Output: [5,6,7,1,2,3,4]

Explanation:

rotate 1 steps to the right: [7,1,2,3,4,5,6]

rotate 2 steps to the right: [6,7,1,2,3,4,5]

rotate 3 steps to the right: [5,6,7,1,2,3,4]

## Approach

1. Since rotating ( n ) times brings the array back to its original state, ( k ) can be reduced to ( k \mod n ).
2. Reverse the entire array.
3. Reverse the first ( k ) elements.
4. Reverse the remaining ( n-k ) elements.
5. The final array will be the desired rotated version.
