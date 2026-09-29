# 73. Set Matrix Zeroes
  
<br>**Problem:** https://leetcode.com/problems/set-matrix-zeroes/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Matrix<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-29 23:40 local time

**Runtime:** 9 ms (beats 26.987499999999997%)
**Memory:** 20.7 MB (beats 69.44720000000001%)


<!-- leetgit:submissionId=2157450894 codeHash=114c7af6c9ed3611e85bc8ab71bd3a65e9457d3b797c2e80236fa033e222b54f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def setZeroes(self, matrix: list[list[int]]) -> None:
        """
        Do not return anything, modify matrix in-place instead.
        """
        r,c = len(matrix),len(matrix[0])
        row,col = [0]*r , [0]*c
        for i in range(0,r):
            for j in range(0,c):
                if matrix[i][j] == 0:
                    row[i],col[j] = -1, -1
        
        for i in range(0,r):
            for j in range(0,c):
                if row[i] == -1 or col[j] == -1:
                    matrix[i][j] = 0
```
