# HashMap Recap: Key-Value Frequency Storage


## Question
Concept recap: hashmap stores key-value pairs and is commonly used for frequency counting.

Source:
- Class notes (Q13)

## Testcases
- Input:
  `arr=[5,5,8,8,1,1,1]`
  Output:
  `{5:2,8:2,1:3}`
  Explanation:
  Frequencies map each element to its occurrence count.

## Edge Cases
- Empty array.
- All values unique.

## Constraint
- `0 <= n <= 10^5`

## Hint
- Initialize missing keys with 0 before incrementing.

## Solution
Iterate array once, increment `freq[x]` for each value.

## Similar Questions
- LeetCode: https://leetcode.com/problems/top-k-frequent-elements/
- GFG: https://www.geeksforgeeks.org/find-frequency-number-array/
- Other: - To be added
