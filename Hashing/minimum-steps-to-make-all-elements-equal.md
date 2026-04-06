# Minimum Steps to Make All Elements Equal


## Question
In one operation, replace a current largest element by current second-largest value. Find minimum operations to make all elements equal.

Source:
- Class notes (Q20)

## Testcases
- Input:
  `arr=[5,1,3]`
  Output:
  `3`
  Explanation:
  Final all values become smallest value.

## Edge Cases
- Already equal array.
- Large duplicates.

## Constraint
- `1 <= n <= 10^5`

## Hint
- Sort/map frequencies and simulate level-wise reductions.

## Solution
Count frequency by value, process values descending, accumulate operations by number of greater elements.

## Similar Questions
- LeetCode: https://leetcode.com/problems/reduction-operations-to-make-the-array-elements-equal/
- GFG: - To be added
- Other: - To be added
