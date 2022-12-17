#### Reverse Linked List

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
    public ListNode reverseList(ListNode head) {
       if(head==null || head.next==null)
       {
           return head;
       }
        ListNode pre=head;
        head=head.next;
        ListNode newL=pre;
        newL.next=null;
        while(head!=null)
        {
            pre=head;
            head=head.next;
            pre.next=newL;
            newL=pre;
        }
        return newL;
    }
}
```

