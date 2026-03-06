# 📁 Greedy Algorithm
- A Greedy Algorithm is a problem-solving method where at each step, we make a choice that seems best at that moment, hoping it will lead to an overall optimal solution.
- Think of it as “taking the best option now” without worrying about the future.
- It works only when the problem has the greedy-choice property and optimal substructure.

## Key Concepts
### Local Choice / Greedy Choice:
At every step, pick the best available option based on some criterion (like largest, smallest, highest ratio, earliest finish, etc.).

### Optimal Substructure:
A problem has optimal substructure if its optimal solution can be built from optimal solutions of subproblems.
Example: Minimum spanning tree uses smaller optimal edges to create the global optimal tree.
<br>
No Backtracking:
- Once a choice is made, it is never changed.
- Unlike dynamic programming, the algorithm does not revisit previous decisions.

## Steps to Solve a Greedy Problem
- Understand the problem clearly.
- Identify the criterion for the “best choice” at each step.
- Apply the greedy choice iteratively or recursively.
<br>
Check if the problem satisfies:
- Greedy-choice property
- Optimal substructure
- Calculate final solution.

## Advantages of Greedy Algorithms:
- Simple and intuitive to understand and implement.
- Often faster than other approaches like dynamic programming.
- Usually O(n log n) or O(n) complexity depending on the sorting or selection step.

## Disadvantages / Limitations:
- Does not guarantee an optimal solution for every problem.
- Example: 0/1 Knapsack problem may fail with greedy.
- Works only if problem has greedy-choice property.

## Common Greedy Problems
Problem	Greedy Strategy Example:
- Coin Change	Pick the largest denomination first
- Fractional Knapsack	Pick items with highest value/weight ratio
- Activity Selection	Choose activity with earliest finishing time
- Minimum Spanning Tree	Prim’s or Kruskal’s algorithm (smallest edge first)
- Huffman Encoding	Merge smallest frequency nodes first

## Example – Coin Change Problem
Problem: Make 30 using coins [25, 10, 5, 1]<br>
Step 1: Pick the largest coin ≤ remaining amount<br>
Take 25 → Remaining = 5<br>
Step 2: Pick next largest coin ≤ remaining<br>
Take 5 → Remaining = 0<br>
Coins used: [25, 5] → This is optimal.<br>
<br>
⚠ Note: If denominations are [25, 20, 1], greedy may not give optimal solution, so always check problem constraints.

## Summary:
Greedy algorithm = Best choice at each step → Global optimum
Works well for problems with:
- Greedy-choice property
- Optimal substructure

Common examples: Coin change, Activity selection, Fractional Knapsack, MST, Huffman Coding

## One-line Definition:
A Greedy Algorithm is an approach where the solution is built step by step, selecting the locally optimal choice at each step, with the hope of reaching a globally optimal solution.
