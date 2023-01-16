**Min Stack**

```java
class MinStack {
    Stack <Integer> st;
    Stack <Integer> minimum;
    public MinStack() {
        st=new Stack<>();
        minimum=new Stack<>();
    }
    
    public void push(int val) {
        st.push(val);
        if(minimum.isEmpty())
            minimum.push(val);
        else
        {
            int x=minimum.pop();
            if(x<=val)
            {
                minimum.push(val);
                minimum.push(x);
            }
            else
            {
                minimum.push(x);
                minimum.push(val);
            }
        }
    }
    
    public void pop() {
        int x=st.pop();
        Stack <Integer> demo=new Stack<>();
        while(x!=minimum.peek())
        {
            int y=minimum.pop();
            demo.push(y);
        }
        minimum.pop();
        while(!demo.isEmpty())
        {
            minimum.push(demo.pop());
        }
    }
    
    public int top() {
        return st.peek();
    }
    
    public int getMin() {
       return minimum.peek();
    }
}

/**
 * Your MinStack object will be instantiated and called as such:
 * MinStack obj = new MinStack();
 * obj.push(val);
 * obj.pop();
 * int param_3 = obj.top();
 * int param_4 = obj.getMin();
 */
```

