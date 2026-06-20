## 1. Project Summary
In this lab assessment for the SECR1213 Network Communications course, my teammate and I utilized Cisco Packet Tracer to simulate and deeply analyze the functionality of the **Transmission Control Protocol (TCP)** and the **User Datagram Protocol (UDP)**. 

The lab was divided into two main phases. In **Part 1**, we generated various types of network traffic from multiple client PCs to a centralized "MultiServer". We used the command line and built-in tools to generate:
*   **HTTP Traffic:** Accessing a web server via a browser.
*   **FTP Traffic:** Initiating a file transfer protocol connection.
*   **DNS Traffic:** Using `nslookup` to query domain names.
*   **Email Traffic:** Sending an email using SMTP and POP3.

In **Part 2**, we switched to Simulation Mode to inspect the Protocol Data Unit (PDU) envelopes as they travelled across the switch. We examined the exact transport layer behaviours:
*   **TCP Reliability & Handshakes:** By inspecting the HTTP (Port 80), FTP (Port 21), and Email (Port 25/110) packets, we verified that TCP is a reliable, connection-oriented protocol. We tracked the sequence numbers, acknowledgment numbers (ACK), and the specific flags used to establish connections (observing the transition from `SYN` to `SYN+ACK` and `ACK` during the three-way handshake).
*   **UDP Statelessness:** By inspecting the DNS (Port 53) packets, we verified that UDP is connectionless and unreliable, noting the complete absence of sequence and acknowledgment numbers.
*   **Active Sessions:** Finally, we utilized the `netstat` command to view live network connections, identifying sessions stuck in the `ESTABLISHED` state (such as the FTP client waiting for a username input).

---

## 2. Reflection

### What I Have Learnt
* Before this activity, I understood the "TCP three-way handshake" conceptually, but tracking the `SYN` and `ACK` flags changing dynamically inside the PDU envelopes in Packet Tracer solidified my understanding. I also gained a much clearer picture of port multiplexing.
* I observed how a single server could simultaneously handle web traffic on Port 80, file transfers on Port 21, and emails on Port 25, simply by organizing the data streams via destination ports.
* A great improvement to this lab would be combining this simulation with a live Wireshark capture of the FTP traffic. Because FTP transmits data in plaintext, analyzing a live capture would allow students to physically see the usernames and passwords being sent over the network, providing a powerful lesson on why modern networks require encrypted protocols like SFTP or HTTPS.