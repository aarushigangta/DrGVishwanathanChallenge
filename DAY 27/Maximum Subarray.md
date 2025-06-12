## Problem Statement

Given an integer array nums, find the subarray with the largest sum, and return its sum.

Example 1:

Input: nums = [-2,1,-3,4,-1,2,1,-5,4]
Output: 6
Explanation: The subarray [4,-1,2,1] has the largest sum 6.
Example 2:

Input: nums = [1]
Output: 1
Explanation: The subarray [1] has the largest sum 1.

## Approach

This problem is solved using Kadane's Algorithm, which is a dynamic programming approach that finds the maximum sum subarray in linear time.

The algorithm maintains two variables:
1. Current Sum (cs): Sum of current subarray being considered
2. Maximum Sum (ms): Maximum sum found so far

Core Logic: At each position, decide whether to:

Extend the current subarray by including current element

Start fresh from current element if previous sum was negative
