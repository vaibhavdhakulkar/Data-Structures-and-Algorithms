# 📘 Dynamic Programming (DP)
## 1. Introduction
In computer science, many problems are very complex because they involve:
- Large input sizes
- Repeated calculations
- Recursive structures
- If we solve them using a normal recursive approach, the same subproblems are solved again and again, which wastes time and memory.
- Dynamic Programming (DP) is an optimization technique used to solve such problems efficiently by storing the results of already solved subproblems and reusing them instead of recomputing them.

## 2. Definition of Dynamic Programming
Dynamic Programming is a method of solving complex problems by:
- Breaking them into smaller overlapping subproblems, solving each subproblem once, and storing their results for future use.

### It combines:
- Recursion
- Optimization
- Memory (storage of results)

## 3. Key Characteristics of Dynamic Programming
Dynamic Programming problems have two main properties:

### 3.1 Overlapping Subproblems
- The same subproblems appear many times during recursion.
<br>
Example: Fibonacci series<br>
To compute fib(5):
<br>
fib(5) = fib(4) + fib(3)<br>
fib(4) = fib(3) + fib(2)<br>
fib(3) = fib(2) + fib(1)<br>

Here, fib(3) and fib(2) are calculated multiple times → overlapping subproblems.

### 3.2 Optimal Substructure
A problem has optimal substructure if:
The optimal solution of the main problem can be obtained from optimal solutions of its subproblems.<br>

Example:<br>
Shortest path problem → shortest path to a node depends on shortest path to previous nodes.

4. Techniques in Dynamic Programming

There are two main techniques:<br>

### 4.1 Memoization (Top-Down Approach)
Memoization is a recursive approach where:
- We solve the problem using recursion.
- We store (cache) the result of each subproblem in an array or dictionary.
- If the same subproblem appears again, we return the stored result instead of recomputing it.

Steps:
- Write recursive solution.
- Create a memory structure (array / hashmap).
- Store results when computed.
- Reuse stored results.

Example: Fibonacci with Memoization<br><br>
fib(n):
    if n <= 1:<br>
        return n<br>
    if dp[n] is already computed:<br>
        return dp[n]<br>
    dp[n] = fib(n-1) + fib(n-2)<br>
    return dp[n]<br>
<br>
Time Complexity: O(n)<br>
Space Complexity: O(n)<br>

### 4.2 Tabulation (Bottom-Up Approach)
Tabulation is an iterative approach where:
- We start solving from the smallest subproblems.
- Build the solution step by step up to the main problem.
- Store results in a table (array).

Steps:
- Create DP table.
- Initialize base cases.
- Fill table using loop.
- Return final value.

Example: Fibonacci with Tabulation<br>
dp[0] = 0<br>
dp[1] = 1<br>
<br>
for i = 2 to n:<br>
    dp[i] = dp[i-1] + dp[i-2]<br>
<br>
Time Complexity: O(n)<br>
Space Complexity: O(n)<br>

## 5. Why Dynamic Programming is Needed
Without DP:
- Time complexity is exponential (2ⁿ)
- Too slow for large inputs
<br>
With DP:
- Each subproblem is solved once
- Huge reduction in time complexity
- Efficient for large datasets

## 6. General Steps to Solve a DP Problem
- Identify the problem type (optimization, counting, decision).
- Define subproblems.
- Write recurrence relation (formula).
- Choose DP method (memoization or tabulation).
- Define base cases.
- Compute and store results.
- Return final answer.

## 7. Common Dynamic Programming Problems
- Fibonacci Series
- Knapsack Problem
- Longest Common Subsequence (LCS)
- Longest Increasing Subsequence (LIS)
- Matrix Chain Multiplication
- Coin Change Problem
- Edit Distance
- Rod Cutting Problem

## 8. Example Problem: Coin Change (Simple Explanation)
Problem:<br>
- Find minimum number of coins to make amount = 5 using coins [1,2,5]

### Subproblems:
Solve for amount = 0,1,2,3,4,5

### DP Table:
dp[0] = 0<br>
dp[1] = 1<br>
dp[2] = 1<br>
dp[3] = 2<br>
dp[4] = 2<br>
dp[5] = 1<br>
<br>
Final Answer: dp[5] = 1

## 9. Advantages of Dynamic Programming
- Reduces time complexity
- Avoids repeated computation
- Efficient for large problems
- Clear problem structure
- Widely used in real-world systems

## 10. Disadvantages of Dynamic Programming
- Uses extra memory
- Hard to design recurrence relation
- Complex implementation
- Debugging can be difficult

## 11. Real-Life Applications of DP
- GPS navigation (shortest path)
- DNA sequence alignment
- Speech recognition
- Image processing
- Resource allocation
- Financial optimization
- Scheduling problems
- Game strategy problems

## 12. Difference Between Recursion and Dynamic Programming
- Feature	Recursion	Dynamic Programming
- Repeated calculations	Yes	No
- Speed	Slow	Fast
- Memory usage	Low	Higher
- Optimization	No	Yes

## 13. Conclusion
Dynamic Programming is a powerful algorithmic technique that helps solve complex problems efficiently by:
- Breaking them into smaller overlapping subproblems
- Storing intermediate results
- Reusing them to build the final solution
- It transforms exponential-time solutions into polynomial-time solutions and is essential for solving real-world optimization and decision-making problems.

## One-line Definition (Exam Ready)
Dynamic Programming is an optimization technique that solves complex problems by dividing them into overlapping subproblems and storing their solutions using memoization or tabulation.
