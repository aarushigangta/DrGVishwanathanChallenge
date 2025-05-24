## Problem
Given the head of a **sorted linked list**, delete all nodes that have **duplicate numbers**, leaving only distinct numbers from the original list.

## Example
**Input:** `1 -> 2 -> 3 -> 3 -> 4 -> 4 -> 5`  
**Output:** `1 -> 2 -> 5`

## Approach
- Use a dummy node to handle cases where the first node(s) are duplicates.
- Use two pointers:
  - `head`: iterates through the list.
  - `prev`: tracks the last confirmed unique node.
- Skip all nodes with duplicate values.
- Connect `prev.next` to the first non-duplicate node after duplicates.

## Complexity
- **Time:** O(N)  
- **Space:** O(1)

## Notes
- Only works correctly for **sorted** linked lists.
- If input is not sorted, consider sorting first or using a HashMap (not constant space).
