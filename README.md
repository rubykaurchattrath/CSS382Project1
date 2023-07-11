# search

Project 1: Single Agent Search

Explanation for each solution:

Question 1: Depth First Search (DFS)
The depthFirstSearch function implements the depth-first search algorithm. It initializes a stack called "frontier" to keep track of states to be explored. The "exploredNodes" list stores the states that have been visited. The start state is obtained from the problem object using the getStartState method. The start node is created with the start state and an empty list of actions. The start node is then pushed onto the frontier stack.

The algorithm continues until the frontier stack is empty. It pops the last node from the frontier stack and checks if it has already been explored. If not, it marks the current state as explored and checks if it is the goal state. If it is the goal state, the algorithm returns the list of actions. Otherwise, it expands the current node by generating the successor states and pushes them onto the frontier stack.

Question 2: Breadth First Search (BFS)
The breadthFirstSearch function implements the breadth-first search algorithm. It uses a queue called "frontier" to keep track of states to be explored. The "exploredNodes" list stores the states that have been visited. The start state is obtained from the problem object using the getStartState method. The start node is created with the start state, an empty list of actions, and a cost of 0. The start node is then pushed onto the frontier queue.

The algorithm continues until the frontier queue is empty. It dequeues the first node from the frontier queue and checks if it has already been explored. If not, it marks the current state as explored and checks if it is the goal state. If it is the goal state, the algorithm returns the list of actions. Otherwise, it expands the current node by generating the successor states and enqueues them into the frontier queue.

Question 3: Uniform Cost Search (UCS)
The uniformCostSearch function implements the uniform-cost search algorithm. It uses a priority queue called "frontier" to keep track of states to be explored, ordered by the total cost. The "exploredNodes" dictionary stores the states as keys and their respective costs as values. The start state is obtained from the problem object using the getStartState method. The start node is created with the start state, an empty list of actions, and a cost of 0. The start node is then pushed onto the frontier priority queue with a priority of 0.

The algorithm continues until the frontier priority queue is empty. It dequeues the node with the lowest cost from the frontier priority queue and checks if its state has already been explored with a lower cost. If not, it marks the current state as explored and checks if it is the goal state. If it is the goal state, the algorithm returns the list of actions. Otherwise, it expands the current node by generating the successor states and updates their costs based on the current cost. The updated successor nodes are pushed into the frontier priority queue.

Question 4: A* Search (AStar)
The aStarSearch function implements the A* search algorithm. It uses a priority queue called "frontier" to keep track of states to be explored, ordered by the sum of the cost and the heuristic value. The "exploredNodes" list stores the states that have been visited along with their costs. The start state is obtained from the problem object using the getStartState method. The start node is created with the start state, an empty list of actions, and a cost of 0. The start node is then pushed onto the frontier priority queue with a priority based on the sum of the cost and the heuristic value.

The algorithm continues until the frontier priority queue is empty. It dequeues the node with the lowest combined cost and heuristic value from the frontier priority queue and checks if its state has already been explored with a lower cost. If not, it marks the current state as explored and checks if it is the goal state. If it is the goal state, the algorithm returns the list of actions. Otherwise, it expands the current node by generating the successor states and updates their costs based on the current cost. The updated successor nodes are pushed into the frontier priority queue with priorities based on the sum of the cost and the heuristic value.

