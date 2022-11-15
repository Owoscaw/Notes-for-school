
A graph is defined as a collection of nodes and arcs. A node is a point that connects to other nodes through arcs, or paths. A graph is often an abstraction of real life, for example a computer or road network. 

Graphs are often useful for solving problems like the shortest route from point A to point B. They are particularly useful in computer science as an ADT, [[Graphs]]. There are many algorithms that can be performed on a graph to find out minimum distances between nodes, as well as the path that should be taken to achieve this minimum distance.

These are a few definitions associated with graphs:
\> Tree - a graph with no cycles
\> Spanning tree - a tree that connects all nodes
\> Minimum spanning tree - a spanning tree of minimum possible weight, found through an [[MST algorithms|MST algorithm]]
\> Order - the amount of arcs that start or finish at a node
\> Simple graph - a graph with no loops or multiple arcs between nodes
\> Cycle - a route starting and finishing at the same node
\> Connected graph - a graph in which there is a path from one node to every other node
\> Complete graph - a simple graph in which every pair of nodes are connected by an arc
\> Bipartite graph - a graph in which the nodes are in two sets and each arc has a node from each set
\> Sub graph - any set of nodes and arcs taken from a graph
\> Hamiltonian cycle - a cycle that visits every node of the graph
\> Eulerian cycle - a cycle that travels along every edge of the graph
\> Di-graph - a graph in which arcs indicate direction
\> Incidence matrix - a matrix representing the edges in a graph, this is sometimes called an adjacency matrix
\> Distance matrix - a matrix representing the weight of the edges in a graph

The handshake lemma dictates that in every undirected graph, the number of nodes that touch an odd number of arcs is even. This can be represented as:
$$\Huge \sum_{v\in V}deg\,v=2|E|$$
Where $V$ is the set of nodes in the graph and $E$ is the set of arcs in the graph. The triangle inequality must hold for all triangles in the network. The triangle inequality holds that the longest side of any triangle $\leq$ the sum of the two shorter sides.

This is a visual representation of an undirected graph with its adjacency matrix beside it. Node that the arcs between nodes can have weight to indicate the time it takes to travel them, in this case the weight of each arc is 1:
![[Graph theory undirected.png|500]]
This is a directed version of the above graph:
![[Graph theory undirected 1.png|500]]

A graph is Eulerian if it contains a trail that includes every arc and starts and finishes at the same node. Any connected graph whose nodes are all of even order is Eulerian. A graph is semi-Eulerian if it contains a trail that includes every arc, but starts and finishes at different nodes. Any connected graph whose nodes are all even order except for two is semi-Eulerian.  Eulerian and semi-Eulerian graphs can be drawn without lifting a pen off of the paper and without repeating any arcs. 