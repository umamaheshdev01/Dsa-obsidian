# Find the Prefix Common Array of Two Arrays


## Question
Given two arrays `A` and `B` (permutation-like constraints), return prefix-common count array.

Source:
- https://leetcode.com/contest/biweekly-contest-103/problems/find-the-prefix-common-array-of-two-arrays/

## Testcases
- Input:
  `A=[1,3,2,4], B=[3,1,2,4]`
  Output:
  `[0,2,3,4]`
  Explanation:
  Count common elements in prefixes `[0..i]`.

## Edge Cases
- `n=1`.
- Matching arrays.

## Constraint
- As per source.

## Hint
- Track seen elements from both arrays and update common count.

## Solution
Maintain frequency/visited markers for elements from A and B per index.

## Similar Questions
- LeetCode: - To be added
- GFG: - To be added
- Other: - To be added
