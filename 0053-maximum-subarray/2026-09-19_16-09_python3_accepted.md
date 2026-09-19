# 53. Maximum Subarray
  
<br>**Problem:** https://leetcode.com/problems/maximum-subarray/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Divide and Conquer, Dynamic Programming<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-19 16:09 local time

**Runtime:** 40 ms (beats 40.39519999999997%)
**Memory:** 31.6 MB (beats 21.11599999999999%)


<!-- leetgit:submissionId=2146559629 codeHash=c1d64ec8170d3aea9f910f23c7145585ae324cae3fe20e5fedf597ef18950e77 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def maxSubArray(self, nums: list[int]) -> int:
        if not nums:
            return 0
        
        bestending = nums[0]
        answer = nums[0]
        for i in range(1,len(nums)):
            bestending = max(nums[i], nums[i]+bestending)
            answer = max(answer,bestending)
        
        return answer
```
