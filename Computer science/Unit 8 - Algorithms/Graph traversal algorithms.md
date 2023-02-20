There are two main methods of traversing a [[Graph theory|graph]], depth first and breadth first:

## Depth first:

In depth first traversal (DFS), a path is fully explored before backtracking and going down the next path. i.e. you go as deep as you can down a path before backtracking.

![[graph.png|200]]

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