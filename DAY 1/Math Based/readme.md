Problem Statement:

Given an array nums containing n distinct numbers in the range [0,n], return the only number that is missing from the array.

Approach:

This solution uses the mathematical summation formula for the first n natural numbers:

The sum of numbers from 0 to n is n(n+1)/2​Calculate the actual sum of elements in the array.

The missing number is the difference between the expected sum and the actual sum.
