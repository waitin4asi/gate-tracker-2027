# 📐 Data Structures & Algorithms

> **Weightage:** ~15% | **Avg Questions:** 10–12 | **Importance:** ⭐⭐⭐⭐⭐ (Highest)

---

## 📊 Overview

DSA is the single highest-weightage subject in GATE CSE. Questions range from theoretical (time/space complexity) to coding-style (trace algorithms). Mastery here is non-negotiable for single-digit AIR.

**Scoring Pattern:**
- 4–6 questions from Algorithms (complexity, DP, greedy)
- 3–4 questions from Data Structures (trees, graphs, hashing)
- 2–3 questions from Sorting/Searching
- 1–2 questions from Recursion/Divide & Conquer

---

## ✅ Topic-wise Checklist

### 📦 Arrays & Strings
- [ ] Array representation (1D, 2D, row/column major)
- [ ] String algorithms (KMP, pattern matching)
- [ ] Matrix operations
- [ ] Prefix sums, sliding window, two pointers
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔗 Linked Lists
- [ ] Singly, doubly, circular linked lists
- [ ] Operations: insert, delete, search, reverse
- [ ] Floyd's cycle detection
- [ ] Merge sorted lists
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📚 Stacks & Queues
- [ ] Array and linked list implementations
- [ ] Applications: infix/postfix/prefix evaluation
- [ ] Balanced parentheses
- [ ] Circular queue, deque, priority queue
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🌳 Trees
- [ ] Binary Trees: traversals (inorder, preorder, postorder, level)
- [ ] Binary Search Trees: search, insert, delete, height
- [ ] AVL Trees: rotations (LL, RR, LR, RL), height calculation
- [ ] B-Trees and B+ Trees: insertion, deletion, order
- [ ] Heaps: max-heap, min-heap, heapify, heap sort
- [ ] Segment Trees, Fenwick Trees (overview)
- [ ] Trie data structure
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🕸️ Graphs
- [ ] Representation: adjacency matrix, adjacency list
- [ ] BFS: level-order, finding shortest path (unweighted)
- [ ] DFS: topological sort, cycle detection
- [ ] Shortest path: Dijkstra's, Bellman-Ford, Floyd-Warshall
- [ ] Minimum Spanning Tree: Prim's, Kruskal's
- [ ] Strongly Connected Components (Kosaraju, Tarjan)
- [ ] Bipartite graph checking
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔢 Hashing
- [ ] Hash functions, hash tables
- [ ] Collision resolution: chaining, open addressing
- [ ] Linear probing, quadratic probing, double hashing
- [ ] Load factor and rehashing
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📊 Sorting Algorithms
- [ ] Bubble sort, Selection sort, Insertion sort
- [ ] Merge sort (divide & conquer, stable)
- [ ] Quick sort (partition, pivot selection, worst case)
- [ ] Heap sort
- [ ] Counting sort, Radix sort, Bucket sort (linear)
- [ ] Lower bound for comparison-based sorting: Ω(n log n)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔍 Searching
- [ ] Linear search, Binary search
- [ ] Search in rotated sorted array
- [ ] Binary search on answer technique
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔄 Recursion & Divide and Conquer
- [ ] Recurrence relations: Master Theorem
- [ ] Merge sort, Quick sort, Binary search analysis
- [ ] Tower of Hanoi
- [ ] Strassen's matrix multiplication
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🎯 Greedy Algorithms
- [ ] Activity selection problem
- [ ] Fractional Knapsack
- [ ] Huffman encoding
- [ ] Job scheduling with deadlines
- [ ] Minimum spanning tree (Prim/Kruskal — greedy proof)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 💡 Dynamic Programming
- [ ] Memoization vs. tabulation
- [ ] 0/1 Knapsack
- [ ] Longest Common Subsequence (LCS)
- [ ] Longest Increasing Subsequence (LIS)
- [ ] Matrix Chain Multiplication
- [ ] Edit Distance
- [ ] Coin Change
- [ ] Optimal BST
- [ ] Bellman-Ford (DP perspective)
- [ ] Floyd-Warshall (all-pairs shortest path)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### ⏱️ Complexity Analysis
- [ ] Big-O, Big-Omega, Big-Theta notation
- [ ] Best, average, worst case
- [ ] Space complexity analysis
- [ ] Amortized analysis (aggregate, accounting, potential)
- [ ] Master Theorem (all cases)
- [ ] Substitution method, Recursion tree
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Formulas & Complexity Table

