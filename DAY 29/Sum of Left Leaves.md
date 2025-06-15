## Problem Statement
Given the root of a binary tree, return the sum of all left leaves.

A **left leaf** is a leaf node that is the left child of another node.

## Approach: Depth-First Search (DFS) with Boolean Flag
This solution uses **recursive DFS** to traverse the tree while keeping track of whether each node is a left child.


1.  If current node is null, return 0
2.  If current node is a leaf (no children):
   - If it's a left child (`is_left == true`), return its value
   - If it's a right child (`is_left == false`), return 0
3. If current node has children:
   - Recursively call on left child with `is_left = true`
   - Recursively call on right child with `is_left = false`
   - Return sum of both recursive calls

### Boolean Flag Logic
- `dfs(root.left, true)` → Left child is marked as "left"
- `dfs(root.right, false)` → Right child is marked as "not left"
- Root node starts with `false` since it's not anyone's left child

## Time & Space Complexity

- **Time Complexity**: O(n)
  
- **Space Complexity**: O(h)
  - h = height of the tree (recursion stack depth)
  - Best case (balanced tree): O(log n)
  - Worst case (skewed tree): O(n)

