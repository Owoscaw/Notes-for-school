There is one main method of finding a lower bound for the [[Travelling salesman problem]]. This method involves finding a lower bound for the classical travelling salesman problem through the use of a minimum spanning tree.

The algorithm flows as follows:
\> Remove each node in turn, together with all of its arcs
\> Find the residual minimum spanning true (RMST) and find its length (you can do this through [[Prim's algorithm]])
\> Add to the RMST the weight of reconecting the deleted node by the two shortest, distinct, arcs and note the total
\> Repeat this for every node, noting the total of each. The greatest total found is the best lower bound
\> Make the lower bound as high as possible to reduce the interval that the optimal solution is contained within
\> If the lower bound is a hamiltonian cycle, or is equal in weight to the upper bound, it is a solution to the problem