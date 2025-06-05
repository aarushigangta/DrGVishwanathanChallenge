## Problem Statement

Given a string s containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid.

An input string is valid if:

1. Open brackets must be closed by the same type of brackets.
2. Open brackets must be closed in the correct order.
3. Every close bracket has a corresponding open bracket of the same type.

## Approach

The solution combines a Stack with a HashMap for efficient bracket matching:

1. Create a hash map and map each closing bracket to its corresponding opening bracket as

')' -> '('
'}' -> '{'
']' -> '['


2. Process Each Character:

i. If it's an opening bracket (found in map values): push to stack

ii. If it's a closing bracket (found in map keys):

4. Check if stack is empty (no matching opener)
5. Pop from stack and verify it matches the expected opener
6. If mismatch, return false
7. Final Check: Stack should be empty (all brackets matched)
