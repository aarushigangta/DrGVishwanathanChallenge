## Problem Statement

Given an array of integers nums sorted in non-decreasing order, find the starting and ending position of a given target value.

If target is not found in the array, return [-1, -1].

You must write an algorithm with O(log n) runtime complexity.

Example 1:

Input: nums = [5,7,7,8,8,10], target = 8

Output: [3,4]

Example 2:

Input: nums = [5,7,7,8,8,10], target = 6

Output: [-1,-1]

Example 3:

Input: nums = [], target = 0

Output: [-1,-1]

## Approach

Define a class named Solution.

Implement a method searchRange within the Solution class that takes three parameters: nums (a sorted list of integers), target (an integer to search for), and is_searching_left (a boolean indicating whether to search for the leftmost or rightmost occurrence of the target).

a. Define a helper method binary_search that takes nums, target, and is_searching_left as arguments. This method performs binary search to find the target value and returns the index of either the leftmost or rightmost occurrence of the target value based on the is_searching_left parameter.

b. Initialize left to 0, right to the length of nums minus 1, and idx to -1.

c. Perform a binary search within the nums array using a while loop until left is less than or equal to right.

d. Calculate the midpoint as (left + right) // 2.

e. Compare the target value with the element at the midpoint of the array (nums[mid]):

1. If nums[mid] is greater than the target, update right to mid - 1.
2. If nums[mid] is less than the target, update left to mid + 1.
3.If nums[mid] is equal to the target, update idx to mid and adjust left or right accordingly based on is_searching_left.
4. f. Return the index idx.

Call binary_search twice within the searchRange method: once to find the leftmost occurrence of the target (left = binary_search(nums, target, True)) and once to find the rightmost occurrence of the target (right = binary_search(nums, target, False)).

Return a list containing the leftmost and rightmost indices of the target: [left, right].

This algorithm uses binary search to efficiently find the leftmost and rightmost occurrences of the target in the sorted array.
