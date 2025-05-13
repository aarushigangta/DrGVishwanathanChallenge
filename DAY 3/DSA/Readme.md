**Problem Statement**

Given the heads of two sorted singly linked lists, list1 and list2.
Our task is to merge the two lists into one sorted list and return the head of the merged list.

**Approach**

A dummy node is used to simplify list creation.

A pointer currNode tracks the current end of the merged list.

We iterate while both list1 and list2 are non-null, adding the smaller node to the merged list.

Once one list is finished, we append the remaining nodes of the other list.
