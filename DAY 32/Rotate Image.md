## Problem statement

You are given an n x n 2D matrix representing an image, rotate the image by 90 degrees (clockwise).
You have to rotate the image in-place, which means you have to modify the input 2D matrix directly. DO NOT allocate another 2D matrix and do the rotation.

## Approach

### 1. Vertical Reversal Loop
- Iterate over rows until the middle of the matrix
- For each column, swap elements in the top and bottom rows

### 2. Transpose Loop
- Iterate through the upper triangular part of the matrix (excluding the diagonal)
- Swap the elements symmetrically across the diagonal


## Time and Space Complexity

- **Time Complexity**: O(n²) where n is the side length of the matrix
- **Space Complexity**: O(1) - in-place rotation with only temporary variables

