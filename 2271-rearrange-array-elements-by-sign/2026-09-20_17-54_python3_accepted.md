# 2271. Rearrange Array Elements by Sign
  
<br>**Problem:** https://leetcode.com/problems/rearrange-array-elements-by-sign/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Simulation<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 17:54 local time

**Runtime:** 33 ms (beats 93.89410000000002%)
**Memory:** 43 MB (beats 65.22189999999999%)


<!-- leetgit:submissionId=2147664554 codeHash=cc1fb6b4b12836f702b2efaf50d91807fa2c6b7b62681bc410507656afd4b920 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def rearrangeArray(self, nums: list[int]) -> list[int]:
        n =len(nums)
        result = [0] *n

        pos,neg = 0,1
        for i in nums:
            if i < 0:
                result[neg] = i
                neg += 2
            else:
                result[pos] = i
                pos += 2
        return result
```
