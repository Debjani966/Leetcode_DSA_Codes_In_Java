#### Valid Anagram

**1. Convert the String into Character array, then sort the elements and compare the two character array.**

- Time Complexity - O(sLogs) OR O(tLogt)
- Space Complexity - O(s+t)

```java
class Solution {
    public boolean isAnagram(String s, String t) {
        char[] s1 = s.toCharArray();
        char[] s2 = t.toCharArray();
        Arrays.sort(s1);
        Arrays.sort(s2);
        int l1=s1.length;
        int l2=s2.length;
        if(l1==l2)
        {
            for(int i=0;i<l1;i++)
            {
                if(s1[i]!=s2[i])
                {
                    return false;
                }
            }
            return true;
        }
        return false;
    }
}
```

**2. Using HashMap**

- Time Complexity - O(s) OR O(t)
- Space Complexity - O(s+t)

```java
class Solution {
 	 public boolean isAnagram(String s, String t) {
        if(s.length()!=t.length())
        {
            return false;
        }
       HashMap <Character,Integer> map1= new HashMap <>();
       HashMap <Character,Integer> map2= new HashMap <>();
       for(int i=0;i<s.length();i++)
       {
           char ch=s.charAt(i);
           map1.put(ch, map1.getOrDefault(ch,0)+1);
       }
        for(int i=0;i<t.length();i++)
       {
           char ch=t.charAt(i);
           map2.put(ch, map2.getOrDefault(ch,0)+1);
       }
       if(map1.equals(map2))
       return true;
       else
       return false;
    }
}
```

