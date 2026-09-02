# 1. Two Sum
  
<br>**Problem:** https://leetcode.com/problems/two-sum/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-03 00:38 local time

**Runtime:** 3 ms (beats 53.604600000000005%)
**Memory:** 20.4 MB (beats 41.47319999999998%)


<!-- leetgit:submissionId=2128890721 codeHash=a5011a3e2e11e31308cc37e97f8bd7176a730152ae20bae847e38f791031bce9 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        need = {}
        for i in range(len(nums)):
            remaining = target - nums[i]

            if remaining in need:
                return [need[remaining], i]

            need[nums[i]] = i
```
