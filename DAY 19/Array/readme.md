## Problem Statement

You are given an array prices where prices[i] is the price of a given stock on the ith day.
You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock.
Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0.

## Approach

The solution uses a greedy approach with two key variables:

1. bb (best buy): Tracks the minimum price seen so far (best day to buy)
2. mp (max profit): Tracks the maximum profit achievable so far.

For each price, calculate potential profit if we sell today

Update maximum profit if current profit is better

Update minimum buy price for future calculations

The key insight: we always want to buy at the lowest price before selling
