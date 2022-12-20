#### Replace Elements with Greatest elements on right side.

- Time Complexity - O(n^2)
- Space Complexity - O(1)

```java
class Solution {
    public int[] replaceElements(int[] arr) {
        for(int i=0;i<arr.length-1;i++)
        {
            int max=0;
            for(int j=i+1;j<arr.length;j++)
            {
                if(arr[j]>max)
                {
                    max=arr[j];
                }
            }
            arr[i]=max;
        }
        arr[arr.length-1]=-1;
        return arr;
    }
}
```

