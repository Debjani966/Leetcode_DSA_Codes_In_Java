#### Linked List Cycle

**1. Using HashSet to keep a record of all the visited Nodes.**

- Time Complexity - O(n)
- Space Complexity - O(n)

```java
/**
 * Definition for singly-linked list.
 * class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public boolean hasCycle(ListNode head) {
        if(head==null)
            return false;

        HashSet hs=new HashSet();
        ListNode ptr=head;
        int f=0;
        hs.add(ptr.next);
        ptr=ptr.next;
        while(ptr!=null)
        {
            if(hs.contains(ptr.next))
             {  
                f=1;
                break;
             }
            hs.add(ptr.next);
            ptr=ptr.next;
        }
        if(f==1)
            return true;
        else
            return false;
    }
}
```

**2. Using slow pointer (moves 1 step) and fast pointer (moves 2 step)**

- Time Complexity - O(n)
- Space Complexity - O(1)

```java
/**
 * Definition for singly-linked list.
 * class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public boolean hasCycle(ListNode head) {
        if(head==null)
            return false;
        ListNode fast=head;
        ListNode slow=head;
        while (fast!=null && fast.next!=null)
        {
            slow=slow.next;
            fast=fast.next.next;
            if(slow==fast)
            {
                return true;
            }
        }
        return false;
    }
}
```
