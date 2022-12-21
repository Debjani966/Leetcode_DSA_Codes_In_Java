#### Valid Parentheses

- Time Complexity - O(n)
- Space Complexity - O(n)

```java
class Solution {
    public boolean isValid(String s) {
        if(s.length()%2!=0)
            return false;
        Stack <Character> st=new Stack<>();
        for(int i=0;i<s.length();i++)
        {
            if(st.isEmpty() && (s.charAt(i)==')' || s.charAt(i)==']' || s.charAt(i)=='}'))
                return false;
            else if(s.charAt(i)==')' && st.peek()=='(')
                st.pop();
            else if(s.charAt(i)==']' && st.peek()=='[')
                st.pop();
            else if(s.charAt(i)=='}' && st.peek()=='{')
                st.pop();
            else
                st.add(s.charAt(i));
        }
        if(st.isEmpty())
            return true;
        else
            return false;
    }
}
```

