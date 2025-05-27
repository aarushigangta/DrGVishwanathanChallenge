## Problem Statement

Given a signed 32-bit integer x, return x with its digits reversed. If reversing x causes the value to go outside the signed 32-bit integer range [-231, 231 - 1], then return 0.

## Approach 

Extract the last digit using modulo operation (x % 10)

Remove the last digit from the original number (x / 10)

Check for potential overflow before updating the reversed number

Update the reversed number: rev = rev * 10 + digit

Recursively process the remaining digits
