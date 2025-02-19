# 1B-4

LINK : https://github.com/mburst/dijkstras-algorithm.git

DOCUMENTATION

This C++ program implements a graph data structure and uses Dijkstra's algorithm to find the shortest path between two nodes in the graph. The graph is represented using an adjacency list stored in an unordered_map, where each vertex is associated with another unordered_map representing its adjacent vertices and the weights of the edges connecting them.



Initialization: Distances to all vertices are initialized to infinity (numeric_limits<int>::max()), except for the start vertex, which is set to 0. A priority queue (vector<char> nodes) is maintained to select the next vertex with the smallest distance.
Main Loop: While there are vertices left in the priority queue:
Extract the vertex with the smallest distance.
If this vertex is the destination, reconstruct the shortest path using the previous map and break the loop.
Otherwise, update distances to adjacent vertices if a shorter path is found through the current vertex.
Reconstruct Path: Starting from the destination vertex, backtrack through the previous map to construct the shortest path.


This implementation assumes that all edge weights are non-negative. Dijkstra's algorithm does not work correctly with negative weight edges.
The graph is undirected in this implementation, meaning that an edge from vertex A to B implies an edge from B to A with the same weight.
