**Problem Statement**

Given an integer num, repeatedly add all its digits until the result has only one digit, and return it.

**Approach**

Instead of simulating repeated digit addition, the code uses the Digital Root formula:

For any num > 0, the digital root is 1 + (num - 1) % 9

