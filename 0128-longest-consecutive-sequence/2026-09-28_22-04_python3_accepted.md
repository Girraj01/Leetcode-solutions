# 128. Longest Consecutive Sequence
  
<br>**Problem:** https://leetcode.com/problems/longest-consecutive-sequence/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Hash Table, Union-Find<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 22:04 local time

**Runtime:** 53 ms (beats 40.77399999999995%)
**Memory:** 36.6 MB (beats 67.71689999999998%)


<!-- leetgit:submissionId=2156208992 codeHash=66d399e661d0222487312fa94f1a4790948cad719239af065b3a7cefa993b586 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def longestConsecutive(self, nums: list[int]) -> int:
        data = set()
        n = len(nums)
        largest = 0
        for i in nums:
            data.add(i)
        
        for num in data:
            if num-1 in data:
                continue
            else:
                count = 1
                x = num
                while x+1 in data:
                    count +=1
                    x +=1
            largest = max(largest, count)
        return largest
```
