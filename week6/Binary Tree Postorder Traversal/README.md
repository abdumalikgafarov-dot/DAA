Problem

Given the root of a binary tree, return the postorder traversal of its nodes' values.

Postorder traversal follows this order:

Left → Right → Root

Example 1

Input:

text
root = [1, null, 2, 3]


Output:

text
[3, 2, 1]


 Example 2

Input:

text
root = [1, 2, 3, 4, 5, null, 8, null, null, 6, 7, 9]


Output:

text
[4, 6, 7, 5, 2, 9, 8, 3, 1]


 Approach 1: Recursive Solution

Use recursion to traverse the binary tree.

1. Check if the current node is null.
2. Recursively traverse the left subtree.
3. Recursively traverse the right subtree.
4. Add the current node's value to the result.

 Java Solution

java
class Solution {
    public List<Integer> postorderTraversal(TreeNode root) {
        List<Integer> result = new ArrayList<>();

        postorder(root, result);

        return result;
    }

    private void postorder(TreeNode node, List<Integer> result) {
        if (node == null) {
            return;
        }

        postorder(node.left, result);

        postorder(node.right, result);

        result.add(node.val);
    }
}


 Approach 2: Iterative Solution

Use a Stack instead of recursion.

The idea is to traverse the tree in the order:

Root → Right → Left

Then reverse the result to get:

Left → Right → Root

 Steps

1. If the root is null, return an empty list.
2. Push the root into the stack.
3. While the stack is not empty:
   - Pop a node.
   - Add its value to the result.
   - Push the left child.
   - Push the right child.
4. Reverse the result using `Collections.reverse()`.

 Java Solution

java
class Solution {
    public List<Integer> postorderTraversal(TreeNode root) {
        List<Integer> result = new ArrayList<>();

        if (root == null) {
            return result;
        }

        Stack<TreeNode> stack = new Stack<>();
        stack.push(root);

        while (!stack.isEmpty()) {
            TreeNode node = stack.pop();

            result.add(node.val);

            if (node.left != null) {
                stack.push(node.left);
            }

            if (node.right != null) {
                stack.push(node.right);
            }
        }

        Collections.reverse(result);

        return result;
    }
}


 Complexity Analysis

Let **n** be the number of nodes and **h** be the height of the tree.

  Complexity  Recursive  Iterative 
 ----------  ---------  --------- 
 Time        O(n)       O(n)      
 Space       O(h)       O(n)      

Time Complexity: O(n) — Every node is visited exactly once.
Space Complexity: O(h) — Recursive call stack.
Iterative Space Complexity: O(n) — Stack and result list require additional memory.

Key Concepts Learned

- Binary Trees
- Postorder Traversal
- Depth-First Search (DFS)
- Recursion
- Stack (LIFO)
- Collections.reverse()
- Time and Space Complexity

 Conclusion

Postorder Traversal visits nodes in the order:

Left → Right → Root

The recursive solution directly follows this order, while the iterative solution uses a Stack and reverses the result.

Both solutions achieve **O(n) time complexity.
