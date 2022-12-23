#### Evaluate Reverse Polish Notation

- Time Complexity - O(n)
- Space Complexity - O(n)

```java
class Solution {
    public int evalRPN(String[] tokens) {
        Stack <Integer> st=new Stack<>();
        for(int i=0;i<tokens.length;i++)
        {
            if(tokens[i].equals("+"))
            {
                int x=st.pop();
                int y=st.pop();
                st.add(y+x);
            }
            else if(tokens[i].equals("-"))
            {
                int x=st.pop();
                int y=st.pop();
                st.add(y-x);
            }
            else if(tokens[i].equals("*"))
            {
                int x=st.pop();
                int y=st.pop();
                st.add(x*y);
            }
            else if(tokens[i].equals("/"))
            {
                int x=st.pop();
                int y=st.pop();
                st.add(y/x);
            }
            else
            {
                int no=Integer.parseInt(tokens[i]);
                st.add(no);
            }
        }
        return st.pop();
    }
}
```

