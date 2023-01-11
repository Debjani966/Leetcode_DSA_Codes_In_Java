**Plus One**

```java
import java.math.BigInteger;
class Solution {
    public int[] plusOne(int[] digits) {
       int len=digits.length-1;
        if(digits[len]==0 || digits[len]==1 || digits[len]==2 || digits[len]==3 || digits[len]==4 || digits[len]==5 || digits[len]==6 || digits[len]==7 || digits[len]==8)
        {
            digits[len]=digits[len]+1;
        }
        else if(digits[len]==9)
        {
            for(int i=len;i>=0;i--)
            {
                if(digits[i]!=9)
                {
                    digits[i]=digits[i]+1;
                    break;
                }
                else
                {
                    digits[i]=0;
                }
            }
        }
        if(digits[0]!=0)
        {
        return digits;
        }
        else
        {
            int A[]=new int[digits.length+1];
            A[0]=1;
            for(int i=1;i<A.length;i++)
            {
                A[i]=0;
            }
            return A;
        }
    }
}
```

