## Problem Statement

Given the root of a binary tree and an integer targetSum, return true if the tree has a root-to-leaf path such that adding up all the values along the path equals targetSum.

## Approach

1. If root is None (i.e., the tree is empty or we reach a null node in recursion), return False.
2. If the current node does not have left or right children, it is a leaf node.
3. Check if targetSum - root.val == 0 (i.e., whether the remaining sum after subtracting root.val equals zero).
4. If True, return True because a valid path is found; otherwise, return False.
5. Subtract the current node's value from targetSum.
6. This reduces the problem to checking whether there exists a path in the left or right subtree with the updated targetSum.
7. Recursively call hasPathSum on the left and right children with the updated targetSum.
8. If either the left or right subtree has a valid path, return True (using the or operator).
9. If neither subtree contains a valid path, return False.
