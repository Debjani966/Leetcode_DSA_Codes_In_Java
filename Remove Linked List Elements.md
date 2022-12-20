#### Remove Linked List Elements

- Time Complexity - O(n)
- Space Complexity - O(1)

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode removeElements(ListNode head, int val) {
        ListNode h1=head;
        ListNode pre=head;
        if(head==null)
            return head;
        
        while(h1!=null)
        {
            if(h1.val==val)
                pre.next=h1.next;
            else
                pre=h1;
            h1=h1.next;
        }
        if(head.val==val)
            head=head.next;
        
        return head;
    }
}
```

