## Problem Statement

Design a stack that supports push, pop, top, and retrieving the minimum element in constant time.

Implement the MinStack class:

1. MinStack() initializes the stack object.
2. void push(int val) pushes the element val onto the stack.
3. void pop() removes the element on the top of the stack.
4. int top() gets the top element of the stack.
5. int getMin() retrieves the minimum element in the stack.
6. You must implement a solution with O(1) time complexity for each function.

## Approach

The solution uses two stacks:

1. Main Stack (stack): Stores all the actual elements
2. Min Stack (minStack): Stores the minimum value at each level
3. When pushing a new element, store the current minimum (either the new element or the previous minimum) in minStack
4. When popping, remove from both stacks simultaneously
5. The top of minStack always contains the current minimum

## Complexity

Time Complexity:

push(): O(1) - Just two stack pushes and one comparison

pop(): O(1) - Just two stack pops

top(): O(1) - One stack peek

getMin(): O(1) - One stack peek

Space Complexity: O(n)


 
