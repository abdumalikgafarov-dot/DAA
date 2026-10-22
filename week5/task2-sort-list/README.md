Task 2: Sort List

1. Problem

The task is to sort a linked list from smallest to biggest.

Example: 4 -> 2 -> 1 -> 3 → 1 -> 2 -> 3 -> 4

2. Approach

I used Merge Sort. I find the middle of the list using slow and fast pointers. Then I divide the list, sort both parts, and merge them.

Example:

4 -> 2 -> 1 -> 3

4 -> 2 and 1 -> 3

2 -> 4 and 1 -> 3

Final result: 1 -> 2 -> 3 -> 4

The difficult part was splitting the list correctly. I would test an empty list, one node, and a list with duplicate numbers.

3. Time and Space Complexity

Time: O(n log n), because the list is divided into smaller parts and merged.

Space: O(log n), because of recursive calls.

4. Improvement

Merge Sort works well for linked lists. An iterative version can reduce extra memory usage.
