# Two Sum


## Question
Given an array and target, return indices of two numbers such that they add up to target.

Source:
- https://leetcode.com/problems/two-sum/

## Testcases
- Input:
  `nums=[2,7,11,15], target=9`
  Output:
  `[0,1]`
  Explanation:
  `2+7=9`.

## Edge Cases
- Duplicate values.
- Negative numbers.

## Constraint
- `2 <= nums.length <= 10^4`

## Hint
- Store needed complement in hashmap.

## Solution
Single pass: if `target-nums[i]` exists in map, return pair; else store current value and index.

## Similar Questions
- LeetCode: https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/
- GFG: https://www.geeksforgeeks.org/check-if-pair-with-given-sum-exists-in-array/
- Other: - To be added
