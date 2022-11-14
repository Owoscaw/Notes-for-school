A tree is a common abstract data type. It has a root, branches and leaves. A tree is a connected, undirected [[Graphs]] with no cycles. A tree does not have to hwave a root. A rooted tree has a node identified as a root. Every node except the root has one unique parent. Tree are read from top to bottom, the top node being the root. Nodes connected to another node above is that node's child.

\> Root: start of the tree, everyone's parent
\> Parent: has children connecting below it
\> Child: has a parent connecting above it
\> Subtree: see [[Graph theory]]
\> Leaf: a child with no children

A binary tree is a rooted tree in which each node has a maximum of two children. They can be traversed in three different ways:
\> Pre-order: visit the root node, traverse the left subtree and then the right subtree
\> In-order: traverse the left subtree, then visit the root, then traverse the right subtree
\> Post-order: traverse the left subtree, then traverse the right subtree, then visit the root

Note that all these methods of traversing a binary tree are recursive, when traversing the left tree, the child of the root becomes the new root.

A binary search tree holds items in a way that the tree can be searched quickly and easily for a particular item. If an item is less than (in value or in alphabet) a root, it can be added to the left of the root. If the left contains a subtree, do this recursively. If an item is greater than a root, it can be added to the right of the root. To search in a binary search tree, in-order traversal can be used.

This, believe it or not, is useful for [[Searching algorithms|binary search]]. The advantage of using a binary tree for binary search is that it is easier to add elements than in an ordered list. In an ordered list, items have to be shuffled arround in memory so that there is space for a new element. So that searching is efficient as possible, the binary tree should be balanced. A balanced tree is one where the nodes are distribued in a way such that the height is kept to a minimum.

A binary tree can be represented as an array of records, or a 2 dimensional list. In this implimentation, each column can represent a left pointer, data, and a right pointer for a node respectively. If a node has no children to the left, then the pointer ftothe left will be -1. If it does have children, the pointers will contain the index of the nodes to the left/right.