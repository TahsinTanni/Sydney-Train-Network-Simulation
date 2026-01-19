# Sydney Train Network Simulation

## Project Overview
This project is a **Cisco Packet Tracer–based simulation** of the Sydney Trains network, developed as part of the **CSE421 Computer Networks** course.  
The goal of this project is to design a **reliable, scalable, and cost-efficient metropolitan network** connecting major Sydney railway stations while following real-world networking constraints.

The network supports internal station operations, staff devices, public services, and backend servers using proper **VLSM subnetting, routing strategies, and centralized services**.

---

## Stations Included
The following six major Sydney Train stations are interconnected:

- **Central Station** – Core Hub
- **Town Hall**
- **Wynyard**
- **Redfern**
- **Burwood**
- **Parramatta**

---

## Network Design Highlights
- Central Station acts as the **core hub**
- **Redundant backup link** between Central and Wynyard
- **VLSM-based IP addressing** to minimize IP wastage
- **Static Routing** implemented at:
  - Central
  - Town Hall
  - Wynyard
- **Dynamic Routing (RIP v2)** implemented at:
  - Redfern
  - Burwood
  - Parramatta
- **No default routes** used anywhere in the network
- **Full end-to-end connectivity** achieved across all stations

---

## Network Services
The following backend services are configured:

| Service | Location |
|------|--------|
| DHCP Server | Central Station |
| DNS Server | Central Station |
| Web Server | Central Station |
| Email Server | Parramatta |

###  DNS Requirement
- URL: `www.sydneyrail.net`
- Resolves to the web server at Central Station
- Displays the message:  
  **“Welcome to Sydney Trains!”**

---

## IP Addressing & Subnetting
- Major network address: `192.168.0.0/16`
- **VLSM (Variable Length Subnet Masking)** applied for:
  - Station LAN networks
  - WAN point-to-point links
- WAN links use `/30` subnets
- LAN subnets are allocated based on user requirements

Detailed **VLSM tree diagrams** and **IP addressing tables** are included in the repository documentation.

---

## Technologies Used
- Cisco Packet Tracer
- VLSM Subnetting
- Static Routing
- RIP version 2
- DHCP Relay
- DNS Configuration
- Web Server Configuration
- Email Server Configuration


---

## ▶️ How to Run the Project
1. Open **Cisco Packet Tracer**
2. Load the `.pkt` file from the `packet-tracer/` directory
3. Allow routing tables to converge
4. Verify:
   - Ping between all stations
   - DHCP IP assignment to end devices
   - DNS resolution of `www.sydneyrail.net`
   - Web and Email server functionality

---

## Assumptions
- All router interfaces are assigned **static IP addresses**
- End devices receive IP addresses via **centralized DHCP**
- LAN interfaces are configured as **passive interfaces** in RIP
- Backup links use **floating static routes**
- All servers are manually configured with **static IPs**

---

## Final Outcome
The completed network successfully demonstrates:
- Efficient IP utilization using VLSM
- Redundancy and fault tolerance
- Centralized service management
- Full connectivity across all Sydney Train stations

---

*This project simulates real-world metropolitan rail communication networks and demonstrates practical applications of subnetting, routing, redundancy, and network services.*


