# Algorithms and Methods

### Depth-First Search (DFS)
DFS is a search algorithm that explores a state space by expanding the deepest node first. DFS has a time complexity of O(b^m) and a space complexity of O(b*m), where b is the branching degree of the search tree and m is the max depth of the search tree. DFS can be implemented using a LIFO stack for the fringe.

### Breadth-First Search (BFS)
BFS explores the state space by expanding the shallowest node first. BFS has a time complexity of O(b^s) and a space complexity of O(b^s), where b is the branching degree of the search tree and s is the depth of the shallowest solution. BFS can be implemented using a FIFO queue for the fringe.

### Uniform Cost Search
Uniform cost search explores the state space by expanding all nodes that have a cost less than that of the cheapest solution found so far. It can be implemented using a priority queue for the fringe.

### Tree Search vs. Graph Search
In a tree search algorithm, the same node in a state space can be expanded multiple times. In a graph search, the same node can only be expanded once.

### A* Search
A-Star Search is an informed search algorithm that uses a heuristic to estimate the cost of the cheapest solution that can be reached from a particular node. A* searches nodes in the order given by f(n) = g(n) + h(n), where n is a node, g(n) is the cost to reach n, and h(n) is the estimated cost to get from n to the goal.

### Admissible Heuristic
A heuristic is addmissible if 0 <= h(n) <= h*(n), where h*(n) is the true cost to the goal. In other words, an admissible heuristic will never overestimate the cost to reach the goal.

### Consistent Heuristic

### Minimax Search

### Minimax Search w/ Alpha-Beta Pruning

### Expectimax Search


### Value Iteration

### Policy Evaluation

### Policy Extraction

### Reinforcement Learning
* model-based vs. model-free
* policy-based vs. value-based
* on-policy vs. off-policy

### Q-Learning

### Cross-entropy Method

