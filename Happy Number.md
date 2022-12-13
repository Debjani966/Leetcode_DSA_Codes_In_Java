####Happy Number

**1. Using While Loop**

```java
class Solution {
    public boolean isHappy(int n) {
        int d,sum=0;
        while(n>0 || sum>9)
        {
            if(n==0)
            {
                n=sum;
                sum=0;
            }
            d=n%10;
            sum=sum+(d*d);
            n=n/10;
        }
        if(sum==1 ||sum==7)
            return true;
        else
            return false;
    }
}
```

