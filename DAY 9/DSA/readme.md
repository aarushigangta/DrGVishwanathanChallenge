**Problem Statement**

You are given the head of a linked list, and an integer k.
Return the head of the linked list after swapping the values of the kth node from the beginning and the kth node from the end (the list is 1-indexed).

**Approach**

Let's use two more pointers first and second, denoting the nodes for swapping

Put slow at head, and put fast k-1 nodes after slow.

first = fast.

If fast isn't already at the last node, move slow and fast one node further until fast.next == null

second = slow

Swap the values of first and second
