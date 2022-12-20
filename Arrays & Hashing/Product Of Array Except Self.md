#### Product Of Array Except Self

- Time Complexity - O(n)
- Space Complexity - O(n)

```java
class Solution {
    public int[] productExceptSelf(int[] nums) {
        int A[]=new int[nums.length];
        int sum=1;
        for(int i=0;i<nums.length;i++)
        { 
            A[i]=sum;
            sum=sum*nums[i];
        }
        sum=1;
        for(int i=nums.length-1;i>=0;i--)
        {
            A[i]=A[i]*sum;
            sum=sum*nums[i];
        }
        return A;
    }
}
```

