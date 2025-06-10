## Problem Statement

Given a string containing just the characters '(' and ')', return the length of the longest valid (well-formed) parentheses substring.

Example 1:

Input: s = "(()"
Output: 2
Explanation: The longest valid parentheses substring is "()".
Example 2:

Input: s = ")()())"
Output: 4
Explanation: The longest valid parentheses substring is "()()".
Example 3:

Input: s = ""
Output: 0

## Approach

1. Initialize Stack with Base Index

Push -1 onto stack as a reference point

This acts as a "ground level" for length calculations

2. Process Each Character

For Opening Parenthesis '(':

Push current index onto stack

This marks a potential start of a valid pair

For Closing Parenthesis ')':


Always pop from stack first

Then check two scenarios:

a. When Stack becomes empty after pop:

No matching '(' available

Push current index as new base reference

This ')' cannot be part of any valid sequence

b. When Stack still has elements after pop:

3. Calculate length: current_index - stack.peek() Update maximum length if this is longer
