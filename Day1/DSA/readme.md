Reverse a Singly Linked List

This repository contains a Java implementation to reverse a singly linked list.

Problem Statement
Given the head of a singly linked list, reverse the list and return the new head.

Example
Input: 1 → 2 → 3 → 4 → 5

Output: 5 → 4 → 3 → 2 → 1 

Approach
The approach used is iterative reversal using three pointers:

prevnode – initially null, holds the previous node.

currnode – starts at head, traverses the list.

nextnode – temporarily holds the next node.

Steps:
Iterate through the list.

For each node, reverse its next pointer.

Move forward by updating prevnode and currnode.
