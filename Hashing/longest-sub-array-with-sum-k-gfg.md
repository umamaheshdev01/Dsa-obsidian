# Longest Subarray with Sum K


## Question
Find maximum length subarray with sum equal to `k`.

Source:
- https://practice.geeksforgeeks.org/problems/longest-sub-array-with-sum-k0809/1

## Testcases
- Input:
  `arr=[10,5,2,7,1,9], k=15`
  Output:
  `4`
  Explanation:
  `[5,2,7,1]` length is 4.

## Edge Cases
- No valid subarray.
- Negative values present.

## Constraint
- As per source.

## Hint
- First occurrence of each prefix sum is important.

## Solution
Keep earliest index for each prefix sum; if `prefix-k` seen, update max length.

## Similar Questions
- LeetCode: https://leetcode.com/problems/maximum-size-subarray-sum-equals-k/
- GFG: https://www.geeksforgeeks.org/longest-sub-array-sum-k/
- Other: - To be added
