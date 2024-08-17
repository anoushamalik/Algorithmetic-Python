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
