# Longest Palindrome by Concatenating Two Letter Words


## Question
Given list of two-letter words, find longest palindrome length that can be formed.

Source:
- https://leetcode.com/problems/longest-palindrome-by-concatenating-two-letter-words/

## Testcases
- Input:
  `words=["lc","cl","gg"]`
  Output:
  `6`
  Explanation:
  `"lc"+"gg"+"cl"` gives length 6 palindrome.

## Edge Cases
- Only symmetric words (like `aa`, `bb`).
- No reversible pair.

## Constraint
- As per source.

## Hint
- Pair reverse words and reserve at most one center symmetric word.

## Solution
Count words via hashmap. Match `ab` with `ba`; handle `aa`-type separately.

## Similar Questions
- LeetCode: https://leetcode.com/problems/palindrome-permutation/
- GFG: - To be added
- Other: - To be added
