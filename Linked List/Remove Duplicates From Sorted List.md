#### Remove Duplicates From Sorted List

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
    public ListNode deleteDuplicates(ListNode head) {
        if(head==null || head.next==null)
        {
            return head;
        }
        ListNode head1=head.next;
        int x=head.val;
        ListNode pre=head;
        while(head1!=null)
        {
            if(x==head1.val)
            {
                pre.next=head1.next;
            }
            else
            {
                x=head1.val;
                pre=head1;
            }
            head1=head1.next;
        }
        return head;
    }
}
```

