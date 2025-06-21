## Problem Statment

Given the root of a binary tree, return the level order traversal of its nodes' values (i.e., from left to right, level by level).

## Examples

### Example 1:
```
Input: root = [3,9,20,null,null,15,7]

    3
   / \
  9   20
    /  \
   15   7

Output: [[3],[9,20],[15,7]]
```

### Example 2:
```
Input: root = [1]
Output: [[1]]
```

### Example 3:
```
Input: root = []
Output: []
```

## Approach 

1. Use recursion with level parameter (starting at 0)
2. If visiting a level for the first time, create new list for that level
3. Otherwise, add node value to existing level list
4. Recursively traverse left subtree then right subtree with level + 1

## Complexity

**Time Complexity:** O(n) | **Space Complexity:** O(h) where h is the height of the tree

