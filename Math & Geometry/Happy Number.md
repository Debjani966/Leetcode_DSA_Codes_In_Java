####Happy Number

**1. Using HashSet**

```java
class Solution {
    public boolean isHappy(int n) {
        int d,sum=0;
        HashSet hs =new HashSet();
        while(true)
        {
            sum=0;
            while(n>0)
            {
                d=n%10;
                sum=sum+(d*d);
                n=n/10;
            }
            if(sum==1 || hs.contains(sum))
            {
                break;
            }
            hs.add(sum);
            n=sum;
        }
        if(sum==1)
            return true;
        else
            return false;
    }
}
```

