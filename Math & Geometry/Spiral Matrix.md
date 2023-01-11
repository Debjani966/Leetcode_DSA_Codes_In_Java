**Spiral Matrix**

```java
class Solution {
    public List<Integer> spiralOrder(int[][] matrix) {
        List<Integer> map=new ArrayList<Integer>();
        int row=matrix.length;
        int col=matrix[0].length;
        
        int top=0,left=0,right=col-1,bottom=row-1;
        int dir=1;
        while(top<=bottom && left<=right)
        {
            if(dir==1)
            {
                for(int i=left;i<=right;i++)
                {
                    map.add(matrix[top][i]);
                }
                dir=2;
                top++;
            }
            else if(dir==2)
            {
                for(int i=top;i<=bottom;i++)
                {
                    map.add(matrix[i][right]);
                }
                dir=3;
                right--;
            }
            else if(dir==3)
            {
                for(int i=right;i>=left;i--)
                {
                    map.add(matrix[bottom][i]);
                }
                bottom--;
                dir=4;
            }
            else
            {
                for(int i=bottom;i>=top;i--)
                {
                    map.add(matrix[i][left]);
                }
                left++;
                dir=1;
            }
        }
        return map;
    }
}
```

