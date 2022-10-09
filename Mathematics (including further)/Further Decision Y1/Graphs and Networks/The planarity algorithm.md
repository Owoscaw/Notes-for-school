A planar graph is one that can be drawn such that no two arcs cross, except for at a node. The planarity algorithm is used to determine if a graph is planar. The algorithm for determining the planarity of a graph is as follows:
\> Identify a hamiltonian cycle
\> Draw a regular polygon with nodes labelled to match those in the hamiltonian cycle
\> Draw arcs inside the polygon to match the arcs in the original graph that are not represented by the edges of the polygon
\> Make a list of all interior arcs
\> Choose any unlabelled arc and label it "Interior". If all edges are labelled, then the graph is planar
\> Look at any unlabelled arc that cross the previously labelled arc. If there are none, return to step 5. If any of these arcs cross each other, then the graph is non-planar. If none of these edges cross each other, give them the opposite label to the arcs just labelled (opposite of interior is exterior). If all edges are now labelled, the graph is planar. Otherwise, go back to the start of step 6

A pair of arcs that cross inside the hamiltonian cycle would also cross if they were to be drawn on the outside of the hamiltonian cycle. This algorithm attempts to partition the edges not in the hamiltonian cycle into two sets: interior and exterior. If the algorithm determines that the graph is planar, you can draw it without crossings by drawing any arcs labelled "interior" inside the polygon and any arcs labelled "exterior" outside of the polygon.

