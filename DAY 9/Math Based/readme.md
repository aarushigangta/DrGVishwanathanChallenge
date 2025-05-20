**Problem statement**

Given an integer n, return the nth digit of the infinite integer sequence [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, ...].

**Approach**

Start with single-digit numbers (len = 1), which includes 9 numbers (1-9).

Subtract the count of digits in that range (len * 9 * 10^len-1) from n until n fits within a specific digit-length group.

Once the correct digit-length is found, calculate the actual number (start + (n - 1)/len).

Convert the number to a string and pick the correct character using (n - 1) % len.
