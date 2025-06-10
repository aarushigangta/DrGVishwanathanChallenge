## Problem Statement

Given a sorted array of distinct integers and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.
You must write an algorithm with O(log n) runtime complexity.

## Approach

1.  We initialize two pointers, left and right. left starts at the beginning of the list (0), and right starts at the end of the list (len(nums) - 1). These pointers help in performing the binary search.
2.  A while loop continues as long as left is less than or equal to right
3.  We then calculate the middle index mid of the current range defined by left and right.
4.  If the element at the midpoint  is equal to the target, we have found the target, and we return the index mid.
5.  If the element at the midpoint  is greater than the target, it means the target must be in the left half of the current range. We adjust the right pointer to mid - 1 to narrow the search to the left half.
6.  If the element at the midpoint  is less than the target, it means the target must be in the right half of the current range. We adjust the left pointer to mid + 1 to narrow the search to the right half.
7.  If the target is not found in the list, the while loop will terminate when left is greater than right. At this point, left will be the index where the target should be inserted to maintain the sorted order. We return left as the insertion point. 
