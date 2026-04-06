# Two Non-Overlapping Maximum Sum Subarrays


## Question
Find maximum sum of two non-overlapping subarrays (empty allowed in class variant).

Source:
- Class notes (Q19)

## Testcases
- Input:
  `arr=[1,3,-1,2,-1,2]`
  Output:
  `7`
  Explanation:
  Choose best left and best right non-overlapping parts.

## Edge Cases
- All negatives (if empty allowed, answer may be 0).
- Small arrays.

## Constraint
- `1 <= n <= 2*10^5`

## Hint
- Precompute best subarray ending on left and starting on right.

## Solution
Compute `leftBest[i]` and `rightBest[i]`, maximize `leftBest[i]+rightBest[i+1]`.

## Similar Questions
- LeetCode: https://leetcode.com/problems/maximum-sum-of-two-non-overlapping-subarrays/
- GFG: - To be added
- Other: - To be added
