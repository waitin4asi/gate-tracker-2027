# 🗄️ Database Management Systems (DBMS)

![Weightage](https://img.shields.io/badge/Weightage-8–10%20marks-red)
![Priority](https://img.shields.io/badge/Priority-Very%20High-red)

---

## 📋 Topic Checklist

### 🔷 ER Model
- [ ] Entities, attributes, relationships
- [ ] Strong vs weak entity sets
- [ ] Cardinality: one-to-one, one-to-many, many-to-many
- [ ] Participation: total vs partial
- [ ] Generalization, specialization, aggregation
- [ ] ER to Relational schema conversion

### 🔷 Relational Model
- [ ] Relational schema, tuples, attributes, domains
- [ ] Keys: super key, candidate key, primary key, foreign key
- [ ] Integrity constraints: entity integrity, referential integrity
- [ ] Relational Algebra operations:
  - [ ] Select (σ), Project (π), Union (∪), Intersection (∩), Difference (−)
  - [ ] Cartesian product (×), Join (⋈)
  - [ ] Natural join, theta join, equijoin
  - [ ] Outer joins (left, right, full)
  - [ ] Division (÷)
- [ ] Relational Calculus (Tuple RC, Domain RC)

### 🔷 SQL
- [ ] DDL: CREATE, ALTER, DROP
- [ ] DML: SELECT, INSERT, UPDATE, DELETE
- [ ] Aggregate functions: COUNT, SUM, AVG, MIN, MAX
- [ ] GROUP BY and HAVING
- [ ] Nested queries (subqueries, correlated subqueries)
- [ ] EXISTS, IN, ANY, ALL
- [ ] Joins in SQL (INNER, LEFT, RIGHT, FULL, CROSS)
- [ ] Views — definition, updateability
- [ ] Triggers — definition and when they fire

### 🔷 Functional Dependencies & Normalization
- [ ] Functional Dependency — definition, trivial/non-trivial
- [ ] Armstrong's axioms: reflexivity, augmentation, transitivity
- [ ] Closure of attribute set (F+)
- [ ] Closure of functional dependency set
- [ ] Minimal cover (canonical cover)
- [ ] 1NF — atomic values, no repeating groups
- [ ] 2NF — no partial dependency on primary key
- [ ] 3NF — no transitive dependency
- [ ] BCNF — every determinant is a superkey
- [ ] BCNF decomposition — lossless, may lose dependency preservation
- [ ] 3NF synthesis — preserves dependencies
- [ ] Multivalued dependency (4NF)
- [ ] Lossless-join decomposition test

### 🔷 Transactions & Concurrency
- [ ] ACID properties: Atomicity, Consistency, Isolation, Durability
- [ ] Transaction states (active, partially committed, committed, failed, aborted)
- [ ] Serializability — conflict serializability, view serializability
- [ ] Precedence graph (conflict serializability test)
- [ ] Concurrency control protocols:
  - [ ] Lock-based: 2-Phase Locking (2PL), strict 2PL
  - [ ] Timestamp ordering
  - [ ] Optimistic concurrency control
- [ ] Deadlock in transactions — detection and prevention
- [ ] Isolation levels: Read Uncommitted, Read Committed, Repeatable Read, Serializable

### 🔷 Indexing & File Organization
- [ ] Dense vs sparse index
- [ ] Clustered vs unclustered index
- [ ] B+ Tree indexing — structure, insert, delete, search
- [ ] Hashing in files — static, dynamic (extendible) hashing
- [ ] File organization: heap, sequential, indexed sequential (ISAM)

### 🔷 Query Processing & Optimization
- [ ] Steps in query processing: parsing → optimization → evaluation
- [ ] Cost estimation: I/O cost, CPU cost
- [ ] Join algorithms: nested loop join, block nested loop, merge join, hash join
- [ ] Equivalence rules for query optimization

---

## ⚡ Key Formulas & Concepts

### Normalization Quick Reference
```
1NF: No multi-valued or composite attributes
2NF: 1NF + No partial dependency (non-prime attr fully depends on PK)
3NF: 2NF + No transitive dependency (non-prime → non-prime not allowed)
BCNF: 3NF + Every determinant must be a super key

4NF: BCNF + No non-trivial multivalued dependencies
5NF: 4NF + No join dependencies
```

### Armstrong's Axioms
```
Reflexivity:   If β ⊆ α, then α → β
Augmentation:  If α → β, then αγ → βγ
Transitivity:  If α → β and β → γ, then α → γ
```

### Conflict Serializability
```
Schedule S is conflict serializable if its precedence graph is ACYCLIC
Precedence graph: Add Ti → Tj if Ti's operation conflicts with Tj's
                  and Ti appears before Tj in the schedule
```

### 2-Phase Locking
```
Phase 1 (Growing): Acquire locks, never release
Phase 2 (Shrinking): Release locks, never acquire
Lock point = first time all needed locks are acquired
```

### Relational Algebra Cardinality
```
|σ_condition(R)| ≤ |R|
|π_A(R)| ≤ |R|
|R × S| = |R| × |S|
|R ⋈ S| ≤ |R × S|
```

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| 2NF only for composite keys | 2NF issue only when PK is composite (partial dependency) |
| BCNF always preserves dependencies | BCNF may NOT preserve all FDs (unlike 3NF) |
| View serializability ⊂ conflict | Conflict serializable ⊂ view serializable |
| Any 2PL prevents deadlock | 2PL prevents only serializability issues, NOT deadlock |
| Clustered = sorted | Clustered index means data stored in index order |
| Natural join = equijoin | Natural join removes duplicate columns; equijoin doesn't |

---

## 📊 PYQ Frequency Analysis (2015–2024)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| Normalization (FDs, 1NF–BCNF) | Very High (every year) | 2–4 |
| Transactions / Serializability | Very High | 2–3 |
| Relational Algebra | High | 1–2 |
| SQL Queries | High | 1–2 |
| B+ Trees / Indexing | Medium | 1–2 |
| ER Model | Medium | 1 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| Normalization | ☐ Low / ☐ Med / ☐ High | |
| Transactions | ☐ Low / ☐ Med / ☐ High | |
| Relational Algebra | ☐ Low / ☐ Med / ☐ High | |
| SQL | ☐ Low / ☐ Med / ☐ High | |
| Indexing | ☐ Low / ☐ Med / ☐ High | |
