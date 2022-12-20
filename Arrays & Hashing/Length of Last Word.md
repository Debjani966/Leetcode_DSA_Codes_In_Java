#### Length of Last Word

- Time Complexity - O(s)
- Space Complexity - O(1)

```java
class Solution {
    public int lengthOfLastWord(String s) {
        s=s.trim();
        int x=0;
        for(int i=s.length()-1;i>=0;i--)
        {
            if(s.charAt(i)==' ')
            {
                x=i+1;
                break;
            }
        }
        return s.length()-x;
    }
}
```

