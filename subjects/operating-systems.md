# 🖥️ Operating Systems

![Weightage](https://img.shields.io/badge/Weightage-8–10%20marks-red)
![Priority](https://img.shields.io/badge/Priority-Very%20High-red)

---

## 📋 Topic Checklist

### 🔷 Processes & Threads
- [ ] Process concept, PCB (Process Control Block)
- [ ] Process states: new, ready, running, waiting, terminated
- [ ] Process creation and termination (fork, exec, wait)
- [ ] Context switching
- [ ] Threads — user-level vs kernel-level
- [ ] Multithreading models: Many-to-One, One-to-One, Many-to-Many
- [ ] Inter-process communication: shared memory, message passing

### 🔷 CPU Scheduling
- [ ] Scheduling criteria: CPU utilization, throughput, turnaround time, waiting time, response time
- [ ] FCFS — non-preemptive, convoy effect
- [ ] SJF — non-preemptive and preemptive (SRTF)
- [ ] Priority Scheduling — preemptive and non-preemptive, starvation
- [ ] Round Robin — time quantum impact, relation to FCFS/SRTF
- [ ] Multilevel Queue Scheduling
- [ ] Multilevel Feedback Queue Scheduling
- [ ] Gantt chart drawing and calculations

### 🔷 Process Synchronization
- [ ] Race condition and critical section problem
- [ ] Requirements: mutual exclusion, progress, bounded waiting
- [ ] Peterson's solution (software)
- [ ] Hardware solutions: test-and-set, compare-and-swap
- [ ] Semaphores — binary (mutex) and counting
- [ ] Monitors — condition variables, wait/signal
- [ ] Classic synchronization problems:
  - [ ] Bounded Buffer (Producer-Consumer)
  - [ ] Readers-Writers (first, second variations)
  - [ ] Dining Philosophers

### 🔷 Deadlocks
- [ ] Conditions for deadlock: mutual exclusion, hold & wait, no preemption, circular wait
- [ ] Resource allocation graph — safe state detection
- [ ] Deadlock prevention — negate each condition
- [ ] Deadlock avoidance — Banker's Algorithm (safety + resource request)
- [ ] Deadlock detection — resource allocation graph + wait-for graph
- [ ] Recovery from deadlock

### 🔷 Memory Management
- [ ] Logical vs physical address space
- [ ] Contiguous allocation: fixed partition, variable partition
- [ ] Fragmentation — internal vs external
- [ ] Paging — page table, page number + offset
- [ ] TLB (Translation Lookaside Buffer) — effective access time calculation
- [ ] Segmentation — segment table, segment + offset
- [ ] Segmentation with paging

### 🔷 Virtual Memory
- [ ] Demand paging — page fault handling
- [ ] Effective access time with page faults
- [ ] Page replacement algorithms:
  - [ ] FIFO — Belady's anomaly
  - [ ] LRU — stack property (no Belady's anomaly)
  - [ ] Optimal (OPT/MIN) — theoretical, no Belady's anomaly
  - [ ] Clock (second chance) algorithm
- [ ] Thrashing — causes and solutions
- [ ] Working set model

### 🔷 File Systems
- [ ] File attributes, operations, types
- [ ] File allocation methods:
  - [ ] Contiguous allocation — fast access, external fragmentation
  - [ ] Linked allocation — no fragmentation, poor random access
  - [ ] Indexed allocation — FAT, inode structure
- [ ] Directory structure: single-level, two-level, tree-structured, acyclic graph
- [ ] Disk scheduling algorithms:
  - [ ] FCFS
  - [ ] SSTF (Shortest Seek Time First)
  - [ ] SCAN (Elevator)
  - [ ] C-SCAN
  - [ ] LOOK, C-LOOK

### 🔷 I/O Systems
- [ ] I/O hardware: device controllers, device drivers
- [ ] I/O techniques: polling, interrupts, DMA
- [ ] Buffering, caching, spooling

---

## ⚡ Key Formulas

### CPU Scheduling
```
Turnaround Time = Completion Time − Arrival Time
Waiting Time    = Turnaround Time − Burst Time
Response Time   = First CPU allocation − Arrival Time
CPU Utilization = (Total CPU burst time) / (Total time) × 100%
```

### Memory — Effective Access Time (with TLB)
```
EAT = h × (TLB time + Memory time) + (1-h) × (TLB time + 2 × Memory time)

Where h = TLB hit ratio
```

### Effective Access Time (with Page Faults)
```
EAT = (1-p) × memory_access_time + p × page_fault_time

Where p = page fault rate
```

### Banker's Algorithm
```
Need[i][j] = Max[i][j] − Allocation[i][j]

Safety condition: Work >= Need[i] (for some process i)
                  Work = Work + Allocation[i]
```

### Disk Scheduling — Seek Time
```
SSTF: Always go to closest request from current head position
SCAN: Move in one direction, then reverse at end
C-SCAN: Move in one direction, jump to start, continue same direction
```

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| Belady's anomaly in all algorithms | Only FIFO has Belady's anomaly, not LRU or OPT |
| SJF is always better | SRTF minimizes avg waiting, but SJF may cause starvation |
| Semaphore = mutex | Binary semaphore ≈ mutex, but counting semaphore is different |
| Paging eliminates all fragmentation | Paging eliminates external fragmentation, has internal fragmentation |
| Wait-for graph used for avoidance | Wait-for graph is for detection; Banker's is for avoidance |
| SCAN reaches disk end always | LOOK version only goes to last request, not disk end |

---

## 📊 PYQ Frequency Analysis (2015–2024)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| CPU Scheduling (Gantt charts) | Very High (every year) | 2–4 |
| Page Replacement | Very High | 2–3 |
| Deadlock / Banker's Algorithm | High | 2–3 |
| Process Synchronization | High | 1–2 |
| Memory Management / TLB | High | 1–2 |
| File System / Disk Scheduling | Medium | 1–2 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| CPU Scheduling | ☐ Low / ☐ Med / ☐ High | |
| Deadlock | ☐ Low / ☐ Med / ☐ High | |
| Memory & Paging | ☐ Low / ☐ Med / ☐ High | |
| Page Replacement | ☐ Low / ☐ Med / ☐ High | |
| Synchronization | ☐ Low / ☐ Med / ☐ High | |
| File Systems | ☐ Low / ☐ Med / ☐ High | |
