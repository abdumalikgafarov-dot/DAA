# Intersection of Two Linked Lists

## Problem
We need to find where two linked lists intersect. If they don't intersect, return null.

## Approach
I used two while loops. The first loop goes through list A, and the second loop checks every node in list B. If both nodes are the same, I return the node. If there is no intersection, I return null.

## Time Complexity
**O(m * n)** because we check each node of A with every node of B.

**Space Complexity: O(1)** because I only use two variables.

## Reflection
This solution works, but it can be slow for big lists. We can make it faster with O(m + n) time.
