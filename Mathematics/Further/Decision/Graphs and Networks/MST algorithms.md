A [[Graph theory|minimum spanning tree]] is a subgraph of a graph that connects all nodes using the arcs of least possible weight. There are two main algorithms used to acomplish this, Prim's and Kruskal's.

## Prim's algorithm:

Prims algorithm can be used to find a minimum spanning tree (MST). This algorithm can be carried out on a distance matrix or a graph. To carry it out on a graph:
\> Choose any vertex
\> Select an arc of the least weight that joins a vertex already in the tree to a vertex not yet in the tree
\> Repeat step 2 until all nodes are connected

To carry this algorithm out on an adjacency matrix:
\> Choose any vertex
\> Remove this vertex's row from the matrix
\> Searching in this vertex's column, find the arc of the least weight
\> Select this arc, while removing the row in which this arc is in from the network
\> Select the node that this arc connects
\> Searching in all columns of selected nodes, find the arc of the least weight
\> Repeat from step 4 until all nodes have been selected
\> Draw an MST using the selected arcs


## Kruskals algorithm:

Kruskal's algorithm is used to find a minimum spanning tree (MST) for a weighted, undirected graph. An MST is defined as a spanning tree (tree that connects all nodes) of minimum weight.

The algorithm flows as follows:
\> Sort all arcs into ascending order of their weight
\> Select the arc of the least weight to add to the tree
\> Consider the next arc of the least weight, if it forms a cycle then reject it, if it does not form a cycle, add it to the tree
\> Repeat step three until all nodes are connected
