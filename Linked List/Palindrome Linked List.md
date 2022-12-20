#### Palindrome Linked List

- Time Complexity - O(n)
- Space Complexity - O(n)

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
    public boolean isPalindrome(ListNode head) {
        ArrayList <Integer> no= new ArrayList<>();
        ListNode ptr=head;
        while(ptr!=null)
        {
            no.add(ptr.val);
            ptr=ptr.next;
        }
        System.out.println(no);
        int x=no.size()/2;
        for(int i=0,j=no.size()-1;i<x;i++,j--)
        {
            if(no.get(i)!=no.get(j))
            return false;
        }
        return true;
    }
}
```

