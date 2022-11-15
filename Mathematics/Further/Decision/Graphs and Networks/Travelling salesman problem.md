
There are two main variations of the travelling salesman problem, the classical and the practical problems. In the classical problem, each node must be visited exactly once before returning to the starting position. In the practical problem, each node must be visited at least once before returning to the starting position. Note that if a graph is converted to a complete graph of the least distances, both solutions are identical.

A few pieces of terminology are needed to be defined:
\> A walk in a graph is a finite sequencde of arcs such that the end node of one arc is the start node of the next
\> A walk that visits every node, returning to its starting node is called a tour

Note that a tour can visit some nodes more than once. If a tour visits each node exactly once, it is a Hamiltonian cycle.

The travelling salesman problem involves finding a tour of minimum possible weight. There exists no efficient algorithm for solving this problem for real life situations, so a heuristic algorithm is often used. This is an algorithm that finds a good solution, but not necessarily the optimal solution.

In practice, upper and lower bounds for the solution can be found. These are used to "trap" the optimal solution with a set of numbers. As the aim is to bind the optimal solution to the smallest range of values possible, a smaller upper bound is better than a larger upper bound and a larger lower bound is better than a smaller upper bound.

## Lower bounds:

\> Remove each node in turn, together with all of its arcs
\> Find the residual minimum spanning tree (RMST) and find its length through [[MST algorithms]]
\> Add to the RMST the weight of reconecting the deleted node by the two shortest, distinct, arcs and note the total
\> Repeat this for every node, noting the total of each. The greatest total found is the best lower bound
\> Make the lower bound as high as possible to reduce the interval that the optimal solution is contained within
\> If the lower bound is a hamiltonian cycle, or is equal in weight to the upper bound, it is a solution to the problem

## Upper bounds:

#### Initial upper bound:
\> Find the MST for the graph using an [[MST algorithms|MST algorithm]]
\> Double the weight of this MST (this represents retracing your steps) so that the cycle is completed
\> Seek shortcuts to reduce the total weight of the graph (a lower upper bound is better than a higher upper bound)

#### Refined upper bound:
There is another algorithm used to find an upper bound called the nearest neighbour algorithm. The method by finding an MST can be useful for smaller graphs, however can quickly become harder to find shortcuts as the size of the graph increases. The nearest neighbour algorithm is better in general and flows as follows:
\> Select each node in turn as the starting point
\> Go to the nearest node that has not yet been visited
\> Repeat step 2 until all nodes have been visited and then return to the starting node using the shortest availible route
\> Once all nodes have been used as the starting node, select the tour with the smallest weight as the upper bound

This can be done with a distance matrix through the following method:
\> Select each node as the starting node
\> Remove the current node's row from the matrix
\> Select the arc of minimum weight in the current node's column
\> Move to the node this arc connects, making that node the current node
\> Repeat steps 3 and 4 until all nodes have been visited
\> For each starting node, add the cost of reconnecting it via the shortest arc to find the upper bound for that starting node
\> Select the tour with the smallest weight as the upper bound