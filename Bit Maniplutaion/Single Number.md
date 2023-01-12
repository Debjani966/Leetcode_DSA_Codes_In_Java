**Single Number**

```java
class Solution {
    public int singleNumber(int[] nums) {
        HashSet hs= new HashSet ();
        for(int i=0;i<nums.length;i++)
        {
            if(hs.contains(nums[i]))
            {
                hs.remove(nums[i]);
            }
            else
            {
                hs.add(nums[i]);
            }
        }
        if(hs.size()<1)
        return 0;
        else
        {
            Integer element : hs;
            int x=element;
            return x;
        }
    }
}
```

