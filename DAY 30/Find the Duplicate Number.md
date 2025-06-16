## Algorithm

Given an array of integers nums containing n + 1 integers where each integer is in the range [1, n] inclusive.

There is only one repeated number in nums, return this repeated number.

You must solve the problem without modifying the array nums and using only constant extra space.

## Approach

1. Initialize slow and fast pointers to the first element of the input list nums.
2. Enter a loop to detect a cycle:

a. Update slow to the next element using nums[slow].

b. Update fast to the next element after nums[fast], effectively moving two steps.

c. Check if slow is equal to fast. If they are equal, a cycle has been found, and exit the loop.
3. After finding the cycle, reset one of the pointers (slow2) to the beginning of the list.
4. Enter a loop to find the duplicate element:

a. Update slow using nums[slow].

b. Update slow2 using nums[slow2].

c. Continue this process until slow is equal to slow2, which represents the duplicate element.
5. Return the duplicate element found (slow).
