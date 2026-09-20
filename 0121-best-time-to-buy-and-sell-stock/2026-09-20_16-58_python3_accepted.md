# 121. Best Time to Buy and Sell Stock
  
<br>**Problem:** https://leetcode.com/problems/best-time-to-buy-and-sell-stock/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Dynamic Programming<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-20 16:58 local time

**Runtime:** 49 ms (beats 54.728200000000065%)
**Memory:** 28.6 MB (beats 42.76960000000005%)


<!-- leetgit:submissionId=2147623902 codeHash=507ea2a98fcc30ba85592f3c4ca939d04b21dc60ecfbe9d43ef6c1232221216f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def maxProfit(self, prices: list[int]) -> int:
        minval = float("inf")
        maxprofit = 0
        for i in prices:
            minval = min(minval, i)
            maxprofit = max(maxprofit, i-minval)
        return maxprofit
```
