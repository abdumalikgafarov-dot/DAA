Find if the tree has a path from the root to a leaf with the given target sum.

My Approach

I used recursion to solve this problem.

First, I check if the root is null. If it is null, I return false.

Then I check if the current node is a leaf.

If it is a leaf, I compare targetSum with the node value.

I subtract the current node value from targetSum.

I check the left and right subtrees.

If one path has the correct sum, I return true.


Complexity

Time Complexity: O(n) - because we may visit every node.

Space Complexity: O(h) - because of recursion.

What I Learned

How to use recursion in a binary tree.

How to check a root-to-leaf path.

How to calculate the remaining sum.

How to use boolean and logical operators.
