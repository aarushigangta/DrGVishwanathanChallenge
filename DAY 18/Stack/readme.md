## Problem Statement

Implement a first in first out (FIFO) queue using only two stacks. The implemented queue should support all the functions of a normal queue (push, peek, pop, and empty).

Implement the MyQueue class:

1. void push(int x) Pushes element x to the back of the queue.
2. int pop() Removes the element from the front of the queue and returns it.
3. int peek() Returns the element at the front of the queue.
4. boolean empty() Returns true if the queue is empty, false otherwise.

Notes:

You must use only standard operations of a stack, which means only push to top, peek/pop from top, size, and is empty operations are valid.
Depending on your language, the stack may not be supported natively. You may simulate a stack using a list or deque (double-ended queue) as long as you use only a stack's standard operations.

## Approach

Stacks operate on a Last In, First Out (LIFO) principle, which is the opposite of a queue. To simulate a queue using two stacks, we use the following approach:


Input stack: Stores elements as they are added.

Output stack: Reverses the order of elements from the input stack, allowing us to access the front of the queue.

The key idea is to transfer elements from the input stack to the output stack when we need to access the front of the queue. This transfer reverses the order, making the oldest element (FIFO) accessible.


 
