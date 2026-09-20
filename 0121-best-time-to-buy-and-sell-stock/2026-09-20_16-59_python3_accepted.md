# 121. Best Time to Buy and Sell Stock
  
<br>**Problem:** https://leetcode.com/problems/best-time-to-buy-and-sell-stock/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Dynamic Programming<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 16:59 local time

**Runtime:** 31 ms (beats 84.79750000000004%)
**Memory:** 28.6 MB (beats 42.76960000000005%)


<!-- leetgit:submissionId=2147624197 codeHash=bbcda5cda704349d505128605c5bb5235885e75bc6f22aaeb8b2262d8964ffc9 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def maxProfit(self, prices: list[int]) -> int:
        minval = float("inf")
        maxprofit = 0
        for i in prices:
            if i< minval:
                minval = i
            else:
                maxprofit = max(maxprofit, i-minval)
        return maxprofit
```
