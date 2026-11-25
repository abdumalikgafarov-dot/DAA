Problem

Merge two binary trees into one tree.

If two nodes overlap, I add their values. If only one node exists, I keep that node.

Approach

I used DFS (Depth-First Search) with recursion.

First, I check if the first tree is null.

Then, I check if the second tree is null.

If both nodes exist, I add their values.

I recursively merge the left children.

I recursively merge the right children.

Finally, I return the merged tree.

Example

Input:

Tree 1: [1,3,2,5]

Tree 2: [2,1,3,null,4,null,7]

Output: [3,4,5,5,4,null,7]

Complexity

Time Complexity: O(n) – I visit each overlapping node once.

Space Complexity: O(h) – Recursion stack depends on the tree height.

What I Learned

I learned how to merge two binary trees using DFS and recursion. I also practiced working with two trees at the same time.
