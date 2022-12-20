#### Remove Nth Node from end of the list.

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
    public ListNode removeNthFromEnd(ListNode head, int n) {
        ListNode head1=head;
        ListNode head2=head;
        int c=0;
        while(head!=null)
        {
            c++;
            head=head.next;
        }
        int b=c-n;
        int x=0;
        ListNode prev=head;
        if(b==0)
        {
            head1=head1.next;
            return head1;
        }
        else
        {
        while (head1!=null)
        {
            if(x==b)
            {
                prev.next=head1.next;
                break;
            }
            x++;
            prev=head1;
            head1=head1.next;
        }
        }
        return head2;
    }
}
```

