## Problem Statement

Given an array nums of size n, return the majority element.
The majority element is the element that appears more than ⌊n / 2⌋ times. You may assume that the majority element always exists in the array.

## Approach

We used Boyer-Moore Majority Vote Algorithm in this question where:
1. Each occurrence of the current candidate gets a +1 vote
2. Each occurrence of a different element gets a -1 vote
3. When votes reach 0, we switch candidates
4. The majority element will always "survive" this battle

Since the majority element appears more than n/2 times, even if every other element "cancels out" one occurrence of the majority element, the majority will still have leftover occurrences
