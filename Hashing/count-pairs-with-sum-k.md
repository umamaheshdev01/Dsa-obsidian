# Count Pairs with Sum K


## Question
Count pairs `(i,j)` with `i<j` such that `arr[i] + arr[j] = k`.

Source:
- Class notes (Q3)

## Testcases
- Input:
  `arr=[1,5,7,-1,5], k=6`
  Output:
  `3`
  Explanation:
  Pairs are `(1,5)` with indices `(0,1)`, `(0,4)`, `(2,3)`.

## Edge Cases
- Negative numbers.
- Duplicate values.

## Constraint
- `1 <= n <= 10^5`

## Hint
- For each value `x`, look for prior frequency of `k-x`.

## Solution
Use hashmap `freq`. At each `x`, add `freq[k-x]` to answer, then do `freq[x]++`.

## Similar Questions
- LeetCode: https://leetcode.com/problems/max-number-of-k-sum-pairs/
- GFG: https://www.geeksforgeeks.org/count-pairs-with-given-sum/
- Other: - To be added
