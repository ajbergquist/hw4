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
A heuristic is consistent if h(n) <= cost(n->m) + h(m), where cost(n->m) is the actual cost to reach state m from state n. In other words, a consistent heuristic guarantees that the value f(n) = g(n) + h(n) never decreases along a path in a graph of the state space.
### Minimax Search
Minimax is an adversarial search algorithm in which players alternate turns, with one side trying to maximize the score and the other trying to minimize it. Minimax produces a state-space search tree in which the value of each node is the best achievable utility against an optimal adversary. For example, the max player assumes the min player will choose the move that minimizes the achievable score, and vice versa.
### Minimax Search w/ Alpha-Beta Pruning
This is a version of minimax search which takes advantage of the fact that some portions of the game tree can be ignored, or pruned, based on previously discovered minimum or maximum scores. Pruning is achieved by keeping track of alpha, the max player's best option on the path to the root of the search tree, and beta, the min player's best option on the path to the root.
### Expectimax Search
Expectimax search is a version of minimax search in which the opponent is not assumed to act optimally. The max nodes are calculated as before, but min nodes are calculated as an expected utility, i.e. a weighted average of the child nodes.
### Value Iteration
Value iteration is a method of determining the values for states of a system with an unknown underlying Markov Decision Process. Values are computed by performing repeated iterations of expectimax until the values converge.
### Policy Evaluation
Policy evaluation finds the values of a system using a fixed policy. Like value iteration, policy evaluation updates values by iterating using the Bellman equations.
### Policy Extraction
Policy extraction is a method for determining the policy implied by a set of optimal values. The policy is found by performing a one-step expectimax using the known values.
### Reinforcement Learning
* Model-Based Learning - Learns an approximate model based on experiences, then solves for values as if the learned model were correct.
* Model-Free - Doesn't estimate an approximate model, but executes an existing policy and learns from the results.
* Policy-based - Learns values by using an explicit policy.
* Value-based - Learns values without knowing policy.
* On-Policy - Learns by following policy and observing results.
* Off-Policy - Converges on optimal policy despite acting suboptimally.
### Q-Learning
* Q-Learning iteratively computes Q-values, which are the values for actions from a particular state. In Q-learning, we take an action from a state, resulting in a sample outcome. We then use the sample to update our estimate of the Q-value for that action and state. Q-learning will converge on an optimal policy, even if suboptimal actions are being taken.
