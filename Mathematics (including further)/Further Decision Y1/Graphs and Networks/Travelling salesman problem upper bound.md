
A minimum spanning tree can be used to find an upper bound for the practical [[Travelling salesman problem]]. The method for which is as follows:
\> Find the MST for the graph using [[Prim's algorithm]] or [[Kruskal's algorithm]]
\> Double the weight of this MST (this represents retracing your steps) so that the cycle is completed
\> Seek shortcuts to reduce the total weight of the graph (a lower upper bound is better than a higher upper bound)

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