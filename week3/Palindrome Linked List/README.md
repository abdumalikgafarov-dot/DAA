LeetCode 234 - Palindrome Linked List

Problem Description

Given the head of a singly linked list, determine whether the linked list is a palindrome.

Return true if it is a palindrome, and false otherwise.

Approach

I solved this problem using the two-pointer technique and linked list reversal.

Find the middle: I use two pointers, slow and fast. The slow pointer moves one step, while the fast pointer moves two steps.

Reverse the second half: I reverse the links using prev, current, and next.

Compare both halves: I compare the values of the nodes. If any values are different, I return false.

Return the result: If all compared values match, I return true.

Complexity Analysis

Time Complexity: O(n), because I traverse the linked list a constant number of times.

Space Complexity: O(1), because I use only a constant number of pointers.

What I Learned

I practiced using two pointers, reversing a linked list, and comparing node values without creating an additional list.
