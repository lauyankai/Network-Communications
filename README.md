# SECR1213: Network Communications

## 1. Course Overview
Welcome to my GitHub E-Portfolio for the **SECR1213 - Network Communications** course. This repository showcases my practical skills in network engineering, packet analysis, and network topology simulation. 

Throughout this course, I gained hands-on experience exploring how data traverses the internet across different layers of the OSI model. I utilized **Wireshark** to sniff and analyze Application Layer protocols (like HTTP and DNS). Furthermore, I extensively used **Cisco Packet Tracer** to simulate network environments, allowing me to configure Transport Layer protocols (TCP/UDP), design Network Layer IP addressing with VLSM subnetting, implement dynamic routing (RIP), and explore Data Link Layer switching operations and ARP mapping.

## 2. Team Members & Collaborators
While some lab assessments were conducted individually, certain simulation activities within this repository were completed collaboratively. I would like to acknowledge my teammate:
*   **Lau Yan Kai (A23CS0098)** 
*   **Elijah She Yu Sheng (A23CS0073)**

---

## 3. Repository Contents (Labs)

### 🔍 [Lab 1: Packet Analysis using Wireshark]
*   **Topic:** Application Layer Protocols, Packet Sniffing, HTTP, and DNS.
*   **Summary:** Introduced to Wireshark as a packet sniffing tool to observe real-time message exchanges. Analyzed basic and conditional HTTP GET requests (exploring `304 Not Modified` status codes for caching). Utilized Windows CLI tools like `nslookup` and `ipconfig` to query authoritative and non-authoritative DNS servers, and traced how DNS queries are executed over UDP Port 53.

### 🛠️ [Lab 2: Packet Tracer Simulation – TCP and UDP Communications]
*   **Topic:** Transport Layer, Connection-Oriented vs. Stateless Protocols.
*   **Summary:** Used Cisco Packet Tracer to simulate network traffic (HTTP, FTP, DNS, and E-Mail) moving from multiple clients to a central MultiServer. Inspected Protocol Data Unit (PDU) envelopes to verify the reliability of TCP (tracking the `SYN`, `SYN+ACK`, and `ACK` flags during the three-way handshake). Contrasted this by analyzing the stateless, connectionless nature of UDP packets, and monitored active TCP sessions using the `netstat` command.

### 🌐 [Lab 3: IP Addressing and Routing Protocols]
*   **Topic:** Network Layer, Subnetting (VLSM), and Dynamic Routing.
*   **Summary:** Designed a network topology by calculating VLSM subnet masks and usable host ranges for multiple LANs and serial connections. Configured routers using the Command Line Interface (CLI) to implement the **Routing Information Protocol (RIP version 2)**, utilizing the `network` command to dynamically advertise connected subnets. Successfully verified end-to-end connectivity across the updated network topology using `ping` tests.

### 📡 [Lab 4: Exploration of ARP, Switch Tables, and Wireless LAN]
*   **Topic:** Data Link Layer, Address Resolution Protocol (ARP), and Wireless Security.
*   **Summary:** Explored how network devices dynamically map IP addresses to physical MAC addresses. Observed empty ARP tables dynamically populating only *after* traffic was generated using the `ping` command. Investigated how switches utilize MAC address tables (`show mac-address-table`) to forward frames intelligently. Finally, configured a wireless client PC to securely connect to a Wireless LAN using DHCP and WPA2-Personal encryption.