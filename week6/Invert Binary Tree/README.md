Problem

Given the root of a binary tree, invert the tree and return its root.

Inverting a binary tree means swapping the left and right children of every node.

Example 1

Input:

root = [4, 2, 7, 1, 3, 6, 9]

Output:

[4, 7, 2, 9, 6, 3, 1]

Example 2

Input:

root = [2, 1, 3]

Output:

[2, 3, 1]

Approach 1: Recursive Solution

Use recursion to swap the left and right children of every node.

Steps

Check if the current node is null.

Store the left child in a temporary variable.

Set the left child to the right child.

Set the right child to the temporary variable.

Recursively invert the left and right subtrees.

Return the root.

Java Solution

class Solution {
    public TreeNode invertTree(TreeNode root) {
        if (root == null) {
            return null;
        }

        TreeNode temp = root.left;
        root.left = root.right;
        root.right = temp;

        invertTree(root.left);
        invertTree(root.right);

        return root;
    }
}

Approach 2: Iterative Solution

Use a Stack instead of recursion.

Steps

If the root is null, return null.

Push the root into the stack.

While the stack is not empty:

Pop a node.

Swap its left and right children.

Push the left child if it exists.

Push the right child if it exists.

Return the root.

Java Solution

class Solution {
    public TreeNode invertTree(TreeNode root) {
        if (root == null) {
            return null;
        }

        Stack<TreeNode> stack = new Stack<>();
        stack.push(root);

        while (!stack.isEmpty()) {
            TreeNode node = stack.pop();

            TreeNode temp = node.left;
            node.left = node.right;
            node.right = temp;

            if (node.left != null) {
                stack.push(node.left);
            }

            if (node.right != null) {
                stack.push(node.right);
            }
        }

        return root;
    }
}

Complexity Analysis

Let n be the number of nodes and h be the height of the tree.

Complexity

Recursive

Iterative

Time

O(n)

O(n)

Space

O(h)

O(n)

Time Complexity: O(n) — Every node is visited exactly once.

Recursive Space Complexity: O(h) — The recursion call stack stores nodes along the current path.

Iterative Space Complexity: O(n) — The Stack may store multiple nodes.

Key Concepts Learned

Binary Trees

Tree Traversal

Recursion

Stack (LIFO)

Swapping Nodes

Depth-First Search (DFS)

Time and Space Complexity

Conclusion

Invert Binary Tree swaps the left and right children of every node.

The recursive solution uses function calls, while the iterative solution uses a Stack.

Both solutions achieve O(n) time complexity.
