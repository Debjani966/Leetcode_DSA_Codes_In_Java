#### Find the Duplicate Number

- Time Complexity - O(n)
- Space Complexity - O(n)

```java
class Solution {
    public int findDuplicate(int[] nums) {
        HashSet hs=new HashSet();
        for(int i=0;i<nums.length;i++)
        {
            if(hs.contains(nums[i]))
                return nums[i];
            hs.add(nums[i]);
        }
        return -1;
    }
}
```

