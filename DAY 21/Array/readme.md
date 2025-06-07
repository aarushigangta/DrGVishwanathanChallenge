## Problem Statement

Given an integer rowIndex, return the rowIndexth (0-indexed) row of the Pascal's triangle.
In Pascal's triangle, each number is the sum of the two numbers directly above it

## Approach

Start with an initial row containing a single element: [1]. This is the 0th row (rowIndex = 0).

For each iteration from 0 to rowIndex (exclusive):
1. Calculate each element of the new row using binomial coefficients.
2. The element at index i in the new row is the sum of the element at index i and the element at index i-1 in the previous row.
3. Update row with the new row for the next iteration.

After all iterations, return the row which represents the rowIndex-th row of Pascal's Triangle

## Complexity 

Time Complexity: O(rowIndex²) - we build rowIndex rows, each taking O(i) time

Space Complexity: O(rowIndex) - only storing one row at a time
