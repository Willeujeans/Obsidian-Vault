A non linear collection of vertices and edges
Vertices are nodes and edges are connections
Graphs can be directed or undirected
Directed means the node's edge will point to another node, these are one way pointers, so two edges will be needed to demonstrate a back and fourth between two nodes.

Adjacency Matrix
Time: O(1)
Space: O(V^2)
![[AdjacencyMatrix.png]]
2D array
A -connected-> B therefore 1
B -not connected-> A therefore 0
fast to search, but takes a lot of space to store

Adjacency List
Time: O(V)
Space: O(V+E)
![[AdjacencyList.png]]
An array of linked lists
slow to search, efficient space storage

Example: Obsidian Notes are a linked list system.