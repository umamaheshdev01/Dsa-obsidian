# Maximum Subarray Sum (Kadane)


## Question
Given an integer array, find maximum possible subarray sum.

Source:
- Class notes (Q19)

## Testcases
- Input:
  `arr=[-2,1,-3,4,-1,2,1,-5,4]`
  Output:
  `6`
  Explanation:
  Best subarray is `[4,-1,2,1]`.

## Edge Cases
- All negative values.
- Empty-subarray-allowed variant.

## Constraint
- `1 <= n <= 2*10^5`

## Hint
- Best ending at `i` depends on best ending at `i-1`.

## Solution
Kadane transition: `cur=max(arr[i], cur+arr[i])`, `ans=max(ans, cur)`.

## Similar Questions
- LeetCode: https://leetcode.com/problems/maximum-subarray/
- GFG: https://www.geeksforgeeks.org/largest-sum-contiguous-subarray/
- Other: - To be added
