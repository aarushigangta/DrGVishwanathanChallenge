**Problem statement**

Given the head of a linked list head, in which each node contains an integer value.

Between every pair of adjacent nodes, insert a new node with a value equal to the greatest common divisor of them.

Return the linked list after insertion.

The greatest common divisor of two numbers is the largest positive integer that evenly divides both numbers.

**Approach**

Initialization:

Start by checking if the linked list contains only one node. If so, no insertions are needed, so return the head as it is.

Traversal and Insertion:

Use two pointers: node1 to represent the current node and node2 to represent the next node.

Compute the GCD of the values in node1 and node2.

Create a new node with the computed GCD and insert it between node1 and node2.
Update the pointers:

Set node1.next to the new GCD node.

Set the new GCD node's next to node2.

Move node1 to node2 and node2 to the next node of node2.

Repeat this until node2 is null.

Return: Once the traversal is complete and all necessary nodes are inserted, return the head of the modified list.
