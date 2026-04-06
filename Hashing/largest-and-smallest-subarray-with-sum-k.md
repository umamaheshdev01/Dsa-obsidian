# Largest and Smallest Subarray with Sum K


## Question
Find smallest-length and largest-length subarrays whose sum equals `k`.

Source:
- Class notes (Q8)
- https://practice.geeksforgeeks.org/problems/longest-sub-array-with-sum-k0809/1

## Testcases
- Input:
  `arr=[10,5,2,7,1,9], k=15`
  Output:
  `smallest=2, largest=4`
  Explanation:
  `[10,5]` has length 2, `[5,2,7,1]` has length 4.

## Edge Cases
- No valid subarray.
- Multiple subarrays with same best length.

## Constraint
- `1 <= n <= 10^5`

## Hint
- Prefix sum map helps find candidate start quickly.

## Solution
Track earliest and latest occurrences of prefix sums to derive both min and max lengths.

## Similar Questions
- LeetCode: https://leetcode.com/problems/maximum-size-subarray-sum-equals-k/
- GFG: https://www.geeksforgeeks.org/longest-sub-array-sum-k/
- Other: - To be added
