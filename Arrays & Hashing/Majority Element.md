####Majority Element

- Time Complexity: O(n)
- Space Complexity: O(n)

```java
class Solution {
    public int majorityElement(int[] nums)
    {
    int ans = -1;
    HashMap<Integer,Integer> freq = new HashMap<Integer,Integer>();
    int n=nums.length;                                
    for (int i=0;i<n;i++)
    {
        if(freq.containsKey(nums[i]))
        {
            freq.put(nums[i], freq.get(nums[i]) + 1);
        }
        else
        {
            freq.put(nums[i], 1);
        }
        if (freq.get(nums[i]) > n/2)
        {
            ans = nums[i];
        }
    }
    return ans;
    }
}
```

