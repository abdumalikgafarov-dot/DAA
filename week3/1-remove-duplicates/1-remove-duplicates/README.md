# Remove Duplicates from Sorted List

## Problem
We need to remove same numbers from sorted linked list.

Example: `1 → 1 → 2 → 3 → 3`

Output: `1 → 2 → 3`

## Approach
I used while loop to check current node and next node. If values are same, I skip next node. If not, I move to next node. I continue until the end of list.

## Time Complexity
**O(n)** because we go through the list one time.

**Space Complexity: O(1)** because we use only one variable.

## Reflection
This solution is good because it is simple and does not need extra memory.
