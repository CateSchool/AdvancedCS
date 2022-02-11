# Graphs

  - [Overview](#overview)
    - [Types](#types)
    - [Use Cases](#use-cases)
  - [Classes](#classes)
  - [Big O](#big-o)
  - [Resources](#resources)

---

## Overview
A graph is a **non-linear** data structure (like a tree) that is used to store relationships between many elements or nodes in a network. **Nodes (also vertices)** are comprise the graph, and the **edges** link nodes together.

![graph](assets/overview.jpeg)

### Types

Directed graphs maintain one way relationships, whereas undirected graphs keep track of two-way relationships between nodes.

![graph](assets/directedundirected.jpeg)

A weighted graph keeps track of the weight (think distance or time) between nodes. Consider the following graph representing an airline network:

![graph](assets/weighted.jpeg)

### Use Cases
* determining optimal travel directions between GPS coordinates
* storing relationships between users in a social network
* routing network internet traffic

## Classes

There are two ways to implement a graph:
1. adjacency list
2. adjacency matrix

In this example, we are going to consider the **adjacency list** implementation. Each node stores its value as well as an array of its neighbors. The Graph class stores all of the nodes.

```javascript
class Node {
  constructor(value) {
    this.value = value;
    this.adjacents = [];
  }

  addAdjacent(node) { /* ... */ }
  removeAdjacent(node) { /* ... */ }
}
```

```javascript
class Graph {
  constructor() {
    this.nodes = [];
  }

  addNode(value) { /* ... */ }
  addEdge(source, destination) { /* ... */ }

  removeNode(value) { /* ... */ }
  removeEdge(source, destination) { /* ... */ }
}
```
## Big O  
TBD

## Resources
[Video](https://www.youtube.com/watch?v=c8P9kB1eun4
)  
[Adrian Mejia](https://adrianmejia.com/data-structures-for-beginners-graphs-time-complexity-tutorial/)