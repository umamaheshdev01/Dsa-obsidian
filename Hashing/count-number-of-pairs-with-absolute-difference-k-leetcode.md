# Count Number of Pairs With Absolute Difference K


## Question
Given array and integer `k`, return count of pairs `(i,j)` where `i<j` and `|nums[i]-nums[j]|=k`.

Source:
- https://leetcode.com/problems/count-number-of-pairs-with-absolute-difference-k/

## Testcases
- Input:
  `nums=[1,2,2,1], k=1`
  Output:
  `4`
  Explanation:
  Four valid pairs.

## Edge Cases
- `k=0`.
- All equal values.

## Constraint
- As per source.

## Hint
- Add frequencies of `x-k` and `x+k` while scanning.

## Solution
One-pass hashmap frequency counting.

## Similar Questions
- LeetCode: https://leetcode.com/problems/k-diff-pairs-in-an-array/
- GFG: https://www.geeksforgeeks.org/count-pairs-difference-equal-k/
- Other: - To be added
