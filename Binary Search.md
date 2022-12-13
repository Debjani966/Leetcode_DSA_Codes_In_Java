####Binary Search

**1. Using while loop (Sorted Array)**

- Time Complexity - O(Log n)

- Space Complexity - O(1) 
  ​
  ```java
   class Solution {
      public int search(int[] nums, int target) {
          int low = 0;
          int high = nums.length-1;
          
          while(low<=high){
          int mid = (low+high)/2;
          if(target<nums[mid]){
              high = mid-1;       
          }
          else if(target>nums[mid]){
              low = mid+1; 
          }
          else if(target==nums[mid]){
              return mid;
              }
          }
          return -1;
      }
  }
  ```
  ​
