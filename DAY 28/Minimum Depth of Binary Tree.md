## Problem Statement
Given a binary tree, find its minimum depth.

The minimum depth is the number of nodes along the shortest path from the root node down to the nearest leaf node.

**Note**: A leaf is a node with no children.

### Approach: Breadth-First Search (BFS)
This solution uses **Level-Order Traversal** (BFS) to find the minimum depth efficiently.

- BFS explores nodes level by level
- The first leaf node encountered will be at the minimum depth
- We can return immediately when we find the first leaf, avoiding unnecessary exploration

### Step-by-Step Process
1. **Base Case**: If root is null, return 0
2. **Initialize**: Create a queue and add root node, set initial depth to 1
3. **Level-by-Level Traversal**:
   - For each level, process all nodes currently in the queue
   - For each node, check if it's a leaf (both children are null)
   - If leaf found, return current depth (this is the minimum depth)
   - If not leaf, add non-null children to queue for next level
4. **Increment Depth**: After processing each level, increment depth counter


## Time & Space Complexity

- **Time Complexity**: O(n) in worst case
  - Best case: O(min_depth) when tree is skewed towards minimum depth
  - Worst case: O(n) when minimum depth leaf is the last node explored
  
- **Space Complexity**: O(w) where w is maximum width of tree
  - Queue stores at most one complete level of nodes
  - For balanced tree: O(n/2) = O(n)
  - For skewed tree: O(1)


    
    if (root.left == null && root.right == null) return 1;
    
    if (root.left == null) return minDepth(root.right) + 1;
    if (root.right == null) return minDepth(root.left) + 1;
    
    ret
