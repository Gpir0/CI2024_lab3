First, an **A\*** algorithm was used to guarantee the optimal solution, employing the Manhattan distance between the nodes and the goal state as the heuristic function. Then, a **bidirectional A\*** algorithm was applied, starting from both the top and the bottom of the tree. This algorithm used the Manhattan distance between the current top and bottom solutions of the paths as the heuristic.

The results obtained are the following (N = 4):

### **A\*** (Exact Solution):
- **Number of iterations**: 1,540,131
- **Number of steps to solve the puzzle**: 46

### **Bidirectional A\*** (Heuristic Solution):
- **Number of iterations**: 56,956
- **Number of steps to solve the puzzle**: 48
### Choice of Data Structures:
- Dictionaries and sets allow direct access when checking if a state has already been visited (\( O(1) \)). Storing states in a list would be inefficient due to its \( O(n) \) lookup cost.  
- The case where a node belongs to an already-visited state but has a lower cost in terms of moves compared to the previous one was considered.  

### Note:
To improve performance, the following optimizations could be implemented:  
- Avoid recalculating the Manhattan distance at each step.  
- Avoid frequent conversions between tuples and `np.array`.  
