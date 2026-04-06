# Count of Longest Subarrays with Sum K


## Question
Find how many subarrays of maximum possible length have sum exactly `k`.

Source:
- Class notes (Q31)

## Testcases
- Input:
  `arr=[10,5,2,7,1,9,8,7], k=15`
  Output:
  `1`
  Explanation:
  Longest valid subarray is `[5,2,7,1]` of length 4.

## Edge Cases
- No valid subarray.
- Multiple longest subarrays.

## Constraint
- `1 <= n <= 2*10^5`

## Hint
- First determine maximum valid length, then count subarrays with that length and sum `k`.

## Solution
Prefix-sum hashing for length discovery + counting pass for max length occurrences.

## Similar Questions
- LeetCode: https://leetcode.com/problems/maximum-size-subarray-sum-equals-k/
- GFG: - To be added
- Other: - To be added
