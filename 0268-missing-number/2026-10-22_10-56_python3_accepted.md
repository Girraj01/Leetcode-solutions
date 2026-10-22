# 268. Missing Number
  
<br>**Problem:** https://leetcode.com/problems/missing-number/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Math, Binary Search, Bit Manipulation, Sorting<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-22 10:56 local time

**Runtime:** 3 ms (beats 60.5222%)
**Memory:** 20.4 MB (beats 41.97699999999999%)


<!-- leetgit:submissionId=2178532971 codeHash=f61b9cb08f49f295c6669cae3d023c55e76cbbf4e0a4e37a12e41c0719e320b7 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def missingNumber(self, nums: list[int]) -> int:
        a = 0
        n = len(nums)
        for i in range(n):
            a ^= nums[i]^i
        a ^= n
        return a
            
```
