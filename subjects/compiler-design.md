# ⚙️ Compiler Design

> **Weightage:** ~5% | **Avg Questions:** 3–4 | **Importance:** ⭐⭐⭐⭐

---

## 📊 Overview

Compiler Design is predictable once you learn the mechanics. Parsing is the most tested area — FIRST/FOLLOW sets, LL(1) and SLR/LR(1) parsing tables are asked almost every year. Code optimization is another frequent topic.

**Scoring Pattern:**
- 1–2 questions on Parsing (FIRST/FOLLOW, parsing tables)
- 1 question on Lexical Analysis (tokens, regex)
- 1 question on Code Generation / Optimization
- 0–1 questions on Syntax-Directed Translation

---

## ✅ Topic-wise Checklist

### 🔤 Lexical Analysis
- [ ] Role of lexer: tokenization, symbol table
- [ ] Tokens, lexemes, patterns
- [ ] Regular expressions for tokens (identifiers, numbers, keywords)
- [ ] LEX tool (overview)
- [ ] Error recovery in lexical analysis
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🌲 Parsing (Syntax Analysis)
- [ ] Context-Free Grammars for programming languages
- [ ] Derivations, parse trees, ambiguity
- [ ] Top-down parsing: Recursive descent, LL(1)
- [ ] FIRST set computation rules
- [ ] FOLLOW set computation rules
- [ ] LL(1) parsing table construction
- [ ] Predictive parsing algorithm
- [ ] Left recursion elimination
- [ ] Left factoring
- [ ] Bottom-up parsing: shift-reduce, LR(0), SLR(1), LALR(1), CLR(1)
- [ ] LR(0) items and LR(0) automaton
- [ ] SLR(1) parsing table construction
- [ ] CLR(1)/LR(1) parsing table construction
- [ ] LALR(1) parsing table construction
- [ ] Conflicts: shift/reduce, reduce/reduce
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🏷️ Syntax-Directed Translation (SDT)
- [ ] Attributes: synthesized vs. inherited
- [ ] S-attributed grammar: all attributes synthesized
- [ ] L-attributed grammar
- [ ] Attribute grammars for type checking, expression evaluation
- [ ] SDT schemes
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔧 Intermediate Code Generation
- [ ] Abstract Syntax Tree (AST)
- [ ] Three-address code: assignments, conditionals, loops
- [ ] Quadruples, triples, indirect triples
- [ ] Backpatching
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### ⚡ Code Optimization
- [ ] Local vs. global optimization
- [ ] Basic blocks and flow graphs
- [ ] Common Sub-expression Elimination (CSE)
- [ ] Dead code elimination
- [ ] Loop invariant code motion
- [ ] Loop unrolling, loop fusion
- [ ] Constant folding, constant propagation
- [ ] Strength reduction
- [ ] Data flow analysis: reaching definitions, live variables, available expressions
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🖥️ Code Generation
- [ ] Code generation issues: instruction selection, register allocation
- [ ] Register allocation: graph coloring approach
- [ ] Activation records (stack frame): parameters, locals, return address
- [ ] Runtime environments: static, stack-based, heap
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Rules

### FIRST Set Rules
```
FIRST(a) = {a}  for terminal a
FIRST(ε) = {ε}
FIRST(A) where A → X₁X₂...Xₙ:
  Add FIRST(X₁) - {ε} to FIRST(A)
  If ε ∈ FIRST(X₁), add FIRST(X₂) - {ε}, and so on
  If ε ∈ FIRST(Xᵢ) for all i, add ε to FIRST(A)
```

### FOLLOW Set Rules
```
Add $ to FOLLOW(Start symbol)
For each production A → αBβ:
  Add FIRST(β) - {ε} to FOLLOW(B)
  If ε ∈ FIRST(β), add FOLLOW(A) to FOLLOW(B)
For each production A → αB:
  Add FOLLOW(A) to FOLLOW(B)
```

### LL(1) Parsing Table Construction
```
For each production A → α:
  For each terminal a in FIRST(α), add A → α to M[A, a]
  If ε ∈ FIRST(α):
    For each terminal b in FOLLOW(A), add A → α to M[A, b]
    If $ ∈ FOLLOW(A), add A → α to M[A, $]
```

### LR(0) Item
```
An LR(0) item is a production with a dot (•) indicating progress
A → α•β means α has been seen, β yet to see
Closure: if item A → α•Bβ exists, add B → •γ for all B → γ
Goto: move dot past a symbol
```

### Grammar Classification
```
LL(1) ⊂ SLR(1) ⊂ LALR(1) ⊂ LR(1) = CLR(1)
(LL(1) is the most restrictive; LR(1) is most powerful)
```

---

## ⚠️ Common Mistakes

1. **FIRST of nullable:** If A → ε is possible, ε may be in FIRST(A)
2. **FOLLOW vs FIRST:** FIRST is for the production body; FOLLOW is for the non-terminal
3. **Left recursion:** A → Aα | β has left recursion; must be eliminated for LL(1)
4. **LL(1) conflict:** A grammar with common prefixes or left recursion is NOT LL(1)
5. **SLR vs LALR vs CLR:** SLR uses FOLLOW; LALR merges LR(1) states; CLR keeps them separate
6. **Synthesized vs. inherited:** Synthesized flows up the parse tree; inherited flows down
7. **Code optimization:** Not all optimizations are safe (may change semantics); must be careful
8. **Dead code vs. unreachable code:** Dead = result never used; unreachable = never executed

---

## 📈 PYQ Frequency Analysis

| Topic | Frequency |
|-------|-----------|
| FIRST/FOLLOW computation | Every year |
| LL(1) / SLR(1) parsing tables | Every year |
| Grammar type identification | Most years |
| SDT and attributes | Some years |
| Code optimization | Most years |

---

## 📚 Resources

- **Primary:** Compilers: Principles, Techniques & Tools — Aho (Dragon Book)
- **Video:** Ravindrababu Ravula Compiler Design (YouTube) — excellent for GATE
- **Practice:** GATE Overflow Compiler tag

---

## 📅 PYQ Progress Tracker

- [ ] PYQs 2020–2026 solved
- [ ] PYQs 2015–2019 solved
- [ ] PYQs 2010–2014 solved

---

*Updated: ___ | Revision Count: ___*
