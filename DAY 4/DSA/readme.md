**Problem Statement**

Given the head of a singly linked list, determine if the linked list has a cycle in it.

A linked list has a cycle if any node in the list is visited more than once while traversing the list.

**Approach**

We use Floyd’s Cycle Detection Algorithm (Tortoise and Hare algorithm):

Use two pointers: slow and fast.

slow moves one step at a time, while fast moves two steps.

If there is a cycle, the two pointers will eventually meet.

If fast reaches the end (null), then the list has no cycle.
