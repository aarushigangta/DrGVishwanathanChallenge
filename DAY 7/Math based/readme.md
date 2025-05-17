**Problem Statement**

You are given a large integer represented as an integer array digits, where each digits[i] is the ith digit of the integer. The digits are ordered from most significant to least significant in left-to-right order. The large integer does not contain any leading 0's.
Increment the large integer by one and return the resulting array of digits

**Approach**

This solution follows a greedy approach that starts from the least significant digit (rightmost) and attempts to add one.

Steps:
Traverse the array from end to start.

If the digit is less than 9, simply add 1 and return the array.

If the digit is 9, it becomes 0 and the loop continues to propagate the carry.

If all digits are 9 (e.g., [9,9,9]), a new array of size n+1 is created with 1 at the first index.
