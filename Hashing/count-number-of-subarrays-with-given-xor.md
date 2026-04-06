# Count Number of Subarrays with Given XOR


## Question
Given array and value `x`, count subarrays whose XOR is exactly `x`.

Source:
- https://www.geeksforgeeks.org/count-number-subarrays-given-xor/

## Testcases
- Input:
  `arr=[4,2,2,6,4], x=6`
  Output:
  `4`
  Explanation:
  Four subarrays have XOR 6.

## Edge Cases
- `x=0`.
- Repeated values.

## Constraint
- As per source.

## Hint
- Prefix XOR and hashmap of seen prefix XOR values.

## Solution
For running xor `px`, add `freq[px^x]` to answer, then increment `freq[px]`.

## Similar Questions
- LeetCode: https://leetcode.com/problems/count-triplets-that-can-form-two-arrays-of-equal-xor/
- GFG: https://www.geeksforgeeks.org/count-number-subarrays-given-xor/
- Other: - To be added
