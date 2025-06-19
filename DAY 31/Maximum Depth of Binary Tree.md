## Problem Statement

Given the root of a binary tree, return its maximum depth.

A binary tree's maximum depth is the number of nodes along the longest path from the root node down to the farthest leaf node.

## Approach

1. If the current node (root) is None ,return 0 because an empty subtree has a depth of 0.
2. The function makes recursive calls to compute: The depth of the left subtree (self.maxDepth(root.left)) and the depth of the right subtree (self.maxDepth(root.right)).
3. After computing the depths of the left and right subtrees: Use max(self.maxDepth(root.left), self.maxDepth(root.right)) to get the maximum depth of the two subtrees and Add 1 to account for the current node.

