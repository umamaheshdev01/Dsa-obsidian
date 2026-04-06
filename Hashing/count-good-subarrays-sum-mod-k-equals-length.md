# Count Good Subarrays Where Sum Mod K Equals Length


## Question
Count subarrays `[i..j]` such that `sum(i..j) % k == length(i..j)`.

Source:
- Class notes (Q25)

## Testcases
- Input:
  `arr=[10,5,2,7,1], k=5`
  Output:
  `To be computed`
  Explanation:
  Use transformed prefix equivalence classes.

## Edge Cases
- `k=1` special handling from class note.
- Negative intermediate modulo values.

## Constraint
- `1 <= n <= 2*10^5`
- `1 <= k <= 10^9`

## Hint
- Rearrange condition using prefix sums and modulo classes.

## Solution
For prefix `p[j]`, compare normalized key `(p[j]%k - j%k + k)%k` with previous prefix keys and count matches.

## Similar Questions
- LeetCode: https://leetcode.com/problems/subarray-sums-divisible-by-k/
- GFG: - To be added
- Other: - To be added
