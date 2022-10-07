
A graph is not a cartesian plane in the context of an [[Queues and ADTs|ADT]]. It is the name given to an ADT that represents complex relationships. An undirected graph means that edges can be traversed in any direction to get to another node. An edge may have a weight to indicate distance, time, etcetera. A directed graph indicates directions, suggesting that edges can only be traversed in one direction. This links heavily to [[Graph theory]].

A graph contains edges/arcs, which are interconnected by vertices/nodes. These edges may be weighted, which indicates cost of traversal. Graphs are used to help computers use maps. Graphs can be implemented as an adjacency matrix or an adjacent list.

A sparse graph (not many connections) may leave a lot of empty space and can therefore waste a lot of space in an array. This wastes memory. An adjacency list can be used instead, as a dictionary containing another dictionary. For a node in general, A, the key in the dictionary would be "A" and its value would be a dictionary containing key:value pairs of node:weight. An adjacency list is more space efficient as it only uses storage for connections that exist.


Applications of graphs include computer networks, navigation, social networks, web pages/links, [[Modelling a project]], and FSM states.

The page rank algorithm, an algorithm used by search engines to display the most relevant page, uses a graph to model the links between pages. If a page links to a page, the page that it links to will be weighted higher. The more links a page receives, the higher it is weighted. A link from a higher weighted page is also worth more than a link from a lower weighed page.
