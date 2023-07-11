# search

Project 1: Single Agent Search

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


Question 5: Finding All the Corners

In this question, the objective is to find the shortest path through a maze that touches all four corners. The search problem is defined as the CornersProblem in searchAgents.py. The problem requires designing a state representation that encodes the information necessary to detect whether all four corners have been reached.

The CornersProblem class represents the search problem and provides methods to determine the start state, goal state, successor states, and whether the goal state has been reached. The state representation used in this problem is a tuple consisting of the current position and a boolean value for each corner, indicating whether it has been visited or not. The algorithm will explore the maze, trying to find the shortest path that touches all four corners, even if there is no actual food in those corners.

Question 6: Corners Problem Heuristic

In this question, a non-trivial, consistent heuristic needs to be implemented for the CornersProblem. The heuristic is used in the A* search algorithm to estimate the cost to the nearest goal and guide the search process.

The heuristic function, called cornersHeuristic, takes a search state as input and returns a non-negative estimate of the remaining cost to reach a goal state. The heuristic should be consistent, meaning that if an action has a cost of c, taking that action should not cause the heuristic value to drop by more than c.

The implementation of the cornersHeuristic function should take into account the specific characteristics of the problem, such as the geometry of the maze and the locations of the corners. It should provide a reasonable estimate of the remaining cost to touch all four corners. The heuristic should reduce the number of nodes expanded during the search compared to an uninformed search algorithm like UCS.

Question 7: Eating All The Dots

In this question, a new search problem called FoodSearchProblem needs to be defined to solve the problem of eating all the Pacman food in as few steps as possible. The objective is to find a path that collects all the food in the Pacman world, taking into account the placement of walls and regular food.

The FoodSearchProblem class is implemented in searchAgents.py and provides methods to determine the start state, goal state, successor states, and whether the goal state has been reached. The problem requires implementing a consistent heuristic function called foodHeuristic that estimates the cost to the nearest goal.

The foodHeuristic function takes a search state as input and returns a non-negative estimate of the remaining cost to reach a goal state. The heuristic should be consistent, ensuring that if an action has a cost of c, taking that action can only cause a drop in the heuristic value of at most c. The heuristic should be designed to expand as few nodes as possible, providing an optimal solution when combined with the A* search algorithm.

Question 8: Suboptimal Search

In some cases, finding the optimal path through all the dots is challenging. In this question, the objective is to implement an agent that greedily eats the closest dot, even if it does not result in the shortest path to eating all the dots.

The ClosestDotSearchAgent class is implemented in searchAgents.py and contains a function called findPathToClosestDot that needs to be implemented. This function solves the AnyFoodSearchProblem, which is missing its goal test, to find a path to the closest dot.
