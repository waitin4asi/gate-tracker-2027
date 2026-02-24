# 📊 Data Structures & Algorithms

![Weightage](https://img.shields.io/badge/Weightage-10–14%20marks-red)
![Priority](https://img.shields.io/badge/Priority-Very%20High-red)

---

## 📋 Topic Checklist

### 🔷 Arrays & Strings
- [ ] Array operations (insert, delete, search)
- [ ] Two-pointer technique
- [ ] Sliding window
- [ ] Prefix sums
- [ ] Kadane's Algorithm (Maximum subarray)
- [ ] String matching (Naive, KMP, Rabin-Karp)

### 🔷 Linked Lists
- [ ] Singly linked list operations
- [ ] Doubly linked list operations
- [ ] Circular linked list
- [ ] Floyd's cycle detection
- [ ] Reversing a linked list
- [ ] Merge sorted linked lists

### 🔷 Stacks & Queues
- [ ] Stack using arrays and linked lists
- [ ] Queue using arrays and linked lists
- [ ] Circular queue
- [ ] Deque (Double-ended queue)
- [ ] Stack applications: infix/postfix/prefix conversion
- [ ] Priority queue

### 🔷 Trees
- [ ] Binary Trees — traversals (inorder, preorder, postorder, level-order)
- [ ] Binary Search Trees — insert, delete, search
- [ ] AVL Trees — rotations, balance factor
- [ ] Red-Black Trees — properties (conceptual)
- [ ] Heap (Min-Heap, Max-Heap) — heapify, insert, extract
- [ ] Heap Sort
- [ ] Segment Tree
- [ ] Fenwick Tree (BIT)
- [ ] Trie
- [ ] B-Trees and B+ Trees

### 🔷 Graphs
- [ ] Graph representations (adjacency matrix, adjacency list)
- [ ] BFS — time/space complexity, applications
- [ ] DFS — time/space complexity, applications
- [ ] Topological Sort (Kahn's + DFS method)
- [ ] Strongly Connected Components (Kosaraju's, Tarjan's)
- [ ] Shortest Path — Dijkstra's Algorithm
- [ ] Shortest Path — Bellman-Ford
- [ ] Shortest Path — Floyd-Warshall (All pairs)
- [ ] Minimum Spanning Tree — Prim's
- [ ] Minimum Spanning Tree — Kruskal's
- [ ] Union-Find / Disjoint Set Union
- [ ] Articulation Points and Bridges

### 🔷 Hashing
- [ ] Hash functions and properties
- [ ] Collision resolution: chaining, open addressing
- [ ] Linear probing, quadratic probing, double hashing
- [ ] Load factor and rehashing
- [ ] Time complexity analysis

### 🔷 Sorting Algorithms
- [ ] Bubble Sort — stable, O(n²)
- [ ] Selection Sort — unstable, O(n²)
- [ ] Insertion Sort — stable, O(n²) worst, O(n) best
- [ ] Merge Sort — stable, O(n log n), O(n) space
- [ ] Quick Sort — unstable, O(n log n) avg, O(n²) worst
- [ ] Heap Sort — unstable, O(n log n), O(1) space
- [ ] Counting Sort — O(n+k)
- [ ] Radix Sort — O(d(n+k))
- [ ] Lower bound for comparison-based sorting: Ω(n log n)

### 🔷 Searching
- [ ] Linear Search — O(n)
- [ ] Binary Search — O(log n)
- [ ] Binary Search on answer pattern

### 🔷 Dynamic Programming
- [ ] 0/1 Knapsack
- [ ] Unbounded Knapsack
- [ ] Longest Common Subsequence (LCS)
- [ ] Longest Increasing Subsequence (LIS)
- [ ] Matrix Chain Multiplication
- [ ] Edit Distance
- [ ] Coin Change
- [ ] Subset Sum
- [ ] Optimal BST
- [ ] Floyd-Warshall (DP formulation)

### 🔷 Greedy Algorithms
- [ ] Activity Selection Problem
- [ ] Fractional Knapsack
- [ ] Huffman Coding
- [ ] Job Scheduling with Deadlines

### 🔷 Divide and Conquer
- [ ] Merge Sort, Quick Sort (D&C view)
- [ ] Strassen's Matrix Multiplication
- [ ] Binary Search (D&C view)
- [ ] Recurrence relations — Master Theorem

### 🔷 Algorithm Analysis
- [ ] Asymptotic notations: O, Ω, Θ, o, ω
- [ ] Master Theorem (all 3 cases)
- [ ] Amortized analysis (aggregate, accounting, potential)
- [ ] Best / Worst / Average case analysis

---

## ⚡ Key Formulas & Complexities

### Time Complexities — Quick Reference

| Algorithm | Best | Average | Worst | Space |
|---|:---:|:---:|:---:|:---:|
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) |
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) |
| Heap Sort | O(n log n) | O(n log n) | O(n log n) | O(1) |
| Binary Search | O(1) | O(log n) | O(log n) | O(1) |
| BFS / DFS | — | O(V+E) | O(V+E) | O(V) |
| Dijkstra (binary heap) | — | O((V+E) log V) | — | O(V) |
| Bellman-Ford | — | O(VE) | O(VE) | O(V) |
| Floyd-Warshall | — | O(V³) | O(V³) | O(V²) |
| Prim's (binary heap) | — | O(E log V) | — | O(V) |
| Kruskal's | — | O(E log E) | — | O(V) |

### Master Theorem
```
T(n) = aT(n/b) + f(n)

Case 1: f(n) = O(n^(log_b a - ε))  →  T(n) = Θ(n^log_b a)
Case 2: f(n) = Θ(n^log_b a)        →  T(n) = Θ(n^log_b a · log n)
Case 3: f(n) = Ω(n^(log_b a + ε))  →  T(n) = Θ(f(n))
```

### Height of Complete Binary Tree
```
Height = ⌊log₂ n⌋   (for n nodes)
```

### AVL Tree — Rotation Triggers
```
Left-Left    → Single Right Rotation
Right-Right  → Single Left Rotation
Left-Right   → Left then Right Rotation
Right-Left   → Right then Left Rotation
```

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| Confusing stable/unstable sorts | Merge Sort = stable; Heap/Quick Sort = unstable |
| Wrong Master Theorem case | Check ε condition strictly, don't assume |
| Dijkstra on negative edges | Dijkstra fails with negative weights → use Bellman-Ford |
| Quick Sort worst case | Always O(n²) on sorted input with naive pivot |
| AVL vs BST | AVL is self-balancing BST; height difference ≤ 1 |
| Heap insert order | Insert at end, then bubble up (sift up) |

---

## 📊 PYQ Frequency Analysis (2015–2024)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| Sorting Algorithms | Very High (every year) | 1–2 |
| Trees (BST, AVL, Heap) | Very High | 2–4 |
| Graphs (BFS, DFS, Dijkstra) | High | 2–4 |
| Dynamic Programming | High | 2–3 |
| Hashing | Medium | 1–2 |
| Algorithm Complexity | High | 1–2 |
| Linked Lists | Medium | 1 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| Arrays & Strings | ☐ Low / ☐ Med / ☐ High | |
| Linked Lists | ☐ Low / ☐ Med / ☐ High | |
| Trees | ☐ Low / ☐ Med / ☐ High | |
| Graphs | ☐ Low / ☐ Med / ☐ High | |
| Sorting | ☐ Low / ☐ Med / ☐ High | |
| Dynamic Programming | ☐ Low / ☐ Med / ☐ High | |
| Hashing | ☐ Low / ☐ Med / ☐ High | |
