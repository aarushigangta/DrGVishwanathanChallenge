**Problem Statement**

Given the head of a singly linked list and an integer val, remove all the nodes of the linked list that have val as their value, and return the new head.

**Approach**

This solution uses a dummy node to handle edge cases smoothly—such as when the head node itself needs to be deleted.

Steps

Create a dummy node:

Initialize a dummy node with value 0 and point its next to head.

This helps easily return the new head even if the first few nodes are removed.

Use a curr pointer to traverse:

While curr.next is not null:

If curr.next.val == val, skip the node by setting curr.next = curr.next.next.

Otherwise, move curr to the next node.

Return dummy.next, which points to the updated list.
