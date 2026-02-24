# 💻 Operating Systems

> **Weightage:** ~9% | **Avg Questions:** 6–8 | **Importance:** ⭐⭐⭐⭐⭐

---

## 📊 Overview

OS is very conceptual with some numerical questions. Scheduling algorithms, memory management, and synchronization are the most important areas. Questions often test deep understanding of mechanisms, not just definitions.

**Scoring Pattern:**
- 2–3 questions on Process Scheduling
- 1–2 questions on Memory Management (paging, segmentation)
- 1–2 questions on Synchronization / Deadlocks
- 1 question on File Systems
- 1 question on Threads / Process concepts

---

## ✅ Topic-wise Checklist

### ⚙️ Process Management
- [ ] Process definition, PCB structure
- [ ] Process states: new, ready, running, waiting, terminated
- [ ] Process creation: fork(), exec() in UNIX
- [ ] Context switching
- [ ] Interprocess communication: pipes, shared memory, message passing
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🧵 Threads
- [ ] User-level vs. kernel-level threads
- [ ] Thread models: many-to-one, one-to-one, many-to-many
- [ ] Benefits of threads over processes
- [ ] Thread libraries (pthreads concept)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📅 CPU Scheduling
- [ ] Scheduling criteria: CPU utilization, throughput, turnaround, waiting, response time
- [ ] FCFS: convoy effect, average waiting time calculation
- [ ] SJF (non-preemptive): optimal for average waiting time (provable)
- [ ] SRTF (preemptive SJF): optimal for average waiting time
- [ ] Priority Scheduling (preemptive and non-preemptive): starvation, aging
- [ ] Round Robin: quantum effect on performance, context switches
- [ ] Multilevel Queue / Multilevel Feedback Queue
- [ ] Gantt chart construction
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔄 Synchronization
- [ ] Race conditions, critical section problem
- [ ] Requirements: mutual exclusion, progress, bounded waiting
- [ ] Peterson's algorithm (2-process software solution)
- [ ] Hardware solutions: TestAndSet, Swap
- [ ] Semaphores: binary (mutex) and counting
- [ ] Classical problems: Producer-Consumer, Reader-Writer, Dining Philosophers
- [ ] Monitors: conditional variables, wait/signal
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 💀 Deadlocks
- [ ] Four necessary conditions: mutual exclusion, hold and wait, no preemption, circular wait
- [ ] Resource allocation graphs (RAG): deadlock detection
- [ ] Deadlock prevention: remove each necessary condition
- [ ] Deadlock avoidance: Banker's algorithm (safety algorithm, resource request algorithm)
- [ ] Deadlock detection: wait-for graph for single-instance resources
- [ ] Recovery: process termination, resource preemption
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🧠 Memory Management
- [ ] Logical vs. physical address space
- [ ] Swapping, contiguous allocation (first fit, best fit, worst fit)
- [ ] External vs. internal fragmentation
- [ ] Paging: page table, page table entry, TLB
- [ ] Effective memory access time (EAT) with TLB
- [ ] Multi-level paging (2-level, 3-level)
- [ ] Inverted page table
- [ ] Segmentation: segment table, protection
- [ ] Segmentation with paging
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔄 Virtual Memory
- [ ] Demand paging, page fault handling
- [ ] Pure demand paging vs. pre-paging
- [ ] Page replacement algorithms: FIFO (Belady's anomaly), Optimal, LRU, LFU, Clock/Second Chance
- [ ] Thrashing: working set model, page fault frequency
- [ ] Frame allocation: equal, proportional, global vs. local
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📁 File Systems
- [ ] File concept, attributes, operations
- [ ] File access methods: sequential, direct, indexed
- [ ] Directory structures: single-level, two-level, tree, acyclic graph, general graph
- [ ] File system implementation: boot block, superblock, FCB/inode
- [ ] Allocation methods: contiguous, linked, indexed
- [ ] Free space management: bit vector, linked list, grouping, counting
- [ ] Directory implementation: linear list, hash table
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 💾 I/O Systems
- [ ] I/O hardware: ports, buses, controllers
- [ ] I/O techniques: polling, interrupts, DMA
- [ ] Disk structure: platters, tracks, sectors, cylinders
- [ ] Disk scheduling: FCFS, SSTF, SCAN, C-SCAN, LOOK, C-LOOK
- [ ] Disk reliability, RAID levels (0, 1, 5, 6, 10)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Formulas

### Scheduling
```
Turnaround Time = Completion Time − Arrival Time
Waiting Time = Turnaround Time − Burst Time
Response Time = First CPU start − Arrival Time
```

### Memory (Paging)
```
Physical Address = Frame Number × Page Size + Offset
Logical Address = Page Number × Page Size + Offset
Page Number = Logical Address / Page Size  (integer division)
Offset = Logical Address mod Page Size

Number of pages = Logical address space / Page size
Number of frames = Physical memory / Page size

EAT (with TLB) = h × (TLB access time + Memory access time)
              + (1-h) × (TLB access time + 2 × Memory access time)
where h = TLB hit ratio
```

### Page Table Size
```
Page table size = Number of pages × PTE size
For 32-bit address space, 4KB pages: 2^20 pages × 4 bytes = 4MB page table
```

### Banker's Algorithm
```
Safety Algorithm:
  Work = Available; Finish[i] = false for all i
  Find i where Finish[i]=false AND Need[i] ≤ Work
  Work = Work + Allocation[i]; Finish[i] = true
  If all Finish[i] = true → SAFE STATE
```

### Disk Scheduling
```
SSTF: Service request closest to current head position
SCAN: Move in one direction, service all; reverse at end
C-SCAN: Move in one direction, service all; jump to start
```

---

## ⚠️ Common Mistakes

1. **FCFS vs. SRTF:** FCFS is non-preemptive; SJF/SRTF can be both; SRTF = preemptive SJF
2. **Belady's Anomaly:** Only FIFO exhibits this; LRU and Optimal do NOT
3. **Deadlock detection vs. avoidance:** Banker's = avoidance (prevents deadlock); wait-for graph = detection
4. **Page fault EAT:** Always include TLB miss penalty correctly
5. **2-level page table:** Outer page number + inner page number + offset — get bit allocation right
6. **Semaphore wait/signal order:** In producer-consumer, order matters for preventing deadlock
7. **Starvation in scheduling:** Priority scheduling can cause starvation; solution = aging
8. **RAID levels:** RAID 0 has no redundancy; RAID 1 mirrors; RAID 5 uses parity distributed

---

## 📈 PYQ Frequency Analysis

| Topic | Frequency |
|-------|-----------|
| CPU Scheduling (numerical) | Every year |
| Memory Management (paging) | Every year |
| Deadlock (Banker's algorithm) | Most years |
| Synchronization (semaphores) | Most years |
| Page replacement algorithms | Most years |
| File system allocation | Some years |

---

## 📚 Resources

- **Primary:** Operating System Concepts — Silberschatz, Galvin, Gagne
- **Video:** Sanchit Jain (YouTube) — GATE OS course
- **Video:** Neso Academy — clear explanations
- **Practice:** GATE Overflow OS tag
- **Quick ref:** GFG GATE OS notes

---

## 📅 PYQ Progress Tracker

- [ ] PYQs 2020–2026 solved
- [ ] PYQs 2015–2019 solved
- [ ] PYQs 2010–2014 solved

---

*Updated: ___ | Revision Count: ___*
