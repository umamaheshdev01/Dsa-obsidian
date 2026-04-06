# 4Sum II

#completed
## Question
Given four integer arrays `nums1`, `nums2`, `nums3`, `nums4`, return number of tuples `(i,j,k,l)` such that `nums1[i]+nums2[j]+nums3[k]+nums4[l]=0`.

Source:
- https://leetcode.com/problems/4sum-ii/
- Class notes (Q36)

## Testcases
- Input:
  `nums1=[1,2], nums2=[-2,-1], nums3=[-1,2], nums4=[0,2]`
  Output:
  `2`
  Explanation:
  Two tuples produce sum zero.

## Edge Cases
- Arrays with zeros only.
- Duplicate values.

## Constraint
- `1 <= n <= 200`
- `-2^28 <= nums[i] <= 2^28`

## Hint
- Precompute pair sums of two arrays and frequency-count them.

## Solution
Store frequency of `nums3[k]+nums4[l]` in map, then for each sum from first two arrays add frequency of negated sum.

## Similar Questions
- LeetCode: https://leetcode.com/problems/4sum/
- GFG: https://www.geeksforgeeks.org/count-quadruples-with-sum-k-from-given-four-arrays/
- Other: - To be added
