Given the root of a binary tree, return the preorder traversal of its nodes' values.

Preorder traversal follows this order:

Root → Left → Right**

 Example 1

Input:
text
root = [1, null, 2, 3]


Output:
text
[1, 2, 3]


 Example 2

Input:
text
root = [1, 2, 3, 4, 5, null, 8, null, null, 6, 7, 9]


Output:
text
[1, 2, 4, 5, 6, 7, 3, 8, 9]


 Approach 1: Recursive Solution

Use recursion to visit each node.

1. Check if the current node is null.
2. Add the current node's value to the result.
3. Recursively traverse the left subtree.
4. Recursively traverse the right subtree.

 Java Solution

java
class Solution {
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> result = new ArrayList<>();

        preorder(root, result);

        return result;
    }

    private void preorder(TreeNode node, List<Integer> result) {
        if (node == null) {
            return;
        }

        result.add(node.val);

        preorder(node.left, result);
        preorder(node.right, result);
    }
}


 Approach 2: Iterative Solution

Use a Stack instead of recursion.

1. If the root is null, return an empty list.
2. Push the root into the stack.
3. While the stack is not empty:
   - Pop a node.
   - Add its value to the result.
   - Push the right child first.
   - Push the left child second.

The left child is processed first because Stack follows the LIFO principle (Last In, First Out).

 Java Solution

java
class Solution {
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> result = new ArrayList<>();

        if (root == null) {
            return result;
        }

        Stack<TreeNode> stack = new Stack<>();
        stack.push(root);

        while (!stack.isEmpty()) {
            TreeNode node = stack.pop();

            result.add(node.val);

            if (node.right != null) {
                stack.push(node.right);
            }

            if (node.left != null) {
                stack.push(node.left);
            }
        }

        return result;
    }
}

 Complexity Analysis

Let n be the number of nodes and **h** be the height of the tree.

| Complexity | Recursive | Iterative |
|---|---|---|
| Time | O(n) | O(n) |
| Space | O(h) | O(h) |

Time Complexity: O(n)** — Every node is visited exactly once.
Space Complexity: O(h)** — Recursion call stack or explicit stack stores nodes along the traversal.

 Key Concepts Learned

 Binary Trees
 Preorder Traversal
 Depth-First Search (DFS)
 Recursion
 Stack (LIFO)
 Time and Space Complexity

 Conclusion

Preorder Traversal visits nodes in the order Root → Left → Right.

The recursive solution is straightforward, while the iterative solution uses a Stack to perform the same traversal without recursion.

Both solutions achieve O(n) time complexity**.
