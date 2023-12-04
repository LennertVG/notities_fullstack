#introductie 
(SOURCE: ChatGPT)
1. **Breadth-First Search (BFS)**:
    
    - BFS explores the maze by visiting all neighbours of the current cell before moving on to the next level.
    - It guarantees the shortest path in an unweighted graph but may not be efficient in large or complex mazes.
2. **Depth-First Search (DFS)**:
    
    - DFS explores the maze by moving as far as possible along one branch before backtracking.
    - It doesn't guarantee the shortest path and can get stuck in infinite loops in some cases.
3. **Dijkstra's Algorithm**:
    
    - Dijkstra's algorithm finds the shortest path by considering the cost of reaching each cell from the start and gradually expanding outward.
    - It's guaranteed to find the shortest path but can be slower than A* if all edge weights are equal.
4. __A_ Algorithm_*:
    
    - A* combines the best features of BFS and Dijkstra's algorithm by using a heuristic to estimate the cost from each cell to the goal.
    - It is one of the most efficient and widely used maze-solving algorithms and guarantees the shortest path if the heuristic is admissible.
5. **Greedy Best-First Search**:
    
    - This algorithm selects the cell that appears closest to the goal based on the heuristic alone.
    - It can be faster than A* but does not guarantee the shortest path.
6. **Bellman-Ford Algorithm**:
    
    - Bellman-Ford is used for solving mazes with weighted edges and can handle negative edge weights.
    - It can find the shortest path but is less efficient than Dijkstra's algorithm when all edge weights are non-negative.
7. **Wall Following (Maze Traversal)**:
    
    - Wall following algorithms follow the maze's walls, keeping one hand (left or right) in contact with the wall.
    - They are often used in solving physical mazes and can find a path but may not guarantee the shortest one.
8. **Randomized Algorithms**:
    
    - These algorithms make random choices to explore the maze until a solution is found.
    - Examples include Random Mouse Algorithm and Randomized Depth-First Search.
9. **Lee Algorithm (Wavefront Algorithm)**:
    
    - Lee's algorithm assigns each cell in the maze a value indicating its distance from the start.
    - It's used for finding paths in grid-based mazes and is efficient for this purpose.
10. **Recursive Division Algorithm**:
    
    - This algorithm constructs mazes rather than solving them.
    - It divides the maze into smaller sections recursively until a desired layout is achieved.

CIRCULAR MAZE
(SOURCE: ChatGPT)
Solving a circular maze efficiently can be challenging because traditional maze-solving algorithms are designed for rectangular grids and may not be directly applicable. However, you can adapt some strategies to solve a circular maze in the least time possible. Here's a general approach:

1. **Start at the Entrance:** Begin at the entrance of the circular maze.
    
2. **Use a Heuristic:** Unlike rectangular mazes, circular mazes don't have a clear "end" or "goal" point. To navigate efficiently, you need a heuristic that guides you toward the center of the circle, assuming the goal is at the center.
    
3. **Keep a Wall on One Side:** One effective strategy is to keep one wall (either the left wall or the right wall) in contact with you at all times. This is known as the "wall-following" strategy.
    
    - **Left Wall Following:** Stick to the left wall as you move through the maze. Keep your left hand on the wall and follow it. This strategy will eventually lead you to the center or to the innermost path.
    - **Right Wall Following:** Similarly, you can choose to follow the right wall, which will also lead you to the center or the innermost path.
4. **Follow Dead Ends:** If you encounter dead ends, return to the last intersection where you made a choice and explore the other path. Continue following the wall until you find a path that leads toward the center.
    
5. **Use a Compass or Directional Sense:** If you have a compass or a good sense of direction, you can use it to navigate toward the center, even in a circular maze.
    
6. **Avoid Backtracking:** Try to minimize backtracking as it can waste time. Keep moving forward, following the wall, and exploring unvisited paths.
    
7. **Adapt to the Maze:** Be flexible in your approach. Circular mazes can vary in complexity, so you may need to adjust your strategy based on the specific maze layout.
    
8. **Be Patient:** Solving a circular maze efficiently may require some trial and error. Be patient and persistent as you explore different paths.
    
9. **Practice:** If possible, practice in simpler circular mazes to develop a better intuition for circular maze solving.
    

Remember that there may not be a single "optimal" path in a circular maze, as the goal is often to reach the center. The key is to navigate in a way that minimizes unnecessary detours and backtracking, which will help you solve the maze in the least time possible.