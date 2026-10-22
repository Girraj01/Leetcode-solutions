# 136. Single Number
  
<br>**Problem:** https://leetcode.com/problems/single-number/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Bit Manipulation<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-22 10:40 local time

**Runtime:** 1 ms (beats 71.3596%)
**Memory:** 21.2 MB (beats 48.247%)


<!-- leetgit:submissionId=2178521723 codeHash=c5fd0a1a1c53faecae0f69320146888217f62423fb8ae7bb6b63b0366ce06fa8 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def singleNumber(self, nums: list[int]) -> int:
        a = 0
        for i in nums:
            a ^= i

        return a
```
