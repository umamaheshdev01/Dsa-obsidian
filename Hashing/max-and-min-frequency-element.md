# Find Any Element with Maximum and Minimum Frequency


## Question
Given an integer array, print any element with maximum frequency and any element with minimum frequency.

Source:
- Class notes (Q1)

## Testcases
- Input:
  `arr = [3,2,3,2,4,3]`
  Output:
  `max: (3,3), min: (4,1)`
  Explanation:
  Frequencies are `3->3`, `2->2`, `4->1`.

## Edge Cases
- Single element array.
- Multiple elements tied for max/min frequency.

## Constraint
- `1 <= n <= 10^5`

## Hint
- Use hashmap frequency counting.

## Solution
Build frequency map in `O(n)`, then scan map to track min and max frequency entries.

## Similar Questions
- LeetCode: - To be added
- GFG: https://www.geeksforgeeks.org/find-frequency-number-array/
- Other: - To be added
