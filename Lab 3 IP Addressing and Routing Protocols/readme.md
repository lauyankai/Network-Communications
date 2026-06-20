## 1. Project Summary
In this lab assessment for the Network Communications course, I focused on the network layer, specifically mastering **Subnetting (VLSM)** and configuring dynamic routing using the **Routing Information Protocol (RIP)**. The lab was structured into three main practical networking tasks using Cisco Packet Tracer:

*   **Task 1: IP Addressing:** Given a base network address of `172.18.110.0/23`, I calculated the subnet masks, usable hosts, and prefix lengths (such as `/26`, `/27`, and `/30`) for four different Local Area Networks (LANs) and three Point-to-Point serial connections linking the central routers (JERUNG, SHARK, and TIBURON). 
*   **Task 2: Routing Table Analysis:** I inspected the initial routing tables using both the Packet Tracer GUI and the `show ip route` CLI command. I conducted preliminary `ping` tests, observing that while PCs on the same subnet could communicate, cross-network communication (e.g., PC1 to PC4) failed with a "Destination host unreachable" error because the routers lacked the necessary routing paths.
*   **Task 3: Routing Configuration & Network Updates:** I configured RIP version 2 on all three routers. By utilizing the `network` command, I instructed the routers to dynamically advertise their connected subnets and exchange routing information. Finally, I simulated a network change by altering TIBURON's interface IP to `192.168.1.1/24`, updating the corresponding PC gateway, and successfully verifying full end-to-end connectivity across the entire updated topology.

---

## 2. Reflection

### What I Have Learnt

* Calculating the VLSM prefixes (`/27`, `/30`) manually taught me exactly how IP addresses are conserved in wide-area links compared to standard LANs. Furthermore, configuring RIP showed me the power of dynamic routing.
* Instead of manually programming every single path into a router, RIP allows the routers to automatically map out the network and adapt to changes. 
* I also learned the critical importance of configuring the correct Default Gateway on client PCs, without it, even the best-configured router cannot help a PC send data outside its local subnet.
* A highly beneficial improvement to this lab would be to configure **OSPF (Open Shortest Path First)** instead. Learning OSPF would introduce students to link-state routing and area concepts, which are much more relevant to current industry networking standards.
