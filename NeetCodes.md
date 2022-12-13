#### 1) Contains Duplicate
**1.1 Sort the array.**

- Time Complexity - O(nLogn)

- Space Complexity - O(1)

```java
class Solution {
public boolean containsDuplicate(int[] nums) {
    Arrays.sort(nums);
    for(int i=0;i<nums.length-1;i++)
    {
        if(nums[i]==nums[i+1])
        {
            return true;
        }
    }
    return false;
  }
}
```


**1.2 Using Hash Set.**

- Time Complexity - O(n)

- Space Complexity - O(n)

```java
class Solution {
public boolean containsDuplicate(int[] nums) {
    HashSet hs= new HashSet ();
    for(int i=0;i<nums.length;i++)
    {
        if(hs.contains(nums[i]))
        {
            return true;
        }
        hs.add(nums[i]);
    }
    return false;
  }
}
```

#### 2) Valid Anagram

**2.1 Convert the String into Character array, then sort the elements and compare the two character array.**

- Time Complexity - O(sLogs) OR O(tLogt)
- Space Complexity - O(s+t)

```java
class Solution {
    public boolean isAnagram(String s, String t) {
        char[] s1 = s.toCharArray();
        char[] s2 = t.toCharArray();
        Arrays.sort(s1);
        Arrays.sort(s2);
        int l1=s1.length;
        int l2=s2.length;
        if(l1==l2)
        {
            for(int i=0;i<l1;i++)
            {
                if(s1[i]!=s2[i])
                {
                    return false;
                }
            }
            return true;
        }
        return false;
    }
}
```

**2.2 Using HashMap**

- Time Complexity - O(s) OR O(t)
- Space Complexity - O(s+t)

```java
class Solution {
 	 public boolean isAnagram(String s, String t) {
        if(s.length()!=t.length())
        {
            return false;
        }
       HashMap <Character,Integer> map1= new HashMap <>();
       HashMap <Character,Integer> map2= new HashMap <>();
       for(int i=0;i<s.length();i++)
       {
           char ch=s.charAt(i);
           map1.put(ch, map1.getOrDefault(ch,0)+1);
       }
        for(int i=0;i<t.length();i++)
       {
           char ch=t.charAt(i);
           map2.put(ch, map2.getOrDefault(ch,0)+1);
       }
       if(map1.equals(map2))
       return true;
       else
       return false;
    }
}
```

#### 3) Two Sum
**3.1 Normal Loop Method**

- Time Complexity - O(n^2)
- Space Complexity - O(1)

```java
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
**3.2 Using HashMap**

- Time Complexity - O(n)
- Space Complexity - O(n)


```java
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

