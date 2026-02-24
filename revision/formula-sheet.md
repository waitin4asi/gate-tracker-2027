# 📋 GATE 2027 Master Formula Sheet

> *Print this. Paste near study desk. Review daily in final month.*

---

## 📐 DATA STRUCTURES & ALGORITHMS

### Complexity Table

| Algorithm | Best | Average | Worst | Space | Stable? |
|-----------|------|---------|-------|-------|---------|
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ |
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) | ❌ |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | ✅ |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) | ❌ |
| Heap Sort | O(n log n) | O(n log n) | O(n log n) | O(1) | ❌ |
| Counting Sort | O(n+k) | O(n+k) | O(n+k) | O(k) | ✅ |
| Radix Sort | O(nk) | O(nk) | O(nk) | O(n+k) | ✅ |

### Master Theorem
```
T(n) = aT(n/b) + f(n)   [a ≥ 1, b > 1]
Let p = log_b(a)

Case 1: f(n) = O(n^(p-ε))  →  T(n) = Θ(nᵖ)
Case 2: f(n) = Θ(nᵖ)       →  T(n) = Θ(nᵖ log n)
Case 3: f(n) = Ω(n^(p+ε))  →  T(n) = Θ(f(n))
```

### Graph Algorithms Complexity

| Algorithm | Time | Space |
|-----------|------|-------|
| BFS / DFS | O(V+E) | O(V) |
| Dijkstra (heap) | O((V+E) log V) | O(V) |
| Bellman-Ford | O(VE) | O(V) |
| Floyd-Warshall | O(V³) | O(V²) |
| Prim's (heap) | O(E log V) | O(V) |
| Kruskal's | O(E log E) | O(V) |

### Tree Formulas
```
Max nodes in binary tree of height h: 2^(h+1) - 1
Min nodes in AVL tree of height h: N(h) = N(h-1) + N(h-2) + 1
Height of complete BT with n nodes: ⌊log₂ n⌋
Leaf nodes in full BT with n internal nodes: n+1
```

---

## 💻 OPERATING SYSTEMS

### Scheduling
```
Turnaround Time = Completion Time − Arrival Time
Waiting Time = Turnaround Time − Burst Time
Response Time = First CPU Start − Arrival Time
CPU Utilization = CPU busy time / Total time
```

### Memory / Paging
```
Page number = Logical Address ÷ Page Size  (integer division)
Offset = Logical Address mod Page Size
Physical Address = Frame Number × Page Size + Offset
EAT = h(TLB + Mem) + (1-h)(TLB + 2×Mem)   [h = TLB hit ratio]
Page table size = # pages × PTE size
```

### Page Replacement
```
FIFO: May exhibit Belady's anomaly ⚠️
OPT: Optimal — no Belady's anomaly
LRU: Replace least recently used — no Belady's anomaly
```

### Banker's Algorithm (Safety)
```
Work = Available;  Finish[i] = false
Find i: Finish[i] = false AND Need[i] ≤ Work
  → Work += Allocation[i]; Finish[i] = true
Safe if all Finish[i] = true
```

---

## 🗄️ DBMS

### Normalization
```
1NF: Atomic attributes
2NF: 1NF + No partial dependency  [non-key attr depends only on full CK]
3NF: 2NF + No transitive dependency  [non-key → non-key forbidden]
BCNF: For every X → Y, X must be a superkey
```

### Armstrong's Axioms
```
Reflexivity:   Y ⊆ X → X → Y
Augmentation:  X → Y → XZ → YZ
Transitivity:  X → Y, Y → Z → X → Z
```

### Serializability
```
Conflict pairs: RW, WR, WW on same data item
Build precedence graph → cycle = NOT conflict serializable
```

### B+ Tree (order m)
```
Internal node: ⌈m/2⌉ to m children
Leaf node: ⌈(m-1)/2⌉ to m-1 keys; all linked
```

---

## 🌐 COMPUTER NETWORKS

### Physical Layer
```
Nyquist (noiseless):  BW = 2B log₂(V)      [B=bandwidth, V=signal levels]
Shannon (noisy):       BW = B log₂(1 + S/N)
Transmission time = L / R
Propagation delay = d / s
```

### Sliding Window (ARQ)
```
Stop-and-Wait efficiency: η = 1 / (1 + 2a)  [a = prop delay / trans time]
For 100% util: W = 1 + 2a

Go-Back-N:   Sender window = 2^n - 1;   Receiver window = 1
Sel. Repeat: Sender window = 2^(n-1);   Receiver window = 2^(n-1)

η = W / (1 + 2a)  if W < 1 + 2a
η = 1              if W ≥ 1 + 2a
```

