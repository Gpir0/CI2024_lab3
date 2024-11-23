In this code, I implemented the A* algorithm (case \( N = 4 \)) and obtained:
- **Number of iterations**: 356060 (*COST*)  
- **Number of steps to solve the puzzle**: 44 (*QUALITY*)  

### Choice of Data Structures:
- Dictionaries and sets allow direct access when checking if a state has already been visited (\( O(1) \)). Storing states in a list would be inefficient due to its \( O(n) \) lookup cost.  
- The case where a node belongs to an already-visited state but has a lower cost in terms of moves compared to the previous one was considered.  
- The second point introduces issues regarding the number of paths that need to be managed.  

### Note:
To improve performance, the following optimizations could be implemented:  
- Avoid recalculating the Manhattan distance at each step.  
- Avoid frequent conversions between tuples and `np.array`.  
