#### Set Matrix Zeroes

**1. Sort the array.**

- Time Complexity - O(row*col)
- Space Complexity - O(row*col)

```java
class Solution {
    public void setZeroes(int[][] matrix) {
        int row=matrix.length;
        int col=matrix[0].length;
        int A[][]=new int[row][col];
        for(int i=0;i<row;i++)
        {
            for(int j=0;j<col;j++)
            {
                A[i][j]=matrix[i][j];
            }
        }
        for(int i=0;i<row;i++)
        {
            for(int j=0;j<col;j++)
            {
                if(matrix[i][j]==0)
                {
                    for(int k=0;k<col;k++)
                    {
                        A[i][k]=0;
                    }
                    for(int k=0;k<row;k++)
                    {
                        A[k][j]=0;
                    }
                }
            }
        }
        for(int i=0;i<row;i++)
        {
            for(int j=0;j<col;j++)
            {
                matrix[i][j]=A[i][j];
            }
        }
    }
}
```

