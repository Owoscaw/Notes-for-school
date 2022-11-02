
There are two main variations of the travelling salesman problem, the classical and the practical problems. In the classical problem, each node must be visited exactly once before returning to the starting position. In the practical problem, each node must be visited at least once before returning to the starting position. Note that if a graph is converted to a complete graph of the least distances, both solutions are identical.

A few pieces of terminology are needed to be defined:
\> A walk in a graph is a finite sequencde of arcs such that the end node of one arc is the start node of the next
\> A walk that visits every node, returning to its starting node is called a tour

Note that a tour can visit some nodes more than once. If a tour visits each node exactly once, it is a Hamiltonian cycle.

The travelling salesman problem involves finding a tour of minimum possible weight. There exists no efficient algorithm for solving this problem for real life situations, so a heuristic algorithm is often used. This is an algorithm that finds a good solution, but not necessarily the optimal solution.

In practice, upper and lower bounds for the solution can be found. These are used to "trap" the optimal solution with a set of numbers. As the aim is to bind the optimal solution to the smallest range of values possible, a smaller upper bound is better than a larger upper bound and a larger lower bound is better than a smaller upper bound.

Note that the triangle inequality must hold for all triangles in the network. The triangle inequality holds that the longest side of any triangle $\leq$ the sum of the two shorter sides.