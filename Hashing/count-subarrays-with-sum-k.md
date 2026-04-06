# Count Subarrays with Sum K


## Question
Count subarrays whose sum equals `k`.

Source:
- Class notes (Q7)
- https://www.geeksforgeeks.org/number-subarrays-sum-exactly-equal-k/

## Testcases
- Input:
  `arr=[1,1,1], k=2`
  Output:
  `2`
  Explanation:
  Subarrays: `[1,1]` at indices `(0,1)` and `(1,2)`.

## Edge Cases
- Negative numbers present.
- `k=0`.

## Constraint
- `1 <= n <= 2*10^5`

## Hint
- Use prefix sum frequency map.

## Solution
For running prefix `s`, add `freq[s-k]` to answer, then increment `freq[s]`.

## Similar Questions
- LeetCode: https://leetcode.com/problems/subarray-sum-equals-k/
- GFG: https://www.geeksforgeeks.org/number-subarrays-sum-exactly-equal-k/
- Other: - To be added
