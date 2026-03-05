# GRAPH (Data Structure)
## 1. Introduction
- A Graph is a non-linear data structure used to represent relationships between different objects.

Unlike arrays, stacks, or queues (which are linear), graphs can represent complex connections such as:
- Social networks
- Road maps
- Computer networks
- Web pages with links
- Airline routes

Graphs focus on:
- Nodes (vertices) and the connections (edges) between them.

## 2. Definition of Graph
A Graph is defined as:
- A collection of vertices (nodes) and edges (connections) that link pairs of vertices.

Mathematically:
G = (V, E)
<br>
Where:<br>
V = set of vertices (nodes)<br>
E = set of edges (connections)

## 3. Components of a Graph
### 3.1 Vertex (Node)
- A vertex represents an entity or object.

Examples:
- City
- Person
- Computer
- Web page

### 3.2 Edge
- An edge represents a connection between two vertices.

Examples:
- Road between cities
- Friendship between people
- Cable between computers

## 4. Types of Graphs
### 4.1 Undirected Graph
- Edges have no direction.

Example:<br>
A —— B<br>
Means A is connected to B and B is connected to A.

### 4.2 Directed Graph (Digraph)
- Edges have direction.

Example:<br>
A → B<br>
Means connection from A to B only.<br>

### 4.3 Weighted Graph
Each edge has a weight (cost, distance, time).
<br>
Example:<br>
A --5--> B<br>
Weight = 5 km or cost = 5 units.<br>

### 4.4 Unweighted Graph
- Edges have no weight (just connection).

### 4.5 Cyclic Graph
- Graph contains a cycle.

Example:<br>
A → B → C → A<br>

### 4.6 Acyclic Graph
- No cycle exists.
Example: Tree, DAG (Directed Acyclic Graph)

### 4.7 Connected Graph
- All vertices are reachable from each other.

### 4.8 Disconnected Graph
- Some vertices are not connected.

## 5. Representation of Graph
Graphs are represented using:

### 5.1 Adjacency Matrix
A 2D array where:
- Rows and columns represent vertices
- Value = 1 if edge exists, else 0

Example:<br>
	A	B	C<br>
A	0	1	1<br>
B	1	0	0<br>
C	1	0	0<br>

Advantages:
- Easy to check edge

Disadvantages:
- Uses more memory

### 5.2 Adjacency List
- Each vertex stores a list of connected vertices.

Example:<br>
A → B, C<br>
B → A<br>
C → A<br>

Advantages:
- Saves memory
- Efficient for sparse graphs

## 6. Graph Traversal
Traversal means:
- Visiting all nodes of the graph systematically.
- Two main traversal techniques:
- Breadth First Search (BFS)
- Depth First Search (DFS)

## 7. Breadth First Search (BFS)
### 7.1 Definition
- BFS explores graph level by level.
- It uses a Queue (FIFO).

### 7.2 Steps of BFS
- Start from a node
- Visit it and mark visited
- Add its neighbors to queue
- Repeat until queue is empty

### 7.3 Example
Graph:<br>
A — B — D<br>
|     |<br>
C     E<br>

BFS from A:<br>
A → B → C → D → E<br>

### 7.4 Properties of BFS
- Finds shortest path in unweighted graph
- Uses queue
- Level order traversal

## 8. Depth First Search (DFS)
### 8.1 Definition
DFS explores as deep as possible before backtracking.<br>

It uses:<br>
Stack or recursion<br>

### 8.2 Steps of DFS:
- Visit node
- Go to one unvisited neighbor
- Repeat until dead end
- Backtrack

### 8.3 Example
Graph:<br>
A — B — D<br>
|     |<br>
C     E<br>

DFS from A:<br>
A → B → D → E → C<br>

### 8.4 Properties of DFS
- Uses stack/recursion
- Good for cycle detection
- Good for path existence

## 9. Shortest Path Basics
Shortest path means:
- Finding the minimum distance from one node to another.

Algorithms:
- BFS (unweighted graph)
- Dijkstra’s algorithm (weighted graph)
- Bellman-Ford
- Floyd-Warshall

Example (BFS shortest path)<br>
Graph:<br>
A — B — C<br>
|         |<br>
D ———— E<br>

Shortest path from A to C:
A → B → C

## 10. Applications of Graph
Graphs are used in:
- Google Maps (shortest route)
- Social networks (friend suggestions)
- Computer networks
- Web page ranking
- Airline routes
- Recommendation systems
- Project scheduling
- Game AI
- GPS navigation
- Fraud detection

## 11. Advantages of Graph
- Represents real-world relationships
- Flexible structure
- Efficient traversal
- Supports complex queries

## 12. Disadvantages of Graph
- Complex implementation
- High memory usage (matrix)
- Hard to debug
- Time-consuming for large graphs

## 13. Comparison: BFS vs DFS
| Feature        | BFS             | DFS               |<br>
|----------------|-----------------|-------------------|<br>
| Data Structure | Queue           | Stack / Recursion |<br>
| Path           | Shortest path   | Not guaranteed    |<br>
| Memory         | High            | Low               |<br>
| Use            | Level traversal | Deep traversal    |<br>

## 14. Time Complexity
For adjacency list:
BFS = O(V + E)
DFS = O(V + E)

Where:
- V = vertices
- E = edges

## 15. Example Problem
Graph:
1 — 2 — 3
|         |
4 ———— 5

BFS from 1:
1, 2, 4, 3, 5

DFS from 1:
1, 2, 3, 5, 4

## 16. Important Exam Notes
- Graph = nodes + edges
- BFS uses queue
- DFS uses stack/recursion
- Adjacency list is memory efficient
- Used in shortest path & connectivity problems

## 17. Conclusion:
- A Graph is a powerful data structure used to represent relationships between objects.
- It consists of vertices and edges and supports traversal using BFS and DFS.
- Graphs are the backbone of many real-world systems such as navigation, networking, and social platforms.
- Understanding graph traversal and shortest path concepts is essential for solving complex algorithmic problems.

## One-line Definition:
A graph is a non-linear data structure consisting of vertices and edges that represent relationships between entities and support traversal techniques like BFS and DFS.
