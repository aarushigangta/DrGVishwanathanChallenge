**Problem Statement**

Given the head of a singly linked list, return the middle node of the linked list.
If there are two middle nodes, return the second middle node.

**Approach**

This implementation uses the two-pointer technique:

1. slow moves one step at a time

2. fast moves two steps at a time

3. When fast reaches the end, slow will be at the middle
