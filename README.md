# knights_tour

Find the hamiltonian path for a knight on a chessboard, such that they make 63 legal moves and visit each sqare of an 8x8 chessboard exactly once. 

For context on the scope of the problem, the total search space is 5.02e58 (legal 63 move tours around the board), the number of open tours is 1.31e35 and the approx number of closed tours is 1.33e13. 

## Warnsdorf
Depth First Search (DFS) with backtracking, where each move the knight moves to the square with the lowest number of next
moves available. The thinking is that at the end of the tour, the knight will visit squares with more choices available. The
way this was presented to me, this amounts to the knight processing around the edge first (where the move possibilities are fewer), and then proceeding to the middle of the board. 

## Divide and Conquer
Recurse over smaller subboards and then stitch together solution.

## Ant Colony Optimization (ACO)

Hingston & Kendell (2004) implemented this variation, exploring both *open* and *closed* tours (ending one legal move away from the knight's starting position). 
