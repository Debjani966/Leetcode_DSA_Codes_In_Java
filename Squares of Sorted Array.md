#### Squares of Sorted Array

- Time Complexity - O(n)
- Space Complexity - O(1)

```java
class Solution {
    public int[] sortedSquares(int[] nums) {
        for(int i=0;i<nums.length;i++)
        {
            nums[i]=nums[i]*nums[i];
        }
        Arrays.sort(nums);
        return nums;
    }
}
```

