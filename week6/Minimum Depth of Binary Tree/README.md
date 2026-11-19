LeetCode 111 - Minimum Depth of Binary Tree

Problem

Find the minimum depth of a binary tree.

Minimum depth means the shortest path from the root to the nearest leaf.

My Approach

I used recursion to solve this problem.

First, I check if the root is null. If it is null, I return 0.

If the left child is null, I continue with the right subtree.

If the right child is null, I continue with the left subtree.

If both children exist, I use Math.min() to find the smaller depth.

I add 1 for the current node.

Code

class Solution {
    public int minDepth(TreeNode root) {
        if (root == null) {
            return 0;
        }

        if (root.left == null) {
            return 1 + minDepth(root.right);
        }

        if (root.right == null) {
            return 1 + minDepth(root.left);
        }

        return 1 + Math.min(minDepth(root.left), minDepth(root.right));
    }
}

Complexity

Time Complexity: O(n) - because we may visit every node.

Space Complexity: O(h) - because of recursion.

What I Learned

How to find the minimum depth of a binary tree.

How to use recursion.

How to use Math.min().

Why we need to check if a child is null.
