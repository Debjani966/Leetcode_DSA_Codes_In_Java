#### Reverse String

- Time Complexity - O(n)
- Space Complexity - O(n)

```java
class Solution {
    public void reverseString(char[] s) {
        char c[]=new char[s.length];
        int i=0;
        for(int j=s.length-1;j>=0;j--)
        {
            c[i]=s[j];
            i++;
        }
        for(i=0;i<s.length;i++)
        {
            s[i]=c[i];
        }
    }
}
```

