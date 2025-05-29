## Problem Statement

You are given two **non-empty** linked lists representing two non-negative integers. The digits are stored in **reverse order**, and each of their nodes contains a single digit. Add the two numbers and return the sum as a linked list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.

## Examples

**Example 1:**

Input: l1 = [2,4,3], l2 = [5,6,4]

Output: [7,0,8]

Explanation: 342 + 465 = 807.

**Example 2:**


Input: l1 = [0], l2 = [0]

Output: [0]

**Example 3:**

Input: l1 = [9,9,9,9,9,9,9], l2 = [9,9,9,9]

Output: [8,9,9,9,0,0,0,1]

## Solution Approach

This solution uses a **single-pass iteration** approach to add corresponding digits from both linked lists while managing carry-over values.

### Key Components

1. **Dummy Node**: Simplifies result list construction by providing a consistent starting point
2. **Carry Management**: Handles digit sums that exceed 9 by carrying over to the next position
3. **Unequal Length Handling**: Continues processing even when one list is exhausted
4. **Final Carry**: Ensures any remaining carry is added as a new node

### Algorithm Steps

1. Create a dummy node to build the result list
2. Initialize carry to 0 and iterate while nodes exist or carry remains
3. For each position:
   - Start with carry from previous position
   - Add current digit from l1 (if exists)
   - Add current digit from l2 (if exists)
   - Calculate new digit: `total % 10`
   - Calculate new carry: `total / 10`
   - Create new node with the digit
   - Move to next nodes in both lists
4. Return the result starting from dummy.next

