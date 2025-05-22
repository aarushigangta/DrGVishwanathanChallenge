**Problem statement**

Given the head of a linked list, remove the nth node from the end of the list and return its head.

**Approach**

Initialize two pointers fast and slow at the head.

Move the fast pointer n steps forward.

If fast becomes null after moving n steps, that means we need to remove the first node. So we return head.next.

Traverse Till End:

Move both fast and slow until fast.next is null.

slow will be right before the node to remove.

Set slow.next = slow.next.next to skip the desired node.

