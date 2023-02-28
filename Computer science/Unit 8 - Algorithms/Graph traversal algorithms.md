In a sparse graph (not very many verticies), traversal algorithms have complexity $n + e$, where $n$ is the number of nodes and $e$ is the number of arcs. This is effectively $O(n)$. With a maximum (complete) graph, traversal algorithms have complexity $n + n(n - 1)$, as there are $n$ nodes and $n(n - 1)$ arcs. This becomes $n^2 - n$, which is $O(n^2)$.
There are two main methods of traversing a [[Graph theory|graph]], depth first and breadth first:

## Depth first:

In depth first traversal (DFS), a path is fully explored before backtracking and going down the next path. i.e. you go as deep as you can down a path before backtracking.

![[graph DFS.png|200]]

A is pushed onto a stack to keep track of where we have started, as well as appended to a list of visited nodes. B is also appended, as this is where we have traversed to:
![[DFS1.png|450]]
C is B's closest neighbour, so it is visited - adding B to the stack:
![[DFS2.png|450]]
The only unvisited node connected to C is G, so it is visited - adding C to the stack:
![[DFS3.png|450]]
Now, there are no connections to any unvisisted node from the current node, G. So the stack has to be inspected to find how to get back. C is the most recent addition to the stack, so it is popped off and visited:
![[DFS4.png|450]]
The same process is repeated to get to B:
![[DFS5.png|450]]
There is now a connection to an unvisited node, so it is traversed. This adds B back onto the stack, and marks D as visited:
![[DFS6.png|450]]
E is then visited:
![[DFS7.png|450]]
The same process of backtracking is performed, until a node is reached with a connection to an unvisited node. In this case, that is node D:
![[DFS8.png|450]]
Finally, F is visited:
![[DFS9.png|450]]
The algorithm does not end here, the stack needs to be emptied. The same steps as before are taken, until A is visited once more, removing the last item from the stack, completing the algorithm.

This is an example of some code to traverse a graph using DFS:
```python
#call stack acts as the stack
def dfs(graph, currentNode, visitedNodes):
	#marking currentNode as visited
	visitedNodes.append(currentNode)
	#iterating over the currentNode's neighbours
	for node in graph[currentNode]:
		#only visit a node if it has not already been visited
		if node not in visitedNodes:
			#visit next unvisited node
			dfs(graph, node, visitedNodes)
	return visitedNodes
```

## Breadth first:

In depth first traversal (BFS), all neighbouring (adjacent) nodes are explored before exploring all the neighbours of all neighbouring nodes. i.e. all neighbours are searched, a neighbour is chosen, all of that node's neighbours are searched e.c.t.

All adjacent nodes are visited before moving to another node. This is repeated when the next node is traversed to and so on and so forth.

Consider a graph:
![[graph BFS.png|300]]
A list of visited nodes is used, as well as a queue, to manage nodes to visit next:
![[BFS1.png|300]]
A is where we are starting, so it is marked as visited:
![[BFS2.png|300]]
A's adjacent nodes are pushed to the queue:
![[BFS3.png|300]]
B is then visited, so it is added to the visited list, removed from the queue, and it's adjacent nodes are pushed to the back of the queue:
![[BFS4.png|300]]
Same process is repeated with the node at the front of the queue, D:
![[BFS5.png|300]]
E is then visited, it has no adjacent nodes that have not already been added to the queue and have not been visited, so nothing is pushed to the queue:
![[BFS6.png|300]]
![[BFS7.png|300]]
![[BFS8.png|300]]
![[BFS9.png|300]]
All nodes have now been visited, so the traversal is complete. This makes a BFS traversal of the graph: ABDECFG