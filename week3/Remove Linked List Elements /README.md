# Linked List Assignment

## Overview

This assignment contains solutions to two LeetCode problems about Linked Lists. The goal is to practice working with nodes, references, and linked list traversal in Java.

## Problems

### 1. Remove Duplicates from Sorted List (LeetCode 83)

**Problem:** Remove duplicate values from a sorted linked list. Each value must appear only once.

**Example:**

Input:
`1 -> 1 -> 2 -> 3 -> 3 -> null`

Output:
`1 -> 2 -> 3 -> null`

**Approach:**
- Use a pointer called `current` to traverse the list.
- Compare the current node with the next node.
- If their values are equal, remove the next node.
- Otherwise, move `current` to the next node.
- Return the head of the list.

### 2. Intersection of Two Linked Lists (LeetCode 160)

**Problem:** Find the node where two linked lists intersect. If they do not intersect, return `null`.

**Approach:**
- Use two pointers, one for each linked list.
- Move both pointers one node at a time.
- When a pointer reaches the end of its list, move it to the beginning of the other list.
- If the lists intersect, the pointers will meet at the intersection node.
- If they do not intersect, both pointers will eventually become `null`.

## Technologies

- Java
- LeetCode
- IntelliJ IDEA

## What I Learned

- How to traverse a linked list.
- How to compare node values.
- How to remove duplicate nodes.
- How to work with references between nodes.
- How to use two pointers to find the intersection of linked lists.

## Conclusion

This assignment helped me understand linked list operations and practice solving data structure problems in Java.