### Sorting Complexity

| Algorithm | Best | Average | Worst | Space | Stable? |
|-----------|------|---------|-------|-------|---------|
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ Yes |
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) | ❌ No |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ Yes |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | ✅ Yes |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) | ❌ No |
| Heap Sort | O(n log n) | O(n log n) | O(n log n) | O(1) | ❌ No |
| Counting Sort | O(n+k) | O(n+k) | O(n+k) | O(k) | ✅ Yes |
| Radix Sort | O(nk) | O(nk) | O(nk) | O(n+k) | ✅ Yes |

### Master Theorem
```
T(n) = aT(n/b) + f(n)

Case 1: f(n) = O(n^(log_b(a) - ε))  →  T(n) = Θ(n^log_b(a))
Case 2: f(n) = Θ(n^log_b(a))         →  T(n) = Θ(n^log_b(a) · log n)
Case 3: f(n) = Ω(n^(log_b(a) + ε))  →  T(n) = Θ(f(n))
```

### Tree Height and Node Formulas
```
Max nodes in binary tree of height h: 2^(h+1) - 1
Min nodes in AVL tree of height h: N(h) = N(h-1) + N(h-2) + 1, N(0)=1, N(1)=2
Height of complete binary tree with n nodes: floor(log₂ n)
Number of leaf nodes in full binary tree with n internal nodes: n+1
```

### Graph Complexity

| Algorithm | Time | Space |
|-----------|------|-------|
| BFS / DFS | O(V+E) | O(V) |
| Dijkstra (Binary Heap) | O((V+E) log V) | O(V) |
| Bellman-Ford | O(VE) | O(V) |
| Floyd-Warshall | O(V³) | O(V²) |
| Prim's (Binary Heap) | O(E log V) | O(V) |
| Kruskal's | O(E log E) | O(V) |

---

## ⚠️ Common Mistakes

1. **AVL Rotation Direction:** Confusing LR and RL rotations — always draw the tree
2. **Quick Sort Worst Case:** O(n²) when array is sorted + first/last element as pivot
3. **Stable vs. Unstable:** Selection sort is NOT stable; Merge sort IS stable
4. **Master Theorem applicability:** Only for recurrences of form T(n) = aT(n/b) + f(n)
5. **Hash collision count:** Forget to account for probe sequences in open addressing
6. **Graph cycle detection:** DFS for directed graphs (back edge = cycle), different for undirected
7. **B-Tree order confusion:** Order m means max m children, max m-1 keys
8. **Amortized ≠ average:** Amortized is over a sequence of operations, not probability-based

---

## 📈 PYQ Frequency Analysis

| Topic | High-Frequency Years | Approx Questions/Year |
|-------|---------------------|----------------------|
| Trees (AVL, BST, B-Tree) | Every year | 2–3 |
| Graph algorithms | Every year | 2 |
| Sorting + Complexity | Every year | 2–3 |
| Dynamic Programming | 2018, 2019, 2021, 2022, 2023 | 1–2 |
| Hashing | 2015, 2017, 2019, 2021, 2023 | 1 |
| Recurrences | Every year | 1 |

---

## 📚 Subject-Specific Resources

- **Primary:** CLRS (Chapter 1–26 relevant)
- **Indian Text:** Narasimha Karumanchi — "Data Structures & Algorithms Made Easy"
- **Video:** Abdul Bari (YouTube) — best for algorithms with animations
- **Practice:** GATE Overflow — DSA tag (all PYQs with discussion)
- **Shortcuts:** GFG GATE CS Notes for quick revision

---

## 📅 PYQ Progress Tracker

- [ ] PYQs 2020–2026 solved
- [ ] PYQs 2015–2019 solved
- [ ] PYQs 2010–2014 solved
- [ ] PYQs 2000–2009 solved (bonus)
- [ ] Second pass: Selected hard PYQs

**Notes on Frequently Repeated Patterns:**
> (Fill in as you solve PYQs)

---

*Updated: ___ | Revision Count: ___*
