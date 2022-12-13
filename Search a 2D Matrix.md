#### Search a 2D Matrix

**1. Using while loop (Sorted Array)**

- Time Complexity - O(row+col)

- Space Complexity - O(1) 
  ​

  ```java
  class Solution {
      public boolean searchMatrix(int[][] matrix, int target) {
          int row=matrix.length;
          int col=matrix[0].length;
          boolean res=false;
          for(int i=0;i<row;i++)
          {
              if(target>=matrix[i][0] && target<=matrix[i][col-1])
              {
                  for(int j=0;j<col;j++)
                  {
                      if(matrix[i][j]==target)
                          res=true;
                  }
              }
          }
          return res;
      }
  }
  ```

  ​