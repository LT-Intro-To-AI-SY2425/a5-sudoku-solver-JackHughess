# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?

I think DFS works better for solving Sudoku because the search depth is naturally limited, so it avoids getting stuck going too far down the wrong path and shifts to other areas more quickly. On the other hand, BFS is better in situations where there’s no limit on how deep DFS can go. In those cases, BFS does a good job of exploring more options at a shallow level before narrowing in on the right path.

2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?

The FIFO or LIFO structure of the code probably affected its efficiency, which you can see in the difference in iteration counts when using a Stack versus a Queue. After doing some research, I found out that a priority queue could work for this type of code too since it prioritizes certain elements, which might make the process more efficient.

3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?

For bigger tasks, we’d probably need a more efficient version of DFS or BFS because this assignment seems to be pushing the limits of what these basic methods can handle. You could relate this to real-life situations, like choosing what to eat. When someone has a lot of options, they might explore them in a way that’s kind of like how DFS or BFS works to find the best choice.