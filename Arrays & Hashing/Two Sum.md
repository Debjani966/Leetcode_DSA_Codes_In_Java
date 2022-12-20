#### Two Sum

**1. Normal Loop Method**

- Time Complexity - O(n^2)
- Space Complexity - O(1)

```
class Solution {
	public int[] twoSum(int[] nums, int target) {
    	int A[]=new int[2];
    	for(int i=0;i<nums.length;i++)
    	{
        	for(int j=i+1;j<nums.length;j++)
        	{
            	if(nums[i]+nums[j]==target)
            	{
                	A[0]=i;
                	A[1]=j;
            	}
        	}
    	}
    	return A;
	}
}
```

**2. Using HashMap**

- Time Complexity - O(n)
- Space Complexity - O(n)

```
// key=nums[i], value=index

class Solution {
	public int[] twoSum(int[] nums, int target) {
    	int A[]=new int[2];
    	HashMap <Integer,Integer> map= new HashMap <>(); 
    	for(int i=0;i< nums.length;i++)
    	{
        	if(map.containsKey(target-nums[i]))
        	{
            	int x=map.get(target-nums[i]);
            	A[0]=x;
            	A[1]=i;
            	break;
        	}
        	else
        	{
            	map.put(nums[i],i);
        	}
    	}
    	return A;
	}
}
```