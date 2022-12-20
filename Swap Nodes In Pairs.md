#### Swap Nodes In Pairs

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
    public ListNode swapPairs(ListNode head) {
        int x=1;
        ListNode h1=head;
        ListNode p=head;
        while(head!=null)
        {
            if(x%2==0)
            {
                int temp=p.val;
                p.val=head.val;
                head.val=temp;
            }
            x++;
            p=head;
            head=head.next;
        }
        return h1;
    }
}
```

