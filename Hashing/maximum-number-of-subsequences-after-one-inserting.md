# Maximum Number of Subsequences After One Inserting


## Question
Given string, insert one character to maximize number of target subsequences (class variant with `LCT`; linked problem has its own target).

Source:
- https://leetcode.com/contest/weekly-contest-460/problems/maximum-number-of-subsequences-after-one-inserting/description/
- Class notes (Q26)

## Testcases
- Input:
  `s="LCLLC"` (class pre-steps)
  Output:
  `4` for count of `LC` before final insertion logic.
  Explanation:
  Build counts via prefix/suffix accumulations.

## Edge Cases
- All same character.
- Insert at boundaries gives best answer.

## Constraint
- As per source.

## Hint
- Compare three insertion families: insert first target char, middle char, or last target char.

## Solution
Precompute needed pair counts (`LC`, `CT`) and evaluate best insertion impact in O(n).

## Similar Questions
- LeetCode: https://leetcode.com/problems/maximum-number-of-subsequences-in-a-string/
- GFG: - To be added
- Other: - To be added
