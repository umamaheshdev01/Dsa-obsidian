# Valid Anagram


## Question
Given two strings `s` and `t`, return true if `t` is an anagram of `s`, otherwise false.

Source:
- https://leetcode.com/problems/valid-anagram/

## Testcases
- Input:
  `s="anagram", t="nagaram"`
  Output:
  `true`
  Explanation:
  Same character multiset.

- Input:
  `s="rat", t="car"`
  Output:
  `false`
  Explanation:
  Character frequencies differ.

## Edge Cases
- Different lengths.
- Unicode handling (if asked by platform variant).

## Constraint
- `1 <= s.length, t.length <= 5*10^4`
- `s` and `t` consist of lowercase English letters (base version).

## Hint
- Compare frequency counts of characters.

## Solution
Either sort both strings and compare, or use fixed array/hashmap frequency counting in linear time.

## Similar Questions
- LeetCode: https://leetcode.com/problems/group-anagrams/
- GFG: https://www.geeksforgeeks.org/check-whether-two-strings-are-anagram-of-each-other/
- Other: - To be added
