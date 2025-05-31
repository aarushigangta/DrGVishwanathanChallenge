Problem Statement
------------------
Given a positive integer columnNumber, return its corresponding column title as it appears in an Excel sheet.

Examples:
Input: columnNumber = 1
Output: "A"

Input: columnNumber = 28
Output: "AB"

Input: columnNumber = 701
Output: "ZY"

Approach
--------------------
The solution uses a base-26 numbering system with a twist - Excel columns are 1-indexed rather than 0-indexed like typical base conversions.

Key Steps:
1. Decrement First: Since Excel columns start at 1 (not 0), we subtract 1 from the column number
2. Extract Character: Use modulo 26 to get the rightmost character, then add to 'A'
3. Insert at Beginning: Build the result string from right to left
4. Divide and Continue: Integer divide by 26 and repeat until column number becomes 0

Time and Space Complexity
-------------------------
Time Complexity: O(log26(n)) where n is the column number
Space Complexity: O(log26(n)) for the StringBuilder storage


