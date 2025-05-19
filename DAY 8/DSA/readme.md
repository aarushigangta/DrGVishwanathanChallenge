**Problem statement**

Given the head of a singly linked list, group all the nodes with odd indices together followed by the nodes with even indices, and return the reordered list.

The first node is considered odd, and the second node is even, and so on.

Note that the relative order inside both the even and odd groups should remain as it was in the input.

You must solve the problem in O(1) extra space complexity and O(n) time complexity.

**Approach**

We use two pointers to separate the list into:

An odd-indexed list

An even-indexed list

We then link the last node of the odd list to the head of the even list.

Steps:

Edge Case Check:

If the list is empty or contains only one node, return the head.

Initialize Pointers:

odd → first node

even → second node

evenHead → stores the start of even list for final connection

Traversal:

While even and even.next are not null:

Connect odd.next to even.next (next odd node)

Move odd forward

Connect even.next to odd.next (next even node)

Move even forward

Connect:

Append the even list at the end of the odd list (odd.next = evenHead)

Return:

Modified head of the list
