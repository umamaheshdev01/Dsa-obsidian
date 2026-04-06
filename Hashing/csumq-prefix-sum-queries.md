# CSUMQ Prefix Sum Range Queries


## Question
Answer multiple range sum queries efficiently.

Source:
- https://www.spoj.com/problems/CSUMQ/

## Testcases
- Input:
  `arr=[1,2,3,4], query [1,2]`
  Output:
  `5`
  Explanation:
  `2+3=5`.

## Edge Cases
- Full range query.
- Single element range.

## Constraint
- As per SPOJ CSUMQ.

## Hint
- Prefix array precomputation.

## Solution
Compute prefix sums once, answer each query in O(1).

## Similar Questions
- LeetCode: https://leetcode.com/problems/range-sum-query-immutable/
- GFG: https://www.geeksforgeeks.org/prefix-sum-array-implementation-applications-competitive-programming/
- Other: https://www.spoj.com/problems/CSUMQ/
