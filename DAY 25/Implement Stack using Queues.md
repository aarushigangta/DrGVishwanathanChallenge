## Problem Statement

Implement a last-in-first-out (LIFO) stack using only two queues. The implemented stack should support all the functions of a normal stack (push, top, pop, and empty).

Implement the MyStack class:

1. void push(int x) Pushes element x to the top of the stack.
2. int pop() Removes the element on the top of the stack and returns it.
3. int top() Returns the element on the top of the stack.
4. boolean empty() Returns true if the stack is empty, false otherwise.

Notes:

You must use only standard operations of a queue, which means that only push to back, peek/pop from front, size and is empty operations are valid.
Depending on your language, the queue may not be supported natively. You may simulate a queue using a list or deque (double-ended queue) as long as you use only a queue's standard operations.

## Approach

1. Initialize a new instance of the MyStack class.
2. Create an empty deque named q to store the stack elements.
3. For push: Accept an integer x as input.
4. Append the input integer x to the right end of the deque q.
5. Loop for the number of times equal to the length of the deque minus one (length - 1).
6. In each iteration, remove an element from the left end of the deque (popleft) and immediately append it back to the right end.
7. This loop ensures that the last added element is at the front of the deque, simulating the behavior of a stack.
8. For pop: Remove and return the element from the left end of the deque q.
9. This operation effectively mimics the behavior of popping an element off the stack.
10. top Method:Return the element at the left end of the deque q without removing it.
11. This operation provides the top element of the stack without altering the stack itself.
12. empty Method:Check if the length of the deque q is equal to 0.
13. If the length is 0, the stack is empty, so return True; otherwise, return False.

## Complexity
Time complexity: pop, top and empty are O(1), push is O(n)

Space complexity: O(n)
