## Problem Description

Given the head of a linked list and a value x, partition the linked list such that all nodes with values less than x come before nodes with values greater than or equal to x.
The original relative order of the nodes in each of the two partitions should be preserved.

## Algorithm Approach
This solution uses a two-pointer technique with dummy nodes to create two separate lists:

Small List: Contains all nodes with values < x

Big List: Contains all nodes with values ≥ x

Create two dummy head nodes (sList and bList) to simplify list construction

Traverse the original list once

For each node, append it to either the small list or big list based on its value

Connect the small list to the big list

Properly terminate the big list with null

Return the head of the partitioned list (skipping dummy nodes)
