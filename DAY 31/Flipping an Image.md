## Problem Statement
Given an n x n binary matrix image, flip the image horizontally, then invert it, and return the resulting image.

To flip an image horizontally means that each row of the image is reversed.

For example, flipping [1,1,0] horizontally results in [0,1,1].
To invert an image means that each 0 is replaced by 1, and each 1 is replaced by 0.

For example, inverting [0,1,1] results in [1,0,0].

## Approach

1. Loop through each row.
2. Use two pointers (j from start, x from end) to swap and invert elements at the same time
3. Invert both image[i][j] and image[i][x] using 1 - value.
4. Swap them.

This ensures both flipping and inversion happen in a single pass
