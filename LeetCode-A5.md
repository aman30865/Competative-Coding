## LeetCode-Interview Prep

### Single Number
Given a non-empty array of integers, every element appears twice except for one. Find that single one.

### Note:

Your algorithm should have a linear runtime complexity. Could you implement it without using extra memory?

### Example 1:

Input: [2,2,1]
Output: 1

### Answer

<pre>class Solution:
    def singleNumber(self, nums: List[int]) -> int:
        xor = 0
        for i in nums:
            xor ^= i
        return xor</pre>
