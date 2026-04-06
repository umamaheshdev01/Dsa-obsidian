# Range Sum Query Using Prefix Sum


## Question
Given an array and multiple queries `[l,r]`, return sum of elements in each range efficiently.

Source:
- Class notes (Q6)
- https://www.spoj.com/problems/CSUMQ/

## Testcases
- Input:
  `arr=[2,4,6,8]`, query `[1,3]`
  Output:
  `18`
  Explanation:
  `4+6+8=18` (0-based indexing example can vary).

## Edge Cases
- `l=r`.
- Query starting at index `0`.

## Constraint
- `1 <= n,q <= 10^5`

## Hint
- Prefix sum array gives O(1) range query.

## Solution
Build prefix `p[i]=p[i-1]+arr[i]`. Query sum: `p[r]-p[l-1]` (or `p[r]` if `l=0`).

## Similar Questions
- LeetCode: https://leetcode.com/problems/range-sum-query-immutable/
- GFG: https://www.geeksforgeeks.org/prefix-sum-array-implementation-applications-competitive-programming/
- Other: https://www.spoj.com/problems/CSUMQ/
