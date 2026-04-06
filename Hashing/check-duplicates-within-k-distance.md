# Check Duplicates Within K Distance


## Question
Given an array and integer `k`, determine whether there exist two equal elements whose index distance is `<= k`.

Source:
- Class notes (Q2)

## Testcases
- Input:
  `arr=[1,2,3,1], k=3`
  Output:
  `true`
  Explanation:
  `arr[0]=arr[3]=1`, distance is `3`.

## Edge Cases
- `k=0`.
- All values distinct.

## Constraint
- `1 <= n <= 10^5`

## Hint
- Track last index of each value using hashmap.

## Solution
For each index `i`, if value seen before at `j` and `i-j <= k`, return true. Update last index each step.

## Similar Questions
- LeetCode: https://leetcode.com/problems/contains-duplicate-ii/
- GFG: https://www.geeksforgeeks.org/check-given-array-contains-duplicate-elements-within-k-distance/
- Other: - To be added
