## Problem Statement

You are given an array of strings tokens that represents an arithmetic expression in a Reverse Polish Notation.

Evaluate the expression. Return an integer that represents the value of the expression.

Note that:

1. The valid operators are '+', '-', '*', and '/'.
2. Each operand may be an integer or another expression.
3. The division between two integers always truncates toward zero.
4. There will not be any division by zero.
5. The input represents a valid arithmetic expression in a reverse polish notation.
6. The answer and all the intermediate calculations can be represented in a 32-bit integer.

## Approach

Input: tokens = ["2","1","+","3","*"]

First of all, we find 2. Add 2 to stack. And one more important thing is that we should convert string 2 to integer 2 because we have to calculate them when we find a operator.

["2","1","+","3","*"]

stack = [2]

Next, we find 1.

["2","1","+","3","*"]

stack = [2, 1]

Next, we find +. Now we have 2 and 1 in stack. Take them and calculate addtion.

1 + 2 = 3

After calculation, we push back the answer to stack because we want to use the answer for future calculation.

stack = [3]

Next, we find 3 in input array. Add 3 to stack.

["2","1","+","3","*"]

stack = [3, 3]

Next we find *. Take two 3 in stack and

3 * 3 = 9

And push 9 back to stack.

stack = [9]

Next, we reach the end of input array

return 9 (= stack[0])

Wait! There is one more important point.


For instance, we have 5 and 10 in stack. Addtion and Multiplication are fine if

stack = [10, 5]
10 + 5 = 15
5 + 10 = 15

10 * 5 = 50
5 * 10 = 50

But how about substraction and division.

10 - 5 = 5
5 - 10 = -5

10 / 5 = 2
5 / 10 = 0.5

The order of numbers is very important. Point is the first poped number from stack will be the second number in calucation.

stack = [10, 5]

At first, pop 5. → This is the second number in calcuation.

Second, pop 10. → This is the first number in calcuation.
