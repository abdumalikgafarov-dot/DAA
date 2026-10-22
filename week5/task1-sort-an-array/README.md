Task 1: Sort an Array

1. Problem

The task is to sort an array from smallest to biggest.

Example: [5, 2, 3, 1] → [1, 2, 3, 5]

2. Approach

I used Merge Sort. First, I divide the array into two parts. Then I sort both parts and merge them.

Example:

[5, 2, 3, 1]

[5, 2] and [3, 1]

[2, 5] and [1, 3]

Final result: [1, 2, 3, 5]

At first, I needed to understand how to merge two sorted arrays correctly. I would test empty arrays, duplicate numbers, and negative numbers.

3. Time and Space Complexity

Time: O(n log n), because the array is divided into smaller parts and merged at each level.

Space: O(n), because temporary arrays are needed.

4. Improvement

Merge Sort is already efficient. It is better than simple Bubble Sort for large arrays.
