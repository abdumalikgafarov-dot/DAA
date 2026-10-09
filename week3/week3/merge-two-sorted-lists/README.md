# Merge Two Sorted Lists

## 1. Problem

We have two sorted linked lists. We need to merge them into one sorted list.

## 2. Approach

I use a dummy node and a current pointer.

First, I compare the values of both lists. If `list1.val` is smaller or equal, I take the node from `list1`. Otherwise, I take the node from `list2`.

After that, I move the pointers to the next nodes. I repeat this until one list becomes empty. Then I connect the rest of the other list.

At the end, I return `dummy.next`.

### Example

Input:

`list1 = [1, 2, 4]`

`list2 = [1, 3, 4]`

* First, I compare 1 and 1. I take 1 from `list1`.
* Then I compare 2 and 1. I take 1 from `list2`.
* Then I compare 2 and 3. I take 2 from `list1`.
* Then I take 3 from `list2`.
* After that, I take 4 and 4.
* The final result is `[1, 1, 2, 3, 4, 4]`.

## 3. Time Complexity

**O(n + m)**

We go through the nodes of both lists. Each node is processed once.

## 4. Space Complexity

**O(1)**

I use only a few extra pointers and reuse the existing nodes.

## 5. Reflection / Improvement

I think this solution is already efficient. It checks each node only once. It is possible to write the code shorter, but the time complexity will stay the same.
