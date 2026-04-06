# Count of Shortest and Longest Subarrays with Sum K


## Question
Count how many subarrays with sum `k` have shortest length and how many have longest length.

Source:
- Class notes (Q9)

## Testcases
- Input:
  `arr=[10,5,2,7,1,9,8,7], k=15`
  Output:
  `shortestCount=2, longestCount=1`
  Explanation:
  Sum-15 subarrays are `[10,5]`, `[5,2,7,1]`, `[8,7]`.

## Edge Cases
- No subarray with sum `k`.
- All valid subarrays same length.

## Constraint
- `1 <= n <= 10^5`

## Hint
- First compute min/max valid lengths, then count subarrays with those lengths.

## Solution
Use prefix-sum hashing to locate sum-k subarrays and track min/max lengths plus counts.

## Similar Questions
- LeetCode: - To be added
- GFG: - To be added
- Other: - To be added
