#### Baseball Game

- Time Complexity - O(n)
- Space Complexity - O(n)

```java
class Solution {
    public int calPoints(String[] operations) {
        Stack <Integer> st=new Stack <>();
        for(int i=0;i<operations.length;i++)
        {
            if(operations[i].equals("C"))
                st.pop();
            else if(operations[i].equals("D"))
               { 
                   int x=st.pop(); 
                   st.add(x);
                   st.add(x*2);
                }
            else if(operations[i].equals("+"))
                { 
                    int x=st.pop(); 
                    int y=st.pop();
                    st.add(y);
                    st.add(x);
                    st.add(x+y);
                }
            else
            {
                int no=Integer.parseInt(operations[i]);
                st.add(no);
            }
        }
        int sum=0;
        while(!st.isEmpty())
        {
            sum=sum+st.pop();
        }
        return sum;
    }
}
```
