# Count Subarrays with Equal Frequency of Given Values


## Question
Given array containing only selected values (e.g., `x` and `y`), count subarrays where counts are equal. Extended variant includes 3 or 5 tracked values.

Source:
- Class notes (Q28)

## Testcases
- Input:
  `arr=[x,y,x,y], x=x, y=y`
  Output:
  `4`
  Explanation:
  Transform to `+1/-1` and count zero-sum subarrays.

## Edge Cases
- No balanced subarray.
- Higher-dimension equal-frequency variant.

## Constraint
- `1 <= n <= 2*10^5`

## Hint
- For 2 values: map to `+1/-1` and use prefix frequency.
- For m values: use vector difference signature as hashmap key.

## Solution
Maintain prefix signature and count repeats of same signature to count valid subarrays.

## Similar Questions
- LeetCode: https://leetcode.com/problems/contiguous-array/
- GFG: - To be added
- Other: - To be added
