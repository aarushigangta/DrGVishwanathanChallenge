Problem Statement
------------------
Given a non-negative integer c, decide whether there are two integers a and b such that a² + b² = c.

Examples:
Input: c = 5
Output: true
Explanation: 1² + 2² = 1 + 4 = 5

Input: c = 3
Output: false
Explanation: No way to express 3 as sum of two squares

Input: c = 4  
Output: true
Explanation: 0² + 2² = 0 + 4 = 4

Approach
--------------------------------
We applied two pointer approach as:

1. Initialize two pointers:
   - left = 0 (minimum possible value for first square)
   - right = √c (maximum possible value for second square)

2. While left <= right:
   - Calculate sum = left² + right²
   - If sum equals c: return true
   - If sum < c: increment left (need larger sum)
   - If sum > c: decrement right (need smaller sum)

3. If no valid pair found: return false

Time and Space Complexity
-------------------------
Time Complexity: O(√c)
- In worst case, we iterate from 0 to √c
- Each iteration does constant work

Space Complexity: O(1)
- Only using constant extra space for pointers
