LeetCode 104 - Maximum Depth of Binary Tree

Problem

Find the maximum depth of a binary tree.

Maximum depth means the number of levels from the root to the deepest leaf.

My Approach

I used recursion to solve this problem.

First, I check if the root is null. If it is null, I return 0.

Then I find the depth of the left subtree.

After that, I find the depth of the right subtree.

I use Math.max() to choose the bigger depth.

Finally, I add 1 for the current node.

Code

class Solution {
    public int maxDepth(TreeNode root) {
        if (root == null) {
            return 0;
        }

        int left = maxDepth(root.left);
        int right = maxDepth(root.right);

        return 1 + Math.max(left, right);
    }
}

Complexity

Time Complexity: O(n) - because we visit every node once.

Space Complexity: O(h) - because of recursion.

What I Learned

How recursion works with binary trees.

How to find the maximum depth.

How to use Math.max()
