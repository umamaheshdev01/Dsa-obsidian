# Largest Subarray with 0 Sum


## Question
Find maximum length of subarray having sum `0`.

Source:
- https://www.geeksforgeeks.org/find-the-largest-subarray-with-0-sum/

## Testcases
- Input:
  `arr=[15,-2,2,-8,1,7,10,23]`
  Output:
  `5`
  Explanation:
  `[-2,2,-8,1,7]` sum is zero.

## Edge Cases
- Entire array sums to zero.
- No zero-sum subarray.

## Constraint
- As per source.

## Hint
- Equal prefix sums imply zero-sum between indices.

## Solution
Store first index of each prefix sum; maximize current index minus first index.

## Similar Questions
- LeetCode: https://leetcode.com/problems/contiguous-array/
- GFG: https://www.geeksforgeeks.org/find-the-largest-subarray-with-0-sum/
- Other: - To be added
