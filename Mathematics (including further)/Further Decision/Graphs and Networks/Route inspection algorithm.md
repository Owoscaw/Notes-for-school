
The route inspection algorithm can be used to find the shortest route in a graph that traverses every arc at least once and returns to its starting point. If a graph is Eulerian, this problem is easily solved, as the route can start and end from any node. See [[Graph theory]] for more information on Eulerian and semi-Eulerian graphs. 

This problem is also easily solved if the graph is semi-Eulerian, as the path will be the cycle that starts and ends at the two nodes of odd order plus the shortest distance that connect these two nodes. 

The algorithm flows as follows:
\> Identify any nodes with odd degree (order)
\> Consider all possible complete pairings of these nodes
\> Select the complete pairing with the least sum
\> Add a repeat of the arcs indicated by this pairing to the graph

This algorithm holds for increasing amounts of even multiples of odd nodes (4, 6, 8, ...$2n$ odd nodes). However, there become exponentially more possible pairings to consider. Note that there cannot be an odd number of odd nodes due to the handshake lemma.