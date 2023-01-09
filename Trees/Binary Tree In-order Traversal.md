####Binary Tree In-order Traversal

**Method 1: Recursive solution**

- Time Complexity - O(n)
- Space Complexity - O(n) 

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
class Solution {
    List <Integer> res=new ArrayList();
    public List<Integer> inorderTraversal(TreeNode root) {
        inorder(root);
        return res;
    }
    public void inorder(TreeNode root)
    {
        if(root==null)
        {
            return;
        }
        else
        {
            inorder(root.left);
            res.add(root.val);
            inorder(root.right);
        }
    }
}
```

**Method 2: Iterative Solution**

- Time Complexity - O(n)
- Space Complexity - O(2n) 

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
class Solution {
    public List<Integer> inorderTraversal(TreeNode root) {
        List<Integer> res = new ArrayList<>();
        Stack<TreeNode> s = new Stack<>();
        TreeNode present=root;
        while(present!=null || !s.isEmpty())
        {
            while(present!=null)
            {
                s.push(present);
                present=present.left;
            }
            present=s.pop();
            res.add(present.val);
            present=present.right;

        }
        return res;
    }
}
```

