# ⚙️ Compiler Design

![Weightage](https://img.shields.io/badge/Weightage-4–6%20marks-yellow)
![Priority](https://img.shields.io/badge/Priority-Medium-yellow)

---

## 📋 Topic Checklist

### 🔷 Introduction & Phases
- [ ] Phases of compilation: lexical analysis → syntax analysis → semantic analysis → IR generation → optimization → code generation
- [ ] Compiler vs Interpreter vs Assembler
- [ ] Frontend vs Backend of compiler
- [ ] Symbol table — purpose and structure
- [ ] Error handling at each phase

### 🔷 Lexical Analysis
- [ ] Tokens, patterns, lexemes
- [ ] Role of lexer (scanner)
- [ ] Regular expressions for tokens
- [ ] Finite automata for lexical analysis
- [ ] LEX tool basics
- [ ] Handling whitespace and comments

### 🔷 Syntax Analysis (Parsing)
- [ ] Context-Free Grammar for programming languages
- [ ] Parse trees and abstract syntax trees (AST)
- [ ] Ambiguity in grammars
- [ ] Top-down parsing:
  - [ ] Recursive descent parser
  - [ ] Predictive parser (non-recursive)
  - [ ] LL(1) parsing — FIRST, FOLLOW, parsing table construction
  - [ ] LL(1) conflicts: FIRST-FIRST, FIRST-FOLLOW
  - [ ] Left recursion elimination
  - [ ] Left factoring
- [ ] Bottom-up parsing:
  - [ ] Shift-reduce parsing — stack + input
  - [ ] LR(0) parsing — canonical items, goto/action table
  - [ ] SLR(1) parsing — uses FOLLOW set for reduce actions
  - [ ] CLR(1) — canonical LR(1) — uses lookaheads
  - [ ] LALR(1) — merge LR(1) states with same core
  - [ ] Relationship: LR(0) ⊆ SLR ⊆ LALR ⊆ CLR
- [ ] Shift-reduce and reduce-reduce conflicts

### 🔷 Semantic Analysis
- [ ] Attribute grammars — synthesized vs inherited attributes
- [ ] S-attributed grammar (only synthesized)
- [ ] L-attributed grammar (synthesized + some inherited)
- [ ] Type checking rules
- [ ] Scope and symbol table management

### 🔷 Intermediate Code Generation
- [ ] Three-address code (TAC) — quadruples, triples
- [ ] Syntax-directed translation
- [ ] Backpatching for control flow

### 🔷 Runtime Environment
- [ ] Activation records (stack frames)
- [ ] Static vs dynamic scoping
- [ ] Heap and stack memory management
- [ ] Parameter passing: call by value, call by reference, call by name

### 🔷 Code Optimization
- [ ] Local vs global optimization
- [ ] Basic blocks and flow graphs
- [ ] Common subexpression elimination
- [ ] Constant folding and propagation
- [ ] Dead code elimination
- [ ] Loop optimizations: code motion, strength reduction, induction variables
- [ ] Machine-independent vs machine-dependent optimization

### 🔷 Code Generation
- [ ] Target code: assembly vs machine code
- [ ] Register allocation and assignment
- [ ] Simple code generation algorithm

---

## ⚡ Key Formulas & Algorithms

### FIRST Set Rules
```
FIRST(terminal a) = {a}
FIRST(ε) = {ε}
FIRST(ABC...) = FIRST(A)  (if A cannot derive ε)
               = FIRST(A) ∪ FIRST(BCD...) − {ε}  (if A can derive ε)
```

### FOLLOW Set Rules
```
FOLLOW(S) = {$}  (S = start symbol)
If A → αBβ: FOLLOW(B) ⊇ FIRST(β) − {ε}
If A → αB or A → αBβ where β ⟹* ε: FOLLOW(B) ⊇ FOLLOW(A)
```

### LL(1) Table Construction
```
For each production A → α:
  1. Add A → α to M[A, a] for each a ∈ FIRST(α) − {ε}
  2. If ε ∈ FIRST(α): Add A → α to M[A, b] for each b ∈ FOLLOW(A)
  
Grammar is LL(1) iff table has no conflicts (each cell has ≤ 1 entry)
```

### LR Parsing Summary
| Parser | Power | How Reduce Decided |
|---|---|---|
| LR(0) | Weakest | State alone |
| SLR(1) | Moderate | State + FOLLOW |
| LALR(1) | Strong | State + lookahead (merged) |
| CLR(1) | Strongest | State + lookahead (distinct) |

### Left Recursion Elimination
```
A → Aα | β  ⟹  A → βA'
                A' → αA' | ε
```

### Left Factoring
```
A → αβ₁ | αβ₂  ⟹  A → αA'
                    A' → β₁ | β₂
```

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| S-attributed allows inherited | S-attributed uses ONLY synthesized attributes |
| LALR more powerful than CLR | CLR > LALR ≥ SLR > LR(0) in power |
| LL(1) uses FOLLOW for all | FOLLOW used in LL(1) only when ε ∈ FIRST(α) |
| Left recursion prevents parsing | Only top-down parsers fail; LR parsers handle it |
| Reduce-reduce conflict = SLR only | Shift-reduce conflicts in SLR; Reduce-reduce in any LR |

---

## 📊 PYQ Frequency Analysis (2015–2024)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| FIRST / FOLLOW computation | Very High (every year) | 1–2 |
| LL(1) / SLR / LALR parsing | Very High | 2–3 |
| Shift-reduce parsing trace | High | 1–2 |
| Code optimization | Medium | 1 |
| Attribute grammars | Medium | 1 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| FIRST / FOLLOW | ☐ Low / ☐ Med / ☐ High | |
| LL(1) Parsing | ☐ Low / ☐ Med / ☐ High | |
| LR Parsing (SLR/LALR/CLR) | ☐ Low / ☐ Med / ☐ High | |
| Semantic Analysis | ☐ Low / ☐ Med / ☐ High | |
| Code Optimization | ☐ Low / ☐ Med / ☐ High | |
