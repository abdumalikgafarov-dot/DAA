Problem

Given the root of a binary tree, return all paths from the root to the leaf nodes.

A leaf is a node that has no left or right child.

Example 1

Input:

root = [1, 2, 3, null, 5]

Output:

["1->2->5", "1->3"]

Approach 1: Recursive Solution

I use recursion to find all paths from the root to the leaves.

Steps

Start from the root node.

Add the current node value to the path.

Check if the node is a leaf.

If it is a leaf, add the path to the result.

If it is not a leaf, continue to the left and right children.

Return to the previous path using backtracking.

Java Solution

class Solution {
    public List<String> binaryTreePaths(TreeNode root) {
        List<String> result = new ArrayList<>();

        dfs(root, new StringBuilder(), result);

        return result;
    }

    private void dfs(TreeNode node, StringBuilder path,
                     List<String> result) {
        if (node == null) {
            return;
        }

        int length = path.length();

        if (length > 0) {
            path.append("->");
        }

        path.append(node.val);

        if (node.left == null && node.right == null) {
            result.add(path.toString());
        } else {
            dfs(node.left, path, result);
            dfs(node.right, path, result);
        }

        path.setLength(length);
    }
}

Explanation

result stores all root-to-leaf paths.

StringBuilder is used to build the path.

path.append(node.val) adds the current node value.

If the node has no children, the path is saved.

dfs() continues to the left and right children.

path.setLength(length) removes the last added part and returns to the previous path.

Approach 2: Iterative Solution

I use two Stacks instead of recursion.

One Stack stores tree nodes and the second Stack stores the paths.

Steps

Check if the root is null.

Add the root and its path to the Stacks.

While the Stack is not empty, take a node and its path.

If the node is a leaf, add the path to the result.

Add the right child and its path if it exists.

Add the left child and its path if it exists.

Return the result.

Java Solution

class Solution {
    public List<String> binaryTreePaths(TreeNode root) {
        List<String> result = new ArrayList<>();

        if (root == null) {
            return result;
        }

        Stack<TreeNode> nodeStack = new Stack<>();
        Stack<String> pathStack = new Stack<>();

        nodeStack.push(root);
        pathStack.push(String.valueOf(root.val));

        while (!nodeStack.isEmpty()) {
            TreeNode node = nodeStack.pop();
            String path = pathStack.pop();

            if (node.left == null && node.right == null) {
                result.add(path);
            }

            if (node.right != null) {
                nodeStack.push(node.right);
                pathStack.push(path + "->" + node.right.val);
            }

            if (node.left != null) {
                nodeStack.push(node.left);
                pathStack.push(path + "->" + node.left.val);
            }
        }

        return result;
    }
}

Explanation

nodeStack stores the nodes.

pathStack stores the paths for each node.

pop() removes the last element from the Stack.

When a leaf is found, its path is added to result.

The algorithm continues until the Stack is empty.

Complexity Analysis

Let n be the number of nodes and h be the height of the tree.

Complexity

Recursive

Iterative

Time

O(n × h)

O(n × h)

Space

O(h)

O(n × h)

Time Complexity: Each node is visited once, and paths are built along the way.

Recursive Space: The recursion stack and current path use memory.

Iterative Space: The Stacks store nodes and their paths.

What I learned

Binary Trees

DFS (Depth-First Search)

Recursion

Stack

StringBuilder

Backtracking

Root-to-Leaf Paths

Time and Space Complexity
