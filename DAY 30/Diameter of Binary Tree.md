# Diameter of Binary Tree

## Problem Statement
Given the root of a binary tree, return the length of the **diameter** of the tree.

The **diameter** of a binary tree is the **length of the longest path** between any two nodes in a tree. This path may or may not pass through the root.

The **length of a path** between two nodes is represented by the number of edges between them.

## Algorithm Explanation

### Approach: DFS with Global Variable
This solution uses **Depth-First Search (DFS)** to calculate the diameter while computing the height of each subtree.

1. If node is null, return height 0
2. Get heights of left and right subtrees
3. Calculate diameter through current node (l + r)
4. Keep track of maximum diameter seen so far
5. Return height of current subtree to parent

## Time & Space Complexity

- **Time Complexity**: O(n)
- **Space Complexity**: O(h)
 
