# Count of Shortest Subarrays with Sum K


## Question
A special subarray is any subarray with sum `k` and minimum possible length among all such subarrays. Count these special subarrays.

Source:
- Class notes (Q30)

## Testcases
- Input:
  `arr=[10,5,2,7,1,9,8,7], k=15`
  Output:
  `2`
  Explanation:
  Shortest length is 2: `[10,5]` and `[8,7]`.

## Edge Cases
- No subarray sum equals `k`.
- Multiple shortest subarrays.

## Constraint
- `1 <= n <= 2*10^5`

## Hint
- Compute all valid lengths, keep global min and count.

## Solution
Use prefix-sum hashmap to generate candidates, track minimum length and its frequency.

## Similar Questions
- LeetCode: - To be added
- GFG: - To be added
- Other: - To be added
