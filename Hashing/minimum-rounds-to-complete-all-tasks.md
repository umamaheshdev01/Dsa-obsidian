# Minimum Rounds to Complete All Tasks


## Question
You can remove tasks in groups of 2 or 3 of same difficulty. Find minimum operations to remove all tasks, else `-1`.

Source:
- Class notes (Q23)
- https://www.desiqna.in/16820/amazon-oa-sde-ctc-45lpa-coding-questions-2024-set-141

## Testcases
- Input:
  `tasks=[1,1,1,2,2,2,2]`
  Output:
  `3`
  Explanation:
  `1`s in 1 round of 3, `2`s in 2 rounds of 2.

## Edge Cases
- Any frequency equals 1 => impossible.
- Large frequencies.

## Constraint
- `1 <= n <= 10^5`

## Hint
- For frequency `f`, rounds are `ceil(f/3)` except `f=1` invalid.

## Solution
Count frequencies. If any `f==1` return `-1`. Else add `(f+2)/3` rounds for each value.

## Similar Questions
- LeetCode: https://leetcode.com/problems/minimum-rounds-to-complete-all-tasks/
- GFG: - To be added
- Other: - To be added
