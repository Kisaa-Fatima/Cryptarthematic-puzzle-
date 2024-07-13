# Cryptarithmetic Puzzles Solver

Cryptarithmetic puzzles are intriguing mathematical problems where numbers are represented by letters or symbols. The objective is to decipher the correspondence between these symbols and digits in a way that satisfies a given arithmetic equation.

## Overview

This repository contains two algorithms implemented to solve cryptarithmetic puzzles using Depth-First Search (DFS) and Uniform Cost Search (UCS). These algorithms are designed to find the unique digit-letter mapping to make the given equation valid.

## Algorithms
## 1. Depth-First Search (DFS) 
** Running Time Complexity ** 
 Worst Case: O(10^8) because there are 8 letters and 10 possible digits.
** Space Complexity** 
Worst Case: O(N) where N is the number of unique letters.
** Solution Approach **
- Search Space Representation: Each level represents a letter and each branch represents a possible assignment of a digit to that letter.
- Backtracking: Start with an empty assignment and explore all possible assignments, backtracking when a constraint is violated.
- Recursive Exploration: At each step, choose an unassigned letter and try assigning each possible digit.
** Code Steps** 
- is_valid_assignment function: Checks if the assignment of digits to letters is valid.
- dfs function: Recursively explores all possible assignments of digits to letters.
- Main Function solve_cryptarithmetic_dfs: Initializes variables and calls the dfs function to find a solution.
- Print the Solution: The main function prints the solution returned by solve_cryptarithmetic_dfs.
## 2. Uniform Cost Search (UCS)
** Running Time Complexity **
Worst Case: O(10^N) where N is the number of unique letters.
** Space Complexity **
Worst Case: O(10^N) where N is the number of unique letters.
** Solution Approach **
- Priority Queue: Start with an empty queue, using a priority queue to keep track of states to explore.
- Cost-Based Expansion: At each step, expand the current state by assigning a digit to the next unassigned letter and calculating the cost.
- Goal Check: If the assignment satisfies the cryptarithmetic equation, return the assignment.
** Code Steps **
- State Class: Represents a state in the search space.
- is_valid_assignment Function: Checks if a given assignment of digits to letters is valid.
- solve_cryptarithmetic_ucs Function: Implements the UCS algorithm to solve the cryptarithmetic puzzle.
- Defining the solve Function: Calls solve_cryptarithmetic_ucs and wraps it with the timeit decorator to measure its execution time.
- Printing the Result: Calls the solve function and prints the result.
## Observations
** Uniform Cost Search (UCS) **
Advantages: Guarantees optimal solution by prioritizing states with lower costs.
Disadvantages: High time and space complexity, especially for puzzles with many unique letters.
** Depth-First Search (DFS) **
Advantages: Explores deep branches before backtracking.
Disadvantages: Does not guarantee an optimal solution, and issues with completeness and optimality.
** Best Algorithm (Opinion) **
A Search:* Balances between completeness, optimality, and efficiency by using heuristic information to guide the search effectively.
## Results
** DFS Algorithm **
- Running Time Complexity: O(10^8)
- Space Complexity: O(N)
** UCS Algorithm **
-Running Time Complexity: O(10^N)
-Space Complexity: O(10^N)
** Optimal Configuration **
- DFS: Suitable for smaller problems with fewer unique letters.
- UCS: More reliable for ensuring optimal solutions but may require significant resources for larger problems.
