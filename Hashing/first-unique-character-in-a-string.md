# First Unique Character in a String


## Question
Return index of first non-repeating character in a string, else `-1`.

Source:
- https://leetcode.com/problems/first-unique-character-in-a-string/

## Testcases
- Input:
  `s="leetcode"`
  Output:
  `0`
  Explanation:
  `l` appears once and first.

## Edge Cases
- No unique character.
- All characters unique.

## Constraint
- `1 <= s.length <= 10^5`

## Hint
- Count frequencies first, then scan for first count=1.

## Solution
Two passes using fixed array/hashmap frequency.

## Similar Questions
- LeetCode: https://leetcode.com/problems/ransom-note/
- GFG: https://www.geeksforgeeks.org/given-a-string-find-its-first-non-repeating-character/
- Other: - To be added
