**Problem statement**

Given two non-negative integers low and high. Return the count of odd numbers between low and high (inclusive).

**Approach**

Total odd number between 1 and low - 1 is low/2.

Total odd number between 1 and high is (high + 1 ) / 2.

For getting answer we will do : Total odd number between 1 and high - Total odd number between 1 and low - 1
