Kruskal's algorithm is used to find a minimum spanning tree (MST) for a weighted, undirected graph. An MST is defined as a spanning tree (tree that connects all nodes) of minimum weight.

The algorithm flows as follows:
\> Sort all arcs into ascending order of their weight
\> Select the arc of the least weight to add to the tree
\> Consider the next arc of the least weight, if it forms a cycle then reject it, if it does not form a cycle, add it to the tree
\> Repeat step three until all nodes are connected