# Maximum Distance Between Two Occurrences of Same Element


## Question
Find maximum index distance between two occurrences of the same element in array.

Source:
- https://www.geeksforgeeks.org/maximum-distance-two-occurrences-element-array/

## Testcases
- Input:
  `arr=[1,1,2,2,2,1]`
  Output:
  `5`
  Explanation:
  Value `1` appears at indices `0` and `5`.

## Edge Cases
- All unique elements.
- Single element.

## Constraint
- As per source.

## Hint
- Track first occurrence index and maximize distance.

## Solution
Use hashmap for first index of each value; update answer with `i-first[val]`.

## Similar Questions
- LeetCode: - To be added
- GFG: https://www.geeksforgeeks.org/maximum-distance-two-occurrences-element-array/
- Other: - To be added
