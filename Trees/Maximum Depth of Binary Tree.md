####Maximum Depth of Binary Tree

**Method 1: Recursive solution** using DFS approach

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
    int res=0;
    public int maxDepth(TreeNode root) {
        if(root==null)
            return 0;
        else
        {
            return (1+Math.max(maxDepth(root.right),maxDepth(root.left)));
        }
    }
}
```

