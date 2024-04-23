## Hamiltonian Cycle 

#### Hamiltonian Cycle 
Cycle that visits every ==vertex== of the graph exactly once and returns to the starting vertex. 

#### Hamiltonian Path
Path that visits every ==vertex== of the graph exactly once and doesn't have to return to the starting vertex - it's an open path. 

### Determining if a graph is Hamiltonian (if it contains a Hamiltonian cycle)
#### 1. Naive approach - O(N!)
Generating all possible configurations and determining if any of them satisfy the given constraints. 

#### 2. Backtracking Algorithm - O(N!)
* Start with node 0. 
* Apply DFS for finding the Hamiltonian path. 
* When base case has been reached, i.e. total number of nodes traversed = number of vertices:
		- Check whether current node is a neighbour of starting node. 
		- If not, backtrack to the previous node. 

## Eulerian Path 
A path in a graph that visits every ==edge== exactly once. 

#### Eulerian Circuit 
A Eulerian Path that starts and ends on the ==same vertex==. 

###### A graph is called Eulerian if it has a Eulerian cycle and it's called Semi-Eulerian if it has an Eulerian Path. 

### Eulerian Cycle 
An undirected graph has Eulerian cycle if following two conditions are true:- 
(a) All vertices with non-zero degree are connected. 
(b) All vertices have even degree 

### Eulerian Path 
An undirected graph has Eulerian Path if following two conditions are true:-
(a) All vertices with non-zero degree are connected. 
(b) If zero or two vertices have odd degree and all other vertices have even degree.  *Two in case of when end nodes have degree = 1*

		Only one vertex with odd degree is not possible in an undirected graph - Sum of all degrees is always even in an undirected graph. 