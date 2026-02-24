# 🗄️ Database Management Systems (DBMS)

> **Weightage:** ~8% | **Avg Questions:** 5–7 | **Importance:** ⭐⭐⭐⭐⭐

---

## 📊 Overview

DBMS is highly predictable in GATE. Normalization and SQL are asked almost every year. Transactions and concurrency control are also frequent. Understanding relational algebra well helps crack tricky SQL questions.

**Scoring Pattern:**
- 2–3 questions on Normalization (1NF–BCNF, finding keys)
- 1–2 questions on SQL (queries, joins, aggregates)
- 1 question on Relational Algebra
- 1 question on Transactions / Concurrency
- 1 question on Indexing / B+ Trees

---

## ✅ Topic-wise Checklist

### 🗂️ ER Model
- [ ] Entities, attributes (simple, composite, multivalued, derived)
- [ ] Relationships, participation constraints (total vs. partial)
- [ ] Cardinality ratios (1:1, 1:N, M:N)
- [ ] Weak entity sets, identifying relationships
- [ ] ER to Relational mapping
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔢 Relational Model
- [ ] Relations, tuples, attributes, schemas
- [ ] Keys: superkey, candidate key, primary key, foreign key
- [ ] Referential integrity
- [ ] Domain constraints, entity integrity
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔣 Relational Algebra
- [ ] Basic operations: σ (select), π (project), × (Cartesian product)
- [ ] Set operations: ∪, ∩, − (union, intersection, difference)
- [ ] Joins: natural join, theta join, equijoin
- [ ] Division operation
- [ ] Renaming operator (ρ)
- [ ] Converting between RA and SQL
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📝 SQL
- [ ] DDL: CREATE, ALTER, DROP
- [ ] DML: SELECT, INSERT, UPDATE, DELETE
- [ ] SELECT with WHERE, GROUP BY, HAVING, ORDER BY
- [ ] Joins: INNER, LEFT, RIGHT, FULL OUTER, CROSS, NATURAL
- [ ] Subqueries: correlated vs. non-correlated
- [ ] Aggregates: COUNT, SUM, AVG, MIN, MAX
- [ ] NULL handling (IS NULL, COALESCE)
- [ ] Views, triggers (conceptual)
- [ ] DISTINCT, UNION, INTERSECT, EXCEPT
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📐 Normalization
- [ ] Functional Dependencies (FD): definition, inference rules (Armstrong's Axioms)
- [ ] Closure of attributes: F+ computation
- [ ] Closure of FD set
- [ ] Finding candidate keys from FDs
- [ ] 1NF, 2NF, 3NF, BCNF: definitions and conversion
- [ ] Minimal cover (canonical form) of FD set
- [ ] Decomposition: lossless join, dependency preservation
- [ ] 4NF, 5NF (overview)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 💳 Transactions & ACID
- [ ] ACID properties: Atomicity, Consistency, Isolation, Durability
- [ ] Transaction states: active, partially committed, committed, failed, aborted
- [ ] Schedules: serial, non-serial, serializable
- [ ] Conflict serializability (precedence graph)
- [ ] View serializability
- [ ] Recoverability: recoverable, cascadeless, strict schedules
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔒 Concurrency Control
- [ ] Lock-based protocols: shared (S), exclusive (X) locks
- [ ] Two-Phase Locking (2PL): basic, strict, rigorous
- [ ] Deadlock in databases: detection, prevention
- [ ] Timestamp-based protocols
- [ ] Optimistic concurrency control
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📁 Indexing & File Organization
- [ ] Ordered indices: dense, sparse
- [ ] B+ Tree structure and operations (insert, delete, search)
- [ ] Hashing: static vs. dynamic hashing
- [ ] ISAM, clustered vs. non-clustered indexes
- [ ] Query cost estimation basics
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Formulas & Rules

### Armstrong's Axioms
```
Reflexivity:   Y ⊆ X → X → Y
Augmentation:  X → Y → XZ → YZ
Transitivity:  X → Y, Y → Z → X → Z
(Derived: Union, Decomposition, Pseudotransitivity)
```

### Candidate Key Identification
```
To find candidate keys from FD set:
1. Find closure of every subset of attributes
2. A set is a superkey if closure = all attributes
3. A minimal superkey is a candidate key
4. LHS-only attributes must be in every key
5. RHS-only attributes are in no key
6. Attributes not in any FD can be in any key
```

### Normal Form Tests
```
1NF : All attributes are atomic (no multivalued, no composite)
2NF : 1NF + No partial dependency (no non-key attribute depends on part of composite PK)
3NF : 2NF + No transitive dependency (non-key → non-key)
BCNF: For every X → Y, X must be a superkey
```

### B+ Tree
```
Order m B+ Tree:
  - Internal node: ⌈m/2⌉ to m children
  - Leaf node: ⌈(m-1)/2⌉ to m-1 keys
  - All data in leaf nodes
  - Leaves linked in a chain
```

### Transaction Conflict Pairs
```
Read-Write (RW), Write-Read (WR), Write-Write (WW) on same item = Conflict
Read-Read (RR) = NOT a conflict
```

---

## ⚠️ Common Mistakes

1. **Candidate key vs. primary key:** Multiple candidate keys possible; PK is one chosen candidate key
2. **BCNF ≠ 3NF:** BCNF is stricter; some 3NF schemas can't be decomposed to BCNF preserving all FDs
3. **NULL in SQL joins:** NULLs are not equal to anything, including NULL (use IS NULL)
4. **Partial vs. transitive dependency:** Partial is about composite PK; transitive is non-key → non-key
5. **Conflict serializability test:** Build precedence graph correctly; cycle = not conflict serializable
6. **2PL types:** Basic 2PL allows cascading rollback; Strict 2PL doesn't release exclusive locks until commit
7. **View serializability:** Harder to check; conflict serializable ⊂ view serializable
8. **SQL HAVING vs. WHERE:** WHERE filters rows; HAVING filters groups (post GROUP BY)

---

## 📈 PYQ Frequency Analysis

| Topic | Frequency |
|-------|-----------|
| Normalization (keys, BCNF) | Every year |
| SQL queries | Every year |
| Relational Algebra | Most years |
| Transactions (serializability) | Most years |
| Indexing / B+ Trees | Alternate years |
| ER Model | Some years |

---

## 📚 Resources

- **Primary:** Database Management Systems — Ramakrishnan & Gehrke
- **Classic:** Database System Concepts — Korth, Silberschatz
- **Online:** GATE Overflow DBMS tag — all PYQs with explanations
- **Video:** Sanchit Jain (YouTube) — excellent DBMS course for GATE
- **Short notes:** GFG GATE DBMS notes

---

## 📅 PYQ Progress Tracker

- [ ] PYQs 2020–2026 solved
- [ ] PYQs 2015–2019 solved
- [ ] PYQs 2010–2014 solved

**Personally Difficult Topics:**
> (Fill in as you practice)

---

*Updated: ___ | Revision Count: ___*
