# Find Common Characters


## Question
Given list of strings, return all characters common to all strings including duplicates.

Source:
- https://leetcode.com/problems/find-common-characters/

## Testcases
- Input:
  `words=["bella","label","roller"]`
  Output:
  `["e","l","l"]`
  Explanation:
  Minimum frequency across words gives result.

## Edge Cases
- Single word input.
- No common character.

## Constraint
- As per source.

## Hint
- Intersect 26-char frequency arrays.

## Solution
Compute min frequency of each letter across words; emit letter that many times.

## Similar Questions
- LeetCode: https://leetcode.com/problems/intersection-of-two-arrays-ii/
- GFG: - To be added
- Other: - To be added
