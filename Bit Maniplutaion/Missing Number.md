#### Missing Number

**1. Sort the array.**

- Time Complexity - O(n)
- Space Complexity - O(1)

```java
class Solution {
    public int missingNumber(int[] nums) {
        Arrays.sort(nums);
        int x=nums[0];
        int f=0;
        for(int i=0;i<nums.length;i++)
        {
            if(x!=nums[i])
            {
                f=1;
                break;
            }
            x++;
        }
        if(f==0)
        {
            if(nums[0]-1>=0)
            {
                return nums[0]-1;
            }
            else
            {
                return nums[nums.length-1]+1;
            }
        }
        return x;
    }
}
```

