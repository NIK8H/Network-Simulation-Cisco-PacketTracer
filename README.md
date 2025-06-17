# Network-Simulation-Cisco-PacketTracer
This project demonstrates setting up Ethernet‑ or Serial‑linked routers/switches, subnet segmentation for site‑to‑site connectivity, static routing, and Local / Site‑to‑Site traffic testing (ping, traceroute), illustrating inter‑office and intra‑office network functionality.
# Corporate-Remote-Network-Simulation

A Cisco Packet Tracer simulation connecting a corporate office with three remote offices.  
This repo includes topology files, documentation, and testing procedures.

---

## 🛠️ Overview

- **Corporate office**  
  - 1 × PC  
  - 1 × Switch/Router gateway

- **3 Remote offices**  
  - Each with 1 × PC  
  - Each with its own Switch/Router

---

## 🌐 Topology Details

1. **Corporate ↔ Remote connections**  
   - The corporate switch/router links to each remote switch/router via dedicated interfaces.  
   - You can choose Ethernet or Serial (mirroring Cisco Packet Tracer examples).

2. **Subnet Scheme**  
   - **Corporate ↔ Remote links:** Unique subnet per link (e.g. 10.0.1.0/30, 10.0.2.0/30, etc.)  
   - **Internal LANs:**  
     - Corporate LAN: 192.168.0.0/24  
     - Remote 1 LAN: 192.168.1.0/24  
     - Remote 2 LAN: 192.168.2.0/24  
     - Remote 3 LAN: 192.168.3.0/24  

3. **Routing**  
   - Static routes on corporate router to reach each remote LAN via appropriate interface  
   - Static routes on remote routers to reach corp LAN and other remotes via corporate router

---

## 💻 Files Included

| File | Description |
|------|-------------|
| `Corporate-Remote-Network-Simulation.pkt` | Cisco Packet Tracer topology file |
| `README.md` | This documentation |
| `subnet_plan.txt` | Subnet allocations and addressing details |
| `traffic_test_results.txt` | Results and observations from traffic tests |

---

## 🧪 Traffic Testing & Observations

To validate connectivity:

1. **Local LAN pings**  
   - From each PC to its router and back (e.g. PC1 → Remote1 Router → PC1)

2. **Site-to-Site pings**  
   - PC at Corporate ↔ PC at each Remote  
   - PC at one Remote ↔ PC at another Remote

3. **Traceroute**  
   - Verify path hops go through corporate router as appropriate

4. **Interface monitoring**  
   - Observed interface counters and link status to confirm traffic flow

Document these in `traffic_test_results.txt` with:
- Command outputs (`ping`, `traceroute`, `show ip route`)
- Observations (e.g. latency, hop counts, success rates)

---

## 🚀 How to Use

1. Install Cisco Packet Tracer (version X.X or higher)  
2. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Corporate-Remote-Network-Simulation.git
   cd Corporate-Remote-Network-Simulation
