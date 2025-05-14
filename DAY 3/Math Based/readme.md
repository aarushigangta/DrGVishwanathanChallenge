**Problem Statement**

A perfect number is a positive integer that is equal to the sum of its proper divisors, excluding the number itself. 
Given a number num, determine whether it is a perfect number.

**Approach**

Initialize sum = 1, since 1 is always a divisor of any number (except 0 and 1).

Iterate from 2 to √num:

If i divides num, then both i and num / i are divisors.

Add i to the sum.

Only add num / i if it's different from i to avoid double-counting in case of perfect squares.

At the end, if sum == num, then num is a perfect number.
