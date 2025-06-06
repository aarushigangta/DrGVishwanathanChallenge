## Problem Statement

Given an integer array nums, return the greatest common divisor of the smallest number and largest number in nums.
The greatest common divisor of two numbers is the largest positive integer that evenly divides both numbers.

## Approach

1. Find the smallest and largest element in the array using a single pass.
2. Apply the Euclidean Algorithm to compute the GCD of the smallest and largest numbers.
3. The algorithm works by repeatedly setting a = b and b = a % b until b % a == 0.
4. The final value of a will be the GCD.

## Complexity

**Time complexity:**
1. O(n+log(min))
2. O(n) to find the smallest and largest values.
3.O(log(min(small, large))) for the Euclidean GCD algorithm.

**Space complexity:** O(1)
