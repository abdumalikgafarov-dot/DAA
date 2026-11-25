Problem

Find the sum of all left leaf nodes in a binary tree.

A leaf is a node that has no children. A left leaf is a leaf that is the left child of another node.

Approach

I used DFS (Depth-First Search) with recursion.

First, I check if the current node is null.

Then, I check the left child.

If the left child has no children, I add its value to the sum.

Otherwise, I continue searching in the left subtree.

I also check the right subtree because it can contain left leaves.

Finally, I return the total sum.

Example

Input: [3,9,20,null,null,15,7]

Output: 24

Explanation:

9 is a left leaf.

15 is a left leaf.

7 is a right leaf, so I don't count it.

Sum = 9 + 15 = 24.

Complexity

Time Complexity: O(n) – I visit each node once.

Space Complexity: O(h) – Recursion uses stack space based on the tree height.

What I Learned

I learned how to find left leaves using DFS and recursion. I also practiced checking whether a node has children.
