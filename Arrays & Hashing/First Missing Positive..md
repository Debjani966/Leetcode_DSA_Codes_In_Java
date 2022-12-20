#### First Missing Positive.

- Time Complexity - O(n)
- Space Complexity - O(1)

```java
class Solution {
    public int firstMissingPositive(int[] nums) {
        Arrays.sort(nums);
        HashSet hs=new HashSet();
        int c=0;
        for(int i=0;i<nums.length;i++)
        {
            if(nums[i]>0)
            {
                c++;
                hs.add(nums[i]);
            }
        }
        for(int i=1;i<=c;i++)
        {
            if(!hs.contains(i))
            {
                return i;
            }
        }
        return c+1;
    }
}
```

