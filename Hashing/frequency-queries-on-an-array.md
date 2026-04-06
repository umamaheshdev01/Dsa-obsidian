# Frequency Queries on an Array


## Question
You are given an array of size `n` and `Q` queries. For each query value `x`, report how many times `x` occurs in the array.

The baseline approach checks frequency for each query by scanning the full array, but the goal is to optimize using hashing.

Two common settings:
- Bounded values: all array values and query values are in range `[0, 50]`.
- General values: array values can be large, so use a hashmap instead of a fixed-size hash array.

Source:
- https://www.geeksforgeeks.org/find-frequency-number-array/
- https://www.geeksforgeeks.org/range-queries-for-frequencies-of-array-elements/
- Reference notes/code set: https://ideone.com/4u4p13 and related links in class notes.

## Testcases
- Input:
  `arr = [1, 3, 2, 4, 2, 1]`
  `queries = [2, 3, 5]`
  Output:
  `2, 1, 0`
  Explanation:
  `2` appears 2 times, `3` appears 1 time, `5` appears 0 times.

- Input:
  `arr = [0, 50, 50, 7, 7, 7]`
  `queries = [0, 7, 50, 10]`
  Output:
  `1, 3, 2, 0`
  Explanation:
  Frequency is answered directly from precomputed hash frequencies.

## Edge Cases
- Query element not present in the array.
- Empty query list (`Q = 0`).
- All elements in array are the same.
- Large element values (fixed hash array is not memory-efficient).

## Constraint
- `1 <= n <= 10^5`
- `0 <= Q <= 10^5`
- Bounded variant: `0 <= arr[i], query[i] <= 50`
- General variant: values may be much larger, so hashmap is preferred.

## Hint
- Precompute frequencies once, answer queries many times.
- If value range is small and fixed, use a frequency array.
- If value range is large/sparse, use hashmap (`key = value`, `value = frequency`).

## Solution
Let `freq` store occurrence counts.

1. Build frequency structure:
- For each `v` in array, do `freq[v]++`.

2. Answer each query `x`:
- Return `freq[x]` if present, otherwise `0`.

Approach comparison:
- Brute force: for each query, scan full array.
  - Time: `O(n * Q)`
  - Space: `O(1)` extra
- Fixed hash array (bounded domain like `[0,50]`):
  - Time: `O(n + Q)`
  - Space: `O(maxValue)`
- Hashmap (general domain):
  - Time: `O(n + Q)` average
  - Space: `O(distinct values)` (worst `O(n)`)

This is optimal for repeated frequency queries over the same array.

## Similar Questions
- LeetCode: - To be added
- GFG: https://www.geeksforgeeks.org/find-frequency-number-array/
- Other: https://www.geeksforgeeks.org/range-queries-for-frequencies-of-array-elements/
