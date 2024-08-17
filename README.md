### Dijkstra's Algorithm Implementation in Python

#### Overview

This Python script implements Dijkstra's algorithm, a famous algorithm used to find the shortest paths between nodes in a graph. The algorithm is particularly useful for graphs with non-negative edge weights and can determine the shortest path from a single source node to all other nodes in the graph.

#### How It Works

1. **Graph Representation**:
   - The graph is represented as a dictionary, where each key is a node, and the value is another dictionary representing the neighboring nodes and their corresponding edge weights.

2. **Dijkstra's Algorithm**:
   - The algorithm starts with an initial node (called the source or start node) and explores all possible paths from this node to the others.
   - It keeps track of the shortest known distance to each node using a priority queue (min-heap) to always explore the shortest path available.
   - As it explores each node, it updates the shortest distances to its neighboring nodes if a shorter path is found.
   - The algorithm continues until all nodes have been processed.

3. **Data Structures**:
   - **Distances Dictionary**: Stores the shortest known distance to each node from the start node.
   - **Priority Queue (Min-Heap)**: Used to efficiently fetch the node with the smallest distance that hasn't been processed yet.

4. **Output**:
   - The script prints out the shortest distance from the start node to each node in the graph.

#### Example Graph

The script includes an example graph where nodes 'A' through 'G' are connected with edges of varying weights. The graph is passed to the `dijkstra` function, which calculates the shortest paths from the start node 'A'.


#### Sample Output

The script prints the shortest distances from the start node 'A' to all other nodes in the graph:

```
Shortest distances from node A
A : 0
B : 2
C : 3
D : 3
E : 4
F : 9
G : 18
```

#### Customization

- **Graph Modification**: You can modify the graph dictionary to test the algorithm on different graph structures.
- **Start Node**: Change the `start_node` variable to set a different starting point for the algorithm.

#### Notes

- The graph must not contain negative edge weights, as Dijkstra's algorithm does not handle such cases correctly.
- The algorithm assumes all nodes are reachable from the start node. If some nodes are not connected, their distance will remain infinity (`float('inf')`).

#### License

This code is open for educational and personal use. Feel free to modify and experiment with the implementation.


### Kruskal's Algorithm Implementation in Python

#### Overview

This Python script implements Kruskal's algorithm, which is used to find the Minimum Spanning Tree (MST) of a connected, undirected graph. The MST is a subset of the graph's edges that connects all vertices, without any cycles, and with the minimum possible total edge weight.

#### How It Works

1. **Graph Representation**:
   - The graph is represented as a dictionary where each key is a node, and its value is another dictionary representing the neighboring nodes and the edge weights connecting them.

2. **Kruskal's Algorithm**:
   - The algorithm works by sorting all graph edges in the non-decreasing order of their weights.
   - It uses a Disjoint Set (Union-Find) data structure to keep track of which vertices are in which components (or sets).
   - Starting with the smallest edge, the algorithm adds edges to the MST, ensuring that no cycles are formed. This is done by checking if the two vertices of an edge belong to different components. If they do, the edge is added to the MST, and the components are merged.

3. **Functions**:
   - **` find(parent, node)`**: Finds the root of the set that the `node` belongs to, with path compression.
   - **`union(parent, rank, node1, node2)`**: Merges the sets containing `node1` and `node2` using union by rank.
   - **` Kruskal (graph)`**: A main function that implements Kruskal's algorithm to find the MST. It returns the edges in the MST.

4. **Output**:
   - The script prints the edges included in the Minimum Spanning Tree (MST) and their weights.

#### Example Graph

The script includes an example graph with nodes 'A' through 'G'. The `kruskal` function processes this graph to produce the MST.

#### Sample Output

The script prints the edges that are part of the MST, showing which nodes are connected and the weight of each connecting edge:

```
Minimum Spanning Tree using kruskal algorithm:
('C', 'E', 1)
('A', 'B', 2)
('A', 'C', 3)
('B', 'E', 3)
('A', 'D', 3)
('D', 'F', 7)
```

#### Customization

- **Graph Modification**: You can modify the graph dictionary to test the algorithm on different graph structures.

#### Notes

- The graph should be connected and undirected.
- Kruskal's algorithm assumes the graph's edges have non-negative weights.
- The output MST is one of possibly many valid MSTs if the graph has edges with equal weights.

#### License

This code is open for educational and personal use. Feel free to modify and experiment with the implementation.
