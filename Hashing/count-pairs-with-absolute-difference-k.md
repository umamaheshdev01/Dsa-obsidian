# Count Pairs with Absolute Difference K


## Question
Count pairs `(i,j)` with `i<j` such that `|arr[i]-arr[j]| = k`.

Source:
- Class notes (Q5)
- https://leetcode.com/problems/count-number-of-pairs-with-absolute-difference-k/

## Testcases
- Input:
  `arr=[1,2,2,1], k=1`
  Output:
  `4`
  Explanation:
  Valid pairs follow absolute difference condition.

## Edge Cases
- `k=0` (equal-number pairs).
- Duplicate-heavy arrays.

## Constraint
- `1 <= n <= 10^5`

## Hint
- For each `x`, add prior counts of `x-k` and `x+k`.

## Solution
Single pass with hashmap frequencies; add matching counts before incrementing current.

## Similar Questions
- LeetCode: https://leetcode.com/problems/count-number-of-pairs-with-absolute-difference-k/
- GFG: https://www.geeksforgeeks.org/count-pairs-difference-equal-k/
- Other: - To be added
