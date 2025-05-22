**Problem Statement**

Given an integer n, return the number of trailing zeroes in n!.

**Approach**

Trailing zeroes in a factorial come from the product of 2 and 5. Since there are usually more 2s than 5s in the prime factorization of n!, we only need to count how many times 5 appears in the factorization of all numbers from 1 to n

Loop through all numbers from 1 to n and count how many times each number is divisible by 5.

Every division by 5 contributes to one trailing zero.

However, numbers like 25, 125, etc., contribute more than one 5. So we continue dividing by 5 until the number is no longer divisible by 5.

Keep a running total of all such contributions.
