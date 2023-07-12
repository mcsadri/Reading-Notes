# Implementation: Graphs

## Reading

### [CF DSAs: Graphs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)

- Graph: A non-linear data structure that consists of a set of nodes (vertices) and a set of edges that connect the nodes.
- Vertex: Also known as a node, it represents a data object in a graph. It may be connected to one or more other adjacent vertices
- Edge: A connection between two nodes in a graph.
- Neighbor: The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
- Degree: The degree of a vertex is the number of edges connected to that vertex.
- Undirected Graph: A graph in which the edges are undirected or bi-directional
- Directed Graph (aka Digraph): A graph in which the edges have a direction.
- Complete Graphs: a graph in which each node is connected to each other node in the graph.
- Connected Graph: a graph in which all vertices have at least one edge.
- Disconnect Graph: a graph in which some vertices may not have an edge.
- Cycle:
  - A cycle is when a node can be travered through and potentially end up back at itself.
  - A cycle is defined as a path of a positive length that starts and ends at the same vertex.
- Acyclic Graph: is a Directed graph without cycles.
- Cyclic Graph: is a graph with cycle



- Weighted Graph: A graph in which each edge has a weight or cost associated with it.
- Unweighted Graph: A graph in which all edges have the same weight or no weight at all.
- Adjacency List: A representation of a graph where each node maintains a list of its adjacent nodes.
- Adjacency Matrix: A two-dimensional matrix that represents the connections between nodes in a graph.
- Degree: The number of edges connected to a node in a graph.
- Path: A sequence of nodes in a graph where each consecutive pair of nodes is connected by an edge.
- Cycle: A path in a graph that starts and ends at the same node.
- Connected Graph: A graph in which there is a path between every pair of nodes.
- Disconnected Graph: A graph in which there are one or more pairs of nodes without a path between them.
- Depth-First Search (DFS): A graph traversal algorithm that explores as far as possible along each branch before backtracking.
- Breadth-First Search (BFS): A graph traversal algorithm that explores all the vertices of a graph in breadth-first order.
- Topological Sort: An ordering of the nodes in a directed acyclic graph (DAG) such that for every directed edge from node A to node B, A comes before B in the ordering.
- Minimum Spanning Tree (MST): A subset of the edges of a connected, weighted graph that connects all the vertices with the minimum possible total edge weight.
- Dijkstra's Algorithm: An algorithm for finding the shortest path between nodes in a graph with non-negative edge weights.
- Bellman-Ford Algorithm: An algorithm for finding the shortest path between nodes in a graph with negative or zero edge weights.