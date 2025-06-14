## Problem Statement
Given an integer array `nums` and an integer `k`, return the number of subarrays of `nums` where the least common multiple of the subarray's elements is `k`.

A **subarray** is a contiguous non-empty sequence of elements within an array.
The **least common multiple of an array** is the smallest positive integer that is divisible by all the array elements.

### Approach
1. Use nested loops to generate all possible subarrays
2. For each subarray, calculate LCM incrementally
3. Count subarrays where LCM equals `k`
4. Use early termination when LCM exceeds `k`

### Time & Space Complexity
- **Time Complexity**: O(n² × log(max(nums)))
- **Space Complexity**: O(1)

