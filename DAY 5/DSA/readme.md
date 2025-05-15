**Problem Statement**

Given the head of a singly linked list, determine whether it is a palindrome.

A palindrome is a sequence that reads the same backward as forward.

**Approach**

This solution uses the fast and slow pointer technique to find the midpoint of the list, reverses the second half, and then compares it with the first half to check for palindrome property.

Steps

Find the Middle:

Use two pointers slow and fast:

slow moves 1 step at a time.

fast moves 2 steps at a time.

When fast reaches the end, slow will be at the middle.

Reverse the Second Half:

Reverse the second half of the list starting from the slow node using a helper function reverse().

Compare Halves:

Iterate through both halves of the list and compare the values node-by-node.

Return Result:

If all corresponding nodes match, return true. Otherwise, return false.

