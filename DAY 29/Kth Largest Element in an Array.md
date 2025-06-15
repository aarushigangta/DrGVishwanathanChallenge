## Problem Statement

Given an integer array nums and an integer k, return the kth largest element in the array.


## Approach

We sort the numbers in descending order and pick the k-th element.
1. Use built-in sorted function to sort the list nums in reverse order (i.e., in descending order).
2. Select the k-th element from the sorted list (keeping in mind the zero-based indexing of lists).
3. The k-th element in the sorted list is the k-th largest element in the original list.

## Complexity:
1. Time Complexity: O(NlogN)
2. Space Complexity: O(1)
