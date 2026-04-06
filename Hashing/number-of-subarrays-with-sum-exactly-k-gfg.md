# Number of Subarrays with Sum Exactly K


## Question
Count subarrays with sum exactly `k`.

Source:
- https://www.geeksforgeeks.org/number-subarrays-sum-exactly-equal-k/

## Testcases
- Input:
  `arr=[10,2,-2,-20,10], k=-10`
  Output:
  `3`
  Explanation:
  Three subarrays sum to `-10`.

## Edge Cases
- Negative values.
- `k=0`.

## Constraint
- As per source.

## Hint
- Prefix sum with hashmap frequencies.

## Solution
Use `ans += freq[prefix-k]` then increment `freq[prefix]`.

## Similar Questions
- LeetCode: https://leetcode.com/problems/subarray-sum-equals-k/
- GFG: https://www.geeksforgeeks.org/number-subarrays-sum-exactly-equal-k/
- Other: - To be added
