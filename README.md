# CI2024_lab3

The problem of this lab is the \(n^2-1\) Puzzle, which consists of finding the number of steps necessary to sort the puzzle by only sliding the 0 tile with the ones around whenever possible. The goal is to go from a scrambled configuration into a sorted one, where the last tile is 0. In order to solve the problem of this lab, we have used three different approaches for the path search: **A\***, **Breadth-First Search (BFS)**, and **Iterative Deepening Depth-First Search (IDDFS)**. Each approach has distinct pros and cons when it comes to the time.

---

## **1. A\*** Algorithm

- A\* combines BFS and heuristics to explore nodes with the lowest estimated cost \(f(n) = g(n) + h(n)\).
- The heuristic \(h(n)\) (e.g., Manhattan distance) estimates the cost to reach the goal.
- A\* is optimal when the heuristic is admissible (does not overestimate the true cost).

---

## **2. Breadth-First Search (BFS)**

- BFS explores all nodes at the current depth level before moving deeper.
- It guarantees finding the shortest solution if one exists.

---

## **3. Iterative Deepening Depth-First Search (IDDFS)**

- IDDFS is an improved version of the DFS and explores as far down a branch as possible before backtracking until a solution is found or the maximum depth is reached.
- However, it does not guarantee the shortest solution.

---

## **Performance Comparison**

The table below compares the performance of A\*, BFS and DFS  for solving \(n^2-1\) puzzles of different sizes. The metrics include:
- **Solution Length**: Number of moves to solve the puzzle.
- **Time (seconds)**: Execution time to find the solution.
- **Memory (MB)**: Approximate memory usage.

| Algorithm | Puzzle Size | Solution Length | Time (seconds) | 
|-----------|-------------|-----------------|----------------|
| **A\***   | 3x3         | 12              | 0.1            | 
| **BFS**   | 3x3         | 12              | 9.2            |
| **IDDFS**   | 3x3         | 15              | 4.0            | 
| **A\***   | 4x4         | 80              | 60             |
| **BFS**   | 4x4         | 80              | 150            | 
| **IDDFS**   | 4x4         | 300             | 600            | 

---

## **Conclusion**

- **A\*** strikes a balance between optimality and efficiency. It is the best choice for larger puzzles if a good heuristic like Manhattan distance is used.
- **BFS** is suitable for small puzzles (e.g., 3x3) where finding the shortest solution is critical. However, its memory requirements make it impractical for larger puzzles.
- **DFS** is memory-efficient but may not find the shortest solution and can perform poorly for larger puzzles.

---

## Contributors
Some techniques implemented were developed jointly with [Gabry0581](https://github.com/Gabry323387/).
