# Range Increment and Point Query Using Difference Array


## Question
Initially array is all zeros. For each query `[L,R]`, add 1 to that range. Then answer point queries.

Source:
- Class notes (Q27)
- https://www.desiqna.in/16114/visa-oa-sde-intern-ctc-30-lac-27th-nov

## Testcases
- Input:
  `n=8, updates=[(1,8),(5,8)], points=[4,6]`
  Output:
  `1,2`
  Explanation:
  Final array becomes `[1,1,1,1,2,2,2,2]`.

## Edge Cases
- `R=n` boundary.
- Multiple overlapping updates.

## Constraint
- Typical class bound: indices up to `100000`.

## Hint
- Difference updates + prefix restore.

## Solution
Do `diff[L]+=1`, `diff[R+1]-=1` when valid, then prefix sum to get final values.

## Similar Questions
- LeetCode: https://leetcode.com/problems/range-addition/
- GFG: https://www.geeksforgeeks.org/difference-array-range-update-query-o1/
- Other: - To be added
