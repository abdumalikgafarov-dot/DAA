

 1. Problem Description

Given the root of a binary tree, return the inorder traversal of its nodes' values.

Inorder traversal means visiting nodes in this order:

1. Left subtree
2. Root node
3. Right subtree

 2. My Approach

I used a recursive solution.

First, I check if the current node is `null`. If it is null, the method stops.

Otherwise:
1. I visit the left child.
2. I add the current node's value to the result list.
3. I visit the right child.

This process continues until all nodes are visited.

 3. Written Tracing

Example input:

text
    1
     \
      2
     /
    3


Step-by-step execution:

1. Visit node 1. Its left child is null, so add 1.
2. Move to node 2.
3. Visit node 3 first and add 3.
4. Return to node 2 and add 2.

Final output:

text
[1, 3, 2]


 4. Challenges and Testing

At first, I was unsure how to name the Java file. I used `Solution.java` because the class is named `Solution`.

I ran the code on LeetCode. The test cases passed successfully.

5. Time Complexity

**O(n)** — Every node is visited exactly once, where n is the number of nodes in the tree.

6. Space Complexity

**O(n)** — The result list stores all n node values. The recursive call stack also uses memory, up to O(h), where h is the height of the tree. In the worst case, h can be n.

 7. Reflection and Possible Improvement

I learned how recursive inorder traversal works.

One possible improvement is to use an iterative approach with a Stack instead of recursion. This avoids using the recursive call stack. The time complexity remains O(n).
