#### Palindrome Number

- Time Complexity - O(n)               //n=no of digits in x
- Space Complexity - O(1)

```java
class Solution {
    public boolean isPalindrome(int x) {
        int rev=0,d,n;
        n=x;
        while(n>0)
        {
            d=n%10;
            rev=rev*10+d;
            n=n/10;
        }
        return (rev==x);
        
    }
}
```

