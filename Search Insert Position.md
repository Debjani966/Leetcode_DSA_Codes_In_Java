#### Search Insert Position

- Time Complexity - O(n)
- Space Complexity - O(1)

```java
class Solution {
    public int searchInsert(int[] nums, int target) {
        int index=-1;
        for(int i=0;i<nums.length;i++)
        {
            if(target==nums[i])
            {
                index=i;
                break;
            }
            else if(nums[i]>target)
            {
                index=i;
                break;
            }
        }
        if(index==-1)
            return nums.length;
        else
            return index;
    }
}
```

