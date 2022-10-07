
[[Dijkstra's algorithm]] is used to find the shortest distance from one node to any other node in an undirected, weighted graph. It is a shortest path algorithm.

The algorithm:

- Select start node
- Temporarily label every node "infinity" distance away from the start node
- All nodes are in a priority queue, with their associated distance (Start is 0 away from start)
- Select the nodes directly connected to start node
- Update each directly connected nodes with the start node's weight added to the weight of any arcs traversed to get to node. Remove start node from the queue
- Select the next node with least associated distance and perform steps 4 and 5 with the current node as start node. Remove currently selected node from queue, only change a node's associated distance if it is less than it's current associated distance


