## Problem Statement

Given the root of a binary tree, return the inorder traversal of its nodes' values.

Example 1:

Input: root = [1,null,2,3]

Output: [1,3,2]



## Approach

The solution uses a classic recursive approach following the inorder pattern:

1. Traverse left subtree recursively
2. Process current node (add to result)
3. Traverse right subtree recursively
