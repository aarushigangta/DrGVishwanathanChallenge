## Problem Statement

Given a string s representing a valid expression, implement a basic calculator to evaluate it, and return the result of the evaluation.
Note: You are not allowed to use any built-in function which evaluates strings as mathematical expressions, such as eval().

## Approach 

This solution utilizes a stack to keep track of results and signs as we parse through the string. 

1. Iterate through the string: Check each character to determine if it’s a digit, an operator, or a parenthesis.
2. Handle digits: Build the current number, accounting for multi-digit numbers.
3. Manage signs: Track the current sign (positive or negative) and apply it when adding to the result.
4. Use a stack for parentheses: Push the current result and sign onto the stack when encountering an opening parenthesis. On a closing parenthesis, pop from the stack to compute the result for the enclosed expression.
