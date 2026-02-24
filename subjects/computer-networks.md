# 🌐 Computer Networks

> **Weightage:** ~8% | **Avg Questions:** 5–7 | **Importance:** ⭐⭐⭐⭐⭐

---

## 📊 Overview

CN is a formula-heavy subject with well-defined question types. The OSI/TCP-IP model structure is the backbone. Routing algorithms, IP addressing, and data link layer protocols are most commonly tested.

**Scoring Pattern:**
- 1–2 questions on IP Addressing/Subnetting
- 1–2 questions on Data Link (CSMA/CD, sliding window)
- 1–2 questions on Routing Protocols/algorithms
- 1 question on Transport Layer (TCP/UDP)
- 1 question on Application Layer / DNS / HTTP

---

## ✅ Topic-wise Checklist

### 🏗️ OSI and TCP/IP Models
- [ ] OSI 7 layers: functions of each layer
- [ ] TCP/IP 5-layer model vs. OSI model
- [ ] PDU at each layer: bit, frame, packet, segment, data
- [ ] Protocols at each layer
- [ ] Encapsulation and decapsulation
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📡 Physical Layer
- [ ] Transmission media: twisted pair, coaxial, fiber optic, wireless
- [ ] Bandwidth, bit rate, baud rate
- [ ] Nyquist theorem (noiseless): Max bit rate = 2B log₂ V
- [ ] Shannon's theorem (noisy): Max bit rate = B log₂(1 + SNR)
- [ ] Transmission time vs. propagation delay
- [ ] Multiplexing: FDM, TDM, WDM
- [ ] Switching: circuit, packet, message
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔗 Data Link Layer
- [ ] Framing: byte count, byte stuffing, bit stuffing
- [ ] Error detection: parity, CRC (cyclic redundancy check), checksum
- [ ] Error correction: Hamming code
- [ ] Flow control: stop-and-wait, sliding window
- [ ] ARQ protocols: Stop-and-Wait ARQ, Go-Back-N ARQ, Selective Repeat ARQ
- [ ] Efficiency calculations for sliding window protocols
- [ ] CSMA/CD: used in Ethernet, collision detection
- [ ] CSMA/CA: used in WiFi, collision avoidance
- [ ] MAC addresses, ARP
- [ ] Ethernet frame format
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🌍 Network Layer
- [ ] IP addressing: IPv4 (32-bit), classes (A, B, C, D, E)
- [ ] Subnetting: subnet mask, CIDR notation, network/host bits
- [ ] Supernetting / CIDR aggregation
- [ ] IPv6: 128-bit addresses, notation, motivation
- [ ] IP datagram format: header fields, fragmentation, TTL
- [ ] IP fragmentation and reassembly
- [ ] ICMP: ping, traceroute, error messages
- [ ] NAT: Network Address Translation
- [ ] Routing: static vs. dynamic
- [ ] Distance Vector Routing (DVR): Bellman-Ford, count-to-infinity
- [ ] Link State Routing (LSR): Dijkstra's, flooding
- [ ] RIP (DVR-based), OSPF (LSR-based), BGP (path vector)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🚀 Transport Layer
- [ ] TCP vs. UDP: connection-oriented, reliable, ordered
- [ ] TCP: 3-way handshake, 4-way termination
- [ ] TCP segment format: sequence numbers, acknowledgment
- [ ] TCP flow control: receive window, sliding window
- [ ] TCP congestion control: slow start, congestion avoidance, fast retransmit, fast recovery
- [ ] UDP: connectionless, datagrams, checksum
- [ ] Port numbers: well-known ports
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🌏 Application Layer
- [ ] DNS: domain name system, hierarchy, resolution (recursive, iterative)
- [ ] HTTP/HTTPS: request methods (GET, POST), status codes, persistent vs. non-persistent
- [ ] FTP, SMTP, IMAP, POP3
- [ ] DHCP: IP assignment, lease, discover/offer/request/ack
- [ ] SNMP (overview)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔐 Network Security (Overview)
- [ ] Symmetric encryption (DES, AES), asymmetric (RSA)
- [ ] Digital signatures, certificates
- [ ] SSL/TLS concept
- [ ] Firewalls, VPNs (overview)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Formulas

### Physical Layer
```
Nyquist: Max bit rate = 2 × B × log₂(V)  [B = bandwidth, V = signal levels]
Shannon: Max bit rate = B × log₂(1 + S/N)
Transmission time = L / R  [L = packet size bits, R = link rate bps]
Propagation delay = d / s  [d = distance, s = speed of signal]
End-to-End delay = Transmission time + Propagation delay
```

### Sliding Window (ARQ)
```
Efficiency of Stop-and-Wait = 1 / (1 + 2a)  [a = propagation delay / transmission time]
Window size for 100% efficiency = 1 + 2a

Go-Back-N:
  Sender window = 2^n - 1  (n = sequence number bits)
  Receiver window = 1
  Efficiency = W / (1 + 2a)  if W ≤ 1 + 2a

Selective Repeat:
  Sender window = Receiver window = 2^(n-1)
  Efficiency = W / (1 + 2a)  if W ≤ 1 + 2a
```

### IP Addressing
```
IPv4: 32 bits = 4 octets
Class A: 0.x.x.x – 127.x.x.x  (default mask /8)
Class B: 128.x.x.x – 191.x.x.x  (default mask /16)
Class C: 192.x.x.x – 223.x.x.x  (default mask /24)
Class D: 224–239 (multicast)
Class E: 240–255 (reserved)

Number of hosts per subnet = 2^h - 2  [h = host bits]
Number of subnets = 2^s  [s = subnet bits]
```

### Hamming Code
```
Parity bits needed: 2^p ≥ m + p + 1  [m = data bits, p = parity bits]
Parity bit positions: 1, 2, 4, 8, 16, ... (powers of 2)
```

---

## ⚠️ Common Mistakes

1. **Efficiency formula:** Use correct formula for Go-Back-N vs. Selective Repeat
2. **Subnetting:** Always subtract 2 for network and broadcast addresses in host count
3. **TCP sequence numbers:** Sequence numbers are byte-based, not segment-based
4. **Count-to-infinity:** Only in DVR (RIP), not in LSR (OSPF)
5. **CSMA/CD minimum frame size:** Must be large enough for collision to be detected (2 × propagation delay × bandwidth)
6. **CRC remainder:** CRC gives the remainder, not the quotient
7. **IP fragmentation:** Each fragment gets the same IP header except offset and flags
8. **ARP vs. RARP:** ARP maps IP → MAC; RARP maps MAC → IP (mostly deprecated)

---

## 📈 PYQ Frequency Analysis

| Topic | Frequency |
|-------|-----------|
| Sliding Window (ARQ efficiency) | Every year |
| IP Addressing / Subnetting | Every year |
| Routing protocols | Most years |
| TCP flow/congestion control | Most years |
| CRC / error detection | Most years |
| OSI layer functions | Some years |

---

## 📚 Resources

- **Primary:** Data Communications and Networking — Forouzan
- **Alternate:** Computer Networks — Tanenbaum
- **Video:** Ravindrababu Ravula — CN lectures (YouTube)
- **Video:** Neso Academy — clear formula explanations
- **Practice:** GATE Overflow CN tag

---

## 📅 PYQ Progress Tracker

- [ ] PYQs 2020–2026 solved
- [ ] PYQs 2015–2019 solved
- [ ] PYQs 2010–2014 solved

---

*Updated: ___ | Revision Count: ___*
