## Problem Statement

Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.

 ## Approach

We use a HashSet to track elements:

1. Initialize an empty HashSet
2. Iterate through each element in the array
3. Try to add the current element to the HashSet
4. If add() returns false (element already exists), return true immediately
5. If we finish the loop without finding duplicates, return false

## Complexity

1. Time Complexity: O(n)
2. Space Complexity: O(n)
