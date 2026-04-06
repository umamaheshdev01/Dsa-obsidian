# Count Unordered Pairs where |a[i]-a[j]| + |a[i]+a[j]| = Target


## Question
Given array and target, count unordered pairs `(i,j)` satisfying `|a[i]-a[j]| + |a[i]+a[j]| = target`.

Source:
- Class notes (Q34)
- https://www.desiqna.in/17097/de-shaw-oa-sde-coding-questions-2024-set-69

## Testcases
- Input:
  `arr=[1,2,3], target=4`
  Output:
  `To be computed`
  Explanation:
  Evaluate expression for unordered pairs only.

## Edge Cases
- Negative and positive mixed values.
- `target` odd/even behavior.

## Constraint
- As per source.

## Hint
- Analyze sign cases to simplify absolute expression.

## Solution
Case-split by sign and relative magnitude; use counting instead of brute-force pair generation.

## Similar Questions
- LeetCode: - To be added
- GFG: - To be added
- Other: https://www.desiqna.in/17097/de-shaw-oa-sde-coding-questions-2024-set-69
