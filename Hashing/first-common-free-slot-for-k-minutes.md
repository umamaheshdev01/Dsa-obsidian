# First Common Free Slot for K Minutes


## Question
Given busy intervals for people in a day, find earliest time where everyone is free for at least `k` continuous minutes.

Source:
- Class notes (Q29)
- https://www.desiqna.in/16189/backend-engineer-hackerrank-online-test

## Testcases
- Input:
  `intervals=[(09:00,10:00),(10:30,11:00)], k=20`
  Output:
  `10:00`
  Explanation:
  First free stretch >=20 min starts at 10:00.

## Edge Cases
- Free slot at day start/end.
- Overlapping intervals.

## Constraint
- Day bound: 1440 minutes.

## Hint
- Convert to minutes and use difference array/sweep.

## Solution
Mark busy timeline with diff array, prefix to occupancy, scan for first run of length `k` with occupancy 0.

## Similar Questions
- LeetCode: https://leetcode.com/problems/meeting-scheduler/
- GFG: - To be added
- Other: - To be added