### IP Classes (IPv4)
```
Class A: 0–127     /8   [N.H.H.H]
Class B: 128–191   /16  [N.N.H.H]
Class C: 192–223   /24  [N.N.N.H]
Class D: 224–239   Multicast
Class E: 240–255   Reserved
```

### Hamming Code
```
Parity bits p: 2^p ≥ m + p + 1
Parity bit positions: 1, 2, 4, 8, 16, ...
```

---

## 🤖 TOC / AUTOMATA

### Language Hierarchy
```
Type 0 (RE) ⊃ Type 1 (CSL) ⊃ Type 2 (CFL) ⊃ Type 3 (Regular)
     TM           LBA              PDA              FA
```

### Pumping Lemma (Regular)
```
If L regular, ∃ p: ∀ w ∈ L with |w| ≥ p, w = xyz where:
  |y| ≥ 1,  |xy| ≤ p,  ∀k ≥ 0: xy^k z ∈ L
Use contrapositive to prove NON-regularity
```

### Closure Properties

| Operation | Regular | CFL |
|-----------|---------|-----|
| Union | ✅ | ✅ |
| Intersection | ✅ | ❌ |
| Complement | ✅ | ❌ |
| Concatenation | ✅ | ✅ |
| Kleene Star | ✅ | ✅ |
| ∩ with Regular | ✅ | ✅ |

---

## ⚙️ COMPILER DESIGN

### FIRST Set Rules
```
FIRST(terminal a) = {a}
FIRST(ε) = {ε}
FIRST(A):
  For A → X₁X₂...Xₙ:
    Add FIRST(X₁) - {ε}
    If ε ∈ FIRST(X₁): add FIRST(X₂) - {ε}, etc.
    If ε ∈ FIRST(all Xᵢ): add ε
```

### FOLLOW Set Rules
```
FOLLOW(Start) contains $
A → αBβ: add FIRST(β) - {ε} to FOLLOW(B)
A → αBβ, ε ∈ FIRST(β): add FOLLOW(A) to FOLLOW(B)
A → αB: add FOLLOW(A) to FOLLOW(B)
```

### Parser Power
```
LL(1) ⊂ SLR(1) ⊂ LALR(1) ⊂ LR(1)
```

---

## 🖥️ COMPUTER ORGANIZATION

### Pipelining
```
Speedup (ideal) = k  [k = number of stages]
Speedup (real) = kn / (k + n - 1)  [n = instructions]
Cycles for n instructions = k + n - 1
CPI (with d stalls per instruction) = 1 + d
```

### Cache
```
EMAT = h × L1 + (1-h) × (L1 + L2_access_time)  [hierarchical]
Miss rate = 1 - Hit rate

Address bits breakdown:
  Offset bits = log₂(block size)
  Index bits = log₂(number of sets)
  Tag bits = total bits - index - offset
```

### IEEE 754 Single Precision (32-bit)
```
[1 sign][8 exponent][23 mantissa]
Bias = 127
Value = (-1)^s × 2^(e-127) × 1.m
Range: ±1.18 × 10⁻³⁸ to ±3.4 × 10³⁸
```

---

## 🔌 DIGITAL LOGIC

### Key Boolean Laws
```
A + A' = 1     A · A' = 0     A + A = A     A · A = A
A + 1 = 1     A · 0 = 0     A + 0 = A     A · 1 = A
De Morgan: (A+B)' = A'B'     (AB)' = A'+B'
Consensus: AB + A'C + BC = AB + A'C  [BC is redundant]
```

### Flip-Flop Equations
```
D FF:  Q(t+1) = D
T FF:  Q(t+1) = T ⊕ Q
JK FF: Q(t+1) = JQ' + K'Q
SR FF: Q(t+1) = S + R'Q  [SR=1 undefined]
```

---

## 🧮 DISCRETE MATHEMATICS

### Counting Formulas
```
Permutation: P(n,r) = n!/(n-r)!
Combination: C(n,r) = n!/(r!(n-r)!)
With repetition (ordered): nʳ
With repetition (unordered): C(n+r-1, r)
Derangements: D(n) = n! Σᵢ₌₀ⁿ (-1)ⁱ/i!
```

### Inclusion-Exclusion
```
|A∪B| = |A| + |B| - |A∩B|
|A∪B∪C| = |A|+|B|+|C| - |A∩B| - |B∩C| - |A∩C| + |A∩B∩C|
```

