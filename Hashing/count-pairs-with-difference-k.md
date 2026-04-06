# Count Ordered Index Pairs with Difference K


## Question
Count pairs `(i,j)` with `i<j` such that `arr[i] - arr[j] = k`.

Source:
- Class notes (Q4)

## Testcases
- Input:
  `arr=[5,1,2,4], k=1`
  Output:
  `1`
  Explanation:
  Only pair `(2,3)` gives `2-1` style based on order condition.

## Edge Cases
- `k=0`.
- Repeated elements.

## Constraint
- `1 <= n <= 10^5`

## Hint
- At current `x`, needed prior element is `x+k`.

## Solution
Maintain prior frequencies. For each `x`, answer += freq[`x+k`], then add `x`.

## Similar Questions
- LeetCode: https://leetcode.com/problems/k-diff-pairs-in-an-array/
- GFG: https://www.geeksforgeeks.org/count-pairs-difference-equal-k/
- Other: - To be added
