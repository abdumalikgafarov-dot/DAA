# Linked List Cycle

## Problem

We need to check if a linked list has a cycle.

If a node appears again, it means there is a cycle. If we reach `null`, there is no cycle.

## Approach

I used a `HashSet` to remember visited nodes.

* First, I check if the head is null.
* Then I check each node.
* If the node is already in the set, I return `true`.
* Otherwise, I add it to the set and move to the next node.
* If I reach null, I return `false`.

## Trace

Example: `1 -> 2 -> 3 -> 2`

1. Visit node 1 and add it to the set.
2. Visit node 2 and add it to the set.
3. Visit node 3 and add it to the set.
4. Node 2 appears again.
5. Return `true`.

## Time Complexity

**O(n)** — We visit each node at most once before finding a cycle or reaching null.

## Space Complexity

**O(n)** — The set can store all nodes if there is no cycle.

## Reflection

The solution is simple and easy to understand. But it uses extra memory. I can try the slow and fast pointer method to reduce the extra space to O(1).
