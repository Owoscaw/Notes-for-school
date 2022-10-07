
This algorithm, created by Edsger Wybe Dijkstra, is an algorithm used on an undirected, weighted graph, to find the shortest distance from one node to any other node. For more information on graphs, see [[Graph theory]].

This is the process for applying Dijkstra's algorithm to find the shortest path from $S$ to $T$ through a graph:
\> Label the starting vertex $S_{1}$ with the final label 0
\> Record a working value at evert vertex, $Y$, that is direcly connected to $S_{1}$, or the node that has just recieved its final label, $X$.
\> Working value at $Y=$ final label at $X+$ weight of arc $XY$
\> If there is already a working value at $Y$, it is only replaced if the new value is smaller
\> Once a vertex has a final label, it is not revisited and its working values are no longer to be considered
\> Looking at the working values at all verticies without final labels, select the node with the smallest working value. This now becomes that node's final label
\> Repeat steps 2 through 6 until the desination vertex, $T$, recieves its final label.
\> To find the shortest path, trace back from $T$ to $S$. Given that $B$ already lies on the route, include arc $AB$ whenever the final label of $B-$ final label of $A=$ weight of arc $AB$

The working values, vertex, order of labelling, and final label are often recorded in a table that represents a node:
![[Dijkstra's notation.png|300]]
