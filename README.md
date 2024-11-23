# CI2024_lab3

The problem of this lab is the \(n^2-1\) Puzzle, which consists of finding the number of steps necessary to sort the puzzle by only sliding the 0 tile with the ones around whenever possible. The goal is to go from a scrambled configuration into a sorted one, where the last tile is 0. In order to solve the problem of this lab, we have used three different approaches for the path search: **A\***, **Breadth-First Search (BFS)**, and **Iterative Deepening Depth-First Search (IDDFS)**. 


## **A\*** Algorithm

- A\* combines BFS and heuristics to explore nodes with the lowest estimated cost \(f(n) = g(n) + h(n)\).
- The heuristic \(h(n)\) (e.g., Manhattan distance) estimates the cost to reach the goal.
- A\* is optimal when the heuristic is admissible (does not overestimate the true cost).


## **Breadth-First Search (BFS)**

- BFS explores all nodes at the current depth level before moving deeper.
- It guarantees finding the shortest solution if one exists.


## **Iterative Deepening Depth-First Search (IDDFS)**

- IDDFS is an improved version of the DFS and explores as far down a branch as possible before backtracking until a solution is found or the maximum depth is reached.
- However, it does not guarantee the shortest solution.


## **Performance Comparison**

The table below compares the performance of A\*, BFS and DFS for solving \(n^2-1\) puzzles of different sizes.

| Algorithm | Puzzle Size | Solution Length | Time (seconds) | 
|-----------|-------------|-----------------|----------------|
| **A\***   | 3x3         | 24              | 0.3            | 
| **BFS**   | 3x3         | 24              | 6.3            |
| **IDDFS**   | 3x3         | 24              | 76.1            | 
| **A\***   | 4x4         | -              | -             |
| **BFS**   | 4x4         | -              | -            | 
| **IDDFS**   | 4x4         | -             | -            | 


## Contributors
Some techniques implemented were developed jointly with [Gabry0501](https://github.com/Gabry323387/).
