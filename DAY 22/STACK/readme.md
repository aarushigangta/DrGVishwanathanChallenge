## Problem Statement

Given a string s of '(' , ')' and lowercase English characters.

Your task is to remove the minimum number of parentheses ( '(' or ')', in any positions ) so that the resulting parentheses string is valid and return any valid string.

Formally, a parentheses string is valid if and only if:
1. It is the empty string, contains only lowercase characters, or
2. It can be written as AB (A concatenated with B), where A and B are valid strings, or
3. It can be written as (A), where A is a valid string.

## Approach

This solution uses a two-pass approach with a stack to track unmatched parentheses:

1. First Pass (Left to Right): Handle unmatched closing parentheses )
2. Second Pass: Handle unmatched opening parentheses (
3. Final Step: Remove all marked invalid characters
