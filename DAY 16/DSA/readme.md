Problem Statement
------------------
There is a singly-linked list head and we want to delete a node node in it.

You are given the node to be deleted node. You will not be given access to the first node of head.

All the values of the linked list are unique, and it is guaranteed that the given node node is not the last node in the linked list.

Delete the given node. Note that by deleting the node, we do not mean removing it from memory. We mean:

The value of the given node should not exist in the linked list.
The number of nodes in the linked list should decrease by one.
All the values before node should be in the same order.
All the values after node should be in the same order.

Approach
--------------------
Since we cannot access the previous node to update its next pointer, we use:

1. Copy the value from the next node into the current node
2. Skip the next node by updating the current node's next pointer

This deletes the current node by overwriting it with the next node's data and removing the next node from the chain.

Time and Space Complexity
-------------------------
Time Complexity: O(1) - Only two operations regardless of list size
Space Complexity: O(1) - No additional space used

