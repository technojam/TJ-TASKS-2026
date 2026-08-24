# Question 2: Tree Construction: Diameter and Leaves

## Explanation

You are given three integers `n`, `d`, and `l`. Your task is to construct a tree with exactly `n` vertices.

The tree must satisfy two conditions:

- It must contain exactly `l` leaves.
- Its diameter must be exactly `d`.

The **diameter** of a tree is the maximum distance between any two vertices, where distance is the number of edges on the path between them.

A **leaf** is a vertex that has exactly one adjacent edge.

For example, when `n = 4`, `d = 2`, and `l = 3`, a tree with vertex `1` connected to vertices `2`, `3`, and `4` has three leaves and a diameter of `2`.

If it is impossible to construct a tree satisfying all the given conditions, print `-1`.

## Problem Statement

You are given three integers `n`, `d`, and `l`.

Construct a tree containing exactly `n` vertices such that:
- The tree has exactly `l` leaves.
- The diameter of the tree is exactly `d`.

If such a tree does not exist, print `-1`.

Otherwise, print the `n - 1` edges of any valid tree.

The vertices must be numbered from `1` to `n`.

The diameter of a tree is the maximum distance between any two vertices.

The distance between two vertices is the number of edges on the unique path between them.

A leaf is a vertex with exactly one adjacent edge.

## Input Format

The first line contains an integer `t`.

Each of the next `t` lines contains three integers:
`n d l`

## Output Format

For each test case:

If no valid tree exists, print:
`-1`

Otherwise, print `n - 1` lines describing the edges of a valid tree.

The edges may be printed in any order.

## Constraints

- `1 <= t <= 10^5`
- `2 <= l <= n <= 2 * 10^5`
- `1 <= d < n`

The sum of `n` over all test cases does not exceed `2 * 10^5`.

## Examples

### Example 1
**Input:**
```text
2
3 2 3
4 2 3
```
**Output:**
```text
-1
1 2
1 3
1 4
```
**Explanation:** 
For `n = 3, d = 2, l = 3`: A tree with 3 vertices can have at most 2 leaves (a straight path), so it is impossible to construct one with 3 leaves. Thus, the output is -1.
For `n = 4, d = 2, l = 3`: A star graph with center vertex 1 connected to vertices 2, 3, and 4 forms a valid tree. It has exactly 4 vertices, a maximum distance of 2 between any two leaves (diameter is 2), and exactly 3 leaves (vertices 2, 3, and 4).

## Topics

- [Trees & Graphs](https://youtu.be/NRghrZdR0G4?si=38zI4RO3pfK6RY4s)
- [DFS/BFS & Tree Diameter](https://youtu.be/pcKY4hjDrxk?si=AtrljJEpfjFHzSpQ)
- [Constructive Algorithms](https://youtu.be/AqpZ-huiyGY?si=WIonjyzWJkeBOXpU)
