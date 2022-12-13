####Valid Palindrome

**1. Remove special Characters then reverse and compare.**

- Time Complexity - O(n)
- Space Complexity - O(n) 

```java
class Solution {
    public boolean isPalindrome(String s) {
        s=s.toLowerCase();
        s=s.replaceAll("[^a-zA-Z0-9]", "");
        String rev="";
        for (int i=0; i<s.length(); i++)
         {
             char ch= s.charAt(i);
             rev= ch+rev;
         }
         if(s.equalsIgnoreCase(rev))
            return true;
         else
            return false;
    }
}
```

