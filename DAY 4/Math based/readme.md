**Problem Statement**

Given an integer x, return true if x is a palindrome, and false otherwise.
A palindrome is a number that reads the same forward and backward. Check whether the integer x is a palindromic number.

**Approach**

Edge Case: If x < 0, return false because negative numbers cannot be palindromes.

Convert the integer to a String.

Use two pointers:

left starts at the beginning of the string.

right starts at the end of the string.

While left < right, compare characters:

If mismatch → return false

If all characters match → return true
