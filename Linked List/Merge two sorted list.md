#### Merge two sorted list

- Time Complexity - O(list1+list2)
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
    public ListNode mergeTwoLists(ListNode list1, ListNode list2) {
        //ListNode root = new ListNode();
        ListNode head=new ListNode();
        ListNode hh=head;
        while(list1!=null && list2!=null)
        {
            if(list1.val<list2.val)
            {
                head.next=list1;
                list1=list1.next;
            }
            else
            {
                head.next=list2;
                list2=list2.next;
            }
            head=head.next;
        }
        if(list1==null)
        {
            head.next=list2;
        }
        else
        {
            head.next=list1;
        }
        return hh.next;
    }
}
```
