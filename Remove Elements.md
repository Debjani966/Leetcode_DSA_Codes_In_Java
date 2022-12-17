#### Remove Elements

- Time Complexity - O(n)
- Space Complexity - O(1)

```java
class Solution {
    public int removeElement(int[] nums, int val) {
        int c=0;
        int l=nums.length;
        for(int i=0;i<l;i++)
        {
            if(nums[i]==val)
            {
                nums[i]=nums[l-1];
                c++;
                i--;
                l--;
            }
        }    
        return nums.length-c;
    }
}
```

