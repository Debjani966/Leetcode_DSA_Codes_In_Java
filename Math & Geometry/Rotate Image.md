**Rotate Image**

Matrix nXn

- Time Complexity: O(n*n)
- Space Complexity: O(n*n)

```java
class Solution {
    public void rotate(int[][] matrix) {
        int x=matrix.length;
        int y=matrix[0].length;
        int[][] m=new int[x][y];
        for(int i=0;i<y;i++)
        {
            for(int j=0;j<x;j++)
            {
                m[i][j]=matrix[j][i];
            }
        }
        int a=0;
        for(int i=0;i<x;i++)
        {
            int b=0;
            for(int j=y-1;j>=0;j--)
            {
                matrix[a][b]=m[i][j];
                b++;
            }
            a++;
        }
    }
}
```

