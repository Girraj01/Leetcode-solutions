# 283. Move Zeroes
  
<br>**Problem:** https://leetcode.com/problems/move-zeroes/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Two Pointers<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-24 18:37 local time

**Runtime:** 3 ms (beats 81.641%)
**Memory:** 20.4 MB (beats 62.893799999999985%)


<!-- leetgit:submissionId=2118444745 codeHash=843bd45e7992faa4f86c21cdc889b0af81ffe543cee5f6962aee59726706de75 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def moveZeroes(self, nums: List[int]) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        if len(nums) == 1:
            return
        i = 0
        n = len(nums)
        for i in range(n):
            if nums[i] == 0:
                break
        j = i+1
        while j < n:
            if nums[j] != 0:
                nums[i],nums[j] = nums[j],nums[i]
                i +=1
            j+=1
        
```
