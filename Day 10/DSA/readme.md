**Problem statement**

You are given the head of a linked list. Delete the middle node, and return the head of the modified linked list.
The middle node of a linked list of size n is the ⌊n / 2⌋th node from the start using 0-based indexing, where ⌊x⌋ denotes the largest integer less than or equal to x.

**Approach**

If the list is empty (head == null) or has only one node (head.next == null), return null (since there's no middle node to delete).

Using Two Pointers (Slow and Fast):

Initialize:

slow → starts at head, moves one step per iteration.

fast → starts at head, moves two steps per iteration.

prev → keeps track of the node before slow.

Traversing the list until fast reaches the end (null).

When fast is at the last node or null, slow will be at the middle node.

prev.next = slow.next → removes the middle node from the list.

Return the Modified List.
