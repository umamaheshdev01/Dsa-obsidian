# Longest Consecutive Sequence


## Question
Given unsorted array, return length of longest consecutive elements sequence.

Source:
- https://leetcode.com/problems/longest-consecutive-sequence/

## Testcases
- Input:
  `nums=[100,4,200,1,3,2]`
  Output:
  `4`
  Explanation:
  Sequence `1,2,3,4`.

## Edge Cases
- Empty array.
- Duplicates.

## Constraint
- `0 <= nums.length <= 10^5`

## Hint
- Use hash set and start only at sequence heads.

## Solution
For each `x` with no `x-1`, count forward `x+1,x+2...`; track max length.

## Similar Questions
- LeetCode: https://leetcode.com/problems/longest-increasing-subsequence/
- GFG: https://www.geeksforgeeks.org/longest-consecutive-subsequence/
- Other: - To be added
