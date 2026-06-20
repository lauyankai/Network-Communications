## 1. Project Summary
In this lab assessment for the Network Communications course, I utilized Cisco Packet Tracer to explore the **Address Resolution Protocol (ARP)** and physical switching operations. The lab was divided into a core routing/switching analysis and an additional wireless configuration activity:

*   **Part 1 & 2: ARP and Switch MAC Tables:** The primary objective was to observe how network devices dynamically map IP addresses to physical MAC addresses. I began by inspecting the routers (RTA, RTB) and switches (SWA, SWB, SWC) using the `show arp` and `show mac-address-table` commands via the Command Line Interface (CLI). Initially, checking the PCs using the `arp -a` command revealed no ARP entries. However, after generating network traffic by executing `ping` commands between the PCs (e.g., from PCC to PCB and PCD), I observed the ARP tables automatically populating as the devices received ARP requests. I also verified that switches dynamically learn and store MAC addresses to identify the destination for network nodes.
*   **Part 3: Wireless LAN Access:** In the final section, I completed a Packet Tracer activity focused on configuring wireless connectivity. I configured a client PC (PC3) to connect to a wireless router by manually entering the SSID (`WRS_LAN`), enabling automatic network settings via DHCP, and securing the connection using WPA2-Personal encryption with the passphrase `cisco123`. 

---

## 2. Reflection

### What I Have Learnt
* Before this activity, I assumed that devices inherently knew the physical addresses of everything else on the subnet. However, seeing the `arp -a` command return "No ARP Entries Found" before a ping was initiated proved that Address Resolution Protocol operates strictly on an as-needed, dynamic basis. 
* Exploring the `show mac-address-table` command demonstrated exactly how switches intelligently forward frames to specific ports based on MAC addresses, rather than blindly broadcasting data like a legacy network hub.
* While we could see that the ARP tables populated *after* the `ping` command, physically capturing and inspecting the raw ARP Broadcast ("Who has this IP? Tell this MAC") in Wireshark would provide a much deeper understanding of the exact packet structure used during address resolution.