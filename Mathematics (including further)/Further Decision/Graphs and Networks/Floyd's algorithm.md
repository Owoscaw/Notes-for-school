This algorithm is like a better version of [[Dijkstra's algorithm]]. Instead of finding the distance from one node to every other node in a graph, this algorithm finds the distanec between any two nodes in a graph. This algorithm also works on two matricies, a distance and a route matrix.

The algorithm flows as follows:
\> Complete an initial distance table for the graph, if there is no direct route from one node to another then label the distance as infinite
\> Complete an initial route table by making every entry in the first column the same as the label at the top of the first column. Do this for every column
\> For the first iteration, copy the values for the first column and row for the distance matrix. Shade these values
\> Consider each unshaded cell. Compare this value to the sum of the shaded values in the cell's column and row. If it is less than the value, write down the sum as the new value. In the route matrix, replace the column and row of the changed cell with the current selected node.
\> Repeat step 4, iterating the shaded cells by one (column 1, row 1 to column 2, row 2 etcetera)
\> The algorithm finishes when there have been $n$ iterations for a graph of $n$ nodes

