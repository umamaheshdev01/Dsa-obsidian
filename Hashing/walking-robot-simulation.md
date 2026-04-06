# Walking Robot Simulation


## Question
A robot on an infinite XY-plane starts at point (0, 0) facing north. The robot receives an array of integers `commands`, which represents a sequence of moves that it needs to execute. There are only three possible types of instructions the robot can receive:

- `-2`: Turn left 90 degrees.
- `-1`: Turn right 90 degrees.
- `1 <= k <= 9`: Move forward `k` units, one unit at a time.

Some of the grid squares are obstacles. The `i`th obstacle is at grid point `obstacles[i] = (xi, yi)`. If the robot runs into an obstacle, it will stay in its current location (on the block adjacent to the obstacle) and move onto the next command.

Return the maximum squared Euclidean distance that the robot reaches at any point in its path.

Notes:
- There can be an obstacle at `(0, 0)`. If this happens, the robot will ignore the obstacle until it has moved off the origin. However, it will be unable to return to `(0, 0)` due to the obstacle.
- North means `+Y` direction.
- East means `+X` direction.
- South means `-Y` direction.
- West means `-X` direction.
- Source: https://leetcode.com/problems/walking-robot-simulation/

## Testcases
- Input:
  `commands = [4,-1,3], obstacles = []`
  Output:
  `25`
  Explanation:
  Robot goes `(0,0) -> (0,4) -> (3,4)`. Max squared distance is `3^2 + 4^2 = 25`.

- Input:
  `commands = [4,-1,4,-2,4], obstacles = [[2,4]]`
  Output:
  `65`
  Explanation:
  Robot goes `(0,0) -> (0,4)`, turns right, gets blocked at `(2,4)` so stays at `(1,4)`, turns left, then reaches `(1,8)`. Max squared distance is `1^2 + 8^2 = 65`.

- Input:
  `commands = [6,-1,-1,6], obstacles = [[0,0]]`
  Output:
  `36`
  Explanation:
  Robot goes `(0,0) -> (0,6)`, turns right twice to face south, then moves toward origin but is blocked by obstacle at `(0,0)`, so stops at `(0,1)`. Max squared distance is `6^2 = 36`.

## Edge Cases
- Obstacle at origin `(0,0)` should be ignored only at start; robot cannot step back onto origin later.
- Consecutive turns (`-1`, `-2`) with no movement.
- Obstacle directly in front of the robot before a move command.
- Multiple obstacles around path requiring one-step movement checks.

## Constraint
- `1 <= commands.length <= 10^4`
- `commands[i]` is one of `-2`, `-1`, or an integer in `[1, 9]`
- `0 <= obstacles.length <= 10^4`
- `-3 * 10^4 <= xi, yi <= 3 * 10^4`
- Answer is guaranteed to be less than `2^31`

## Hint
- Store all obstacles in a hash set for `O(1)` collision checks.
- Process forward movement one unit at a time so obstacle blocking is handled correctly.
- Track direction using an index over 4 direction vectors and update on left/right turns.

## Solution
Use direct simulation with hashing:

1. Keep current position `(x, y)` and direction index `dir`.
2. Represent directions as vectors in clockwise order, for example: North, East, South, West.
3. For each command:
   - If `-2`, rotate left: `dir = (dir + 3) % 4`.
   - If `-1`, rotate right: `dir = (dir + 1) % 4`.
   - Otherwise move step-by-step for `k` steps:
     - Compute next cell `(nx, ny)`.
     - If `(nx, ny)` is an obstacle, stop this command immediately.
     - Else move to `(nx, ny)` and update answer with `max(ans, x*x + y*y)`.
4. Return `ans`.

Why this works:
- The robot rules require checking obstacles at each unit step, which this simulation does exactly.
- Hashing obstacles makes each collision check constant-time.

Complexity:
- Time: `O(total_steps + obstacles.length)`, where `total_steps` is the sum of all forward command values.
- Space: `O(obstacles.length)`.

## Similar Questions
- LeetCode: https://leetcode.com/problems/robot-bounded-in-circle/
- GFG: https://www.geeksforgeeks.org/check-if-a-given-sequence-of-moves-for-a-robot-is-circular-or-not/
- Other: https://leetcode.com/problems/path-crossing/
