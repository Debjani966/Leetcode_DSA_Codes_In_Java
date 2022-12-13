#### 1) Contains Duplicate
**1.1 Sort the array.**

Time Complexity - O(nLogn)
Space Complexity - O(1)

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

Time Complexity - O(n)
Space Complexity - O(n)

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