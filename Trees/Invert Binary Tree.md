####Invert Binary Tree

- Time Complexity - O(n)
- Space Complexity - O(1) 

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
    public TreeNode invertTree(TreeNode root) {
        if(root==null)
        {
            return  null;
        }
        else
        {
            swap(root);
            invertTree(root.left);
            invertTree(root.right);
        }
        return root;
    }
    public TreeNode swap(TreeNode root)
    {
        TreeNode temp=root.left;
        root.left=root.right;
        root.right=temp;
        return root;
    }
}
```

