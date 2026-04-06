# Maximum Pair Sum with Equal Digit Sum


## Question
Pick two numbers with same digit sum and maximize their pair sum.

Source:
- Class notes (Q21)
- https://www.desiqna.in/13267/microsoft-coding-oa-sde-1-may-3-2023

## Testcases
- Input:
  `arr=[51,71,17,42]`
  Output:
  `93`
  Explanation:
  Best valid pair is `51+42` (digit sum 6).

## Edge Cases
- No valid pair exists.
- Many values sharing same digit sum.

## Constraint
- `1 <= n <= 10^5`

## Hint
- Maintain max value seen per digit sum.

## Solution
For each number, compute digit sum `d`, if map has `d`, update answer with current + map[d], then update map[d]=max(map[d], current).

## Similar Questions
- LeetCode: https://leetcode.com/problems/max-sum-of-a-pair-with-equal-sum-of-digits/
- GFG: - To be added
- Other: - To be added