### Graphs
```
Handshaking: Σ deg(v) = 2|E|
Tree: |E| = |V| - 1
Euler circuit: all degrees even + connected
Euler path: exactly 2 odd-degree vertices
Planar: V - E + F = 2  (connected)
Kₙ: n(n-1)/2 edges,  chromatic number = n
Bipartite: χ = 2  (if non-trivial)
```

### Number Theory
```
gcd × lcm = a × b
Fermat's: aᵖ⁻¹ ≡ 1 (mod p)  [p prime, gcd(a,p)=1]
Euler's: aᶠ⁽ⁿ⁾ ≡ 1 (mod n)  [gcd(a,n)=1]
φ(pᵏ) = pᵏ - pᵏ⁻¹
```

---

## 🔢 LINEAR ALGEBRA

### Eigenvalue Properties
```
Sum of eigenvalues = tr(A) = Σaᵢᵢ
Product of eigenvalues = det(A)
If Av = λv:
  A^n v = λⁿv;  A⁻¹v = (1/λ)v;  (A-kI)v = (λ-k)v
```

### Systems of Equations (Ax = b)
```
rank(A) = rank([A|b]) = n     →  Unique solution
rank(A) = rank([A|b]) < n    →  Infinite solutions
rank(A) < rank([A|b])         →  No solution
```

### Rank-Nullity
```
rank(A) + nullity(A) = # columns of A
```

---

## 🎲 PROBABILITY

### Key Formulas
```
P(A∪B) = P(A) + P(B) - P(A∩B)
P(A|B) = P(A∩B) / P(B)
Bayes: P(A|B) = P(B|A)P(A) / Σ P(B|Aᵢ)P(Aᵢ)
E[aX+b] = aE[X]+b;  Var(aX+b) = a²Var(X)
Var(X) = E[X²] - (E[X])²
For independent: Var(X+Y) = Var(X)+Var(Y)
```

### Distribution Quick Reference

| Distribution | PMF/PDF | Mean | Variance |
|-------------|---------|------|---------|
| Binomial(n,p) | C(n,k)pᵏ(1-p)ⁿ⁻ᵏ | np | np(1-p) |
| Poisson(λ) | e⁻λλᵏ/k! | λ | λ |
| Geometric(p) | (1-p)ᵏ⁻¹p | 1/p | (1-p)/p² |
| Uniform(a,b) | 1/(b-a) | (a+b)/2 | (b-a)²/12 |
| Exponential(λ) | λe⁻λˣ | 1/λ | 1/λ² |
| Normal(μ,σ²) | Bell curve | μ | σ² |

---

## ∫ ENGINEERING MATHEMATICS

### Derivatives
```
d/dx(xⁿ) = nxⁿ⁻¹,   d/dx(eˣ) = eˣ,   d/dx(ln x) = 1/x
d/dx(sin x) = cos x,  d/dx(cos x) = -sin x,  d/dx(tan x) = sec²x
Chain: d/dx f(g(x)) = f'(g(x))·g'(x)
```

### Taylor Series
```
eˣ = 1 + x + x²/2! + x³/3! + ...
sin x = x - x³/3! + x⁵/5! - ...
cos x = 1 - x²/2! + x⁴/4! - ...
ln(1+x) = x - x²/2 + x³/3 - ...  |x| ≤ 1
```

### ODE
```
First order linear: dy/dx + Py = Q
  Integrating factor: μ = e^(∫P dx)
  Solution: y = (1/μ) ∫μQ dx

Second order: ar² + br + c = 0
  Two real roots r₁≠r₂: y = C₁e^(r₁x) + C₂e^(r₂x)
  Repeated root r: y = (C₁ + C₂x)e^(rx)
  Complex α±βi: y = e^(αx)(C₁cos βx + C₂sin βx)
```

### Numerical Methods
```
Newton-Raphson: xₙ₊₁ = xₙ - f(xₙ)/f'(xₙ)
Trapezoidal: h/2 (f₀ + 2f₁ + ... + 2fₙ₋₁ + fₙ)
Simpson's 1/3: h/3 (f₀ + 4f₁ + 2f₂ + 4f₃ + ... + fₙ)
```

---

## 📝 GENERAL APTITUDE

### Arithmetic Quick Reference
```
SI = PRT/100;  CI = P(1 + R/100)ⁿ - P
Profit % = (Profit/CP) × 100
Speed × Time = Distance
Time together = T₁T₂/(T₁+T₂)
Mixture ratio (alligation): (C₂-C):(C-C₁)
Clock angle: |30H - 5.5M|°
Leap year: divisible by 4; century year by 400
```

---

*Formula Sheet Version: Final | Review Date: ___*
