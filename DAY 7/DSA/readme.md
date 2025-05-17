**Problem Statement**

Given the head of a singly linked list, rotate the list to the right by k places.

**Approach**

To rotate the list to the right:

Calculate the Length of the linked list.

Make it Circular: Connect the last node to the head to form a loop.

Adjust k: If k > length, do k = k % length to avoid extra rotations.

Find the new Tail: It will be at length - k position. (this step is avoided when asked for left rotation)

Break the Circle: Set the new head and break the circular link.
