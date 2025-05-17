**Problem Statement**

A number is considered a Happy Number if it eventually reaches 1 when replaced by the sum of the squares of each digit. If it loops endlessly without reaching 1, it is not a happy number.

**Approach**

This solution uses recursion to repeatedly compute the sum of the squares of the digits of the number. It relies on a known property that if a number becomes 1 or 7 during this process, it is guaranteed to be a happy number.

Base Cases:

n == 1 or n == 7: Return true

If n < 10: Only 1 and 7 are considered happy single-digit numbers, so return false for other digits

Recursive Step:

Calculate the sum of the squares of digits

Recurse on the resulting sum
