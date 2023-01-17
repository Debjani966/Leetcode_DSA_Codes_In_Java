**Intersection of Two Linked Lists**

- Time Complexity- O(N+M)
- Space Complexity- O(1)

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public ListNode getIntersectionNode(ListNode headA, ListNode headB) {
        ListNode L1=headA;
        ListNode L2=headB;
        while(L1!=L2)
        {
            if(L1!=null)
                L1=L1.next;
            else
                L1=headB;
            if(L2!=null)
                L2=L2.next;
            else
                L2=headA;
        }
        return L1;
    }
}
```

