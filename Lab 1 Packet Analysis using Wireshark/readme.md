## 1. Project Summary

In this lab assessment for the SCSR1213 Network Communications course, I was introduced to **Wireshark**, a powerful packet sniffing and analysis tool. The core objective was to observe the sequence of messages exchanged between protocol entities and dive deep into the operations of Application Layer protocols, specifically HTTP and DNS.

The lab was divided into practical network tracing activities:
*   **HTTP Tracing (Basic & Conditional GETs):** I analyzed `pcapng` trace files to inspect basic HTTP GET requests and server responses, identifying the client and server IP addresses, byte lengths, and status codes (such as `200 OK` and `404 Not Found`). I also explored Conditional GETs, observing how an `IF-MODIFIED-SINCE` header allows the server to return a `304 Not Modified` status, instructing the browser to use its cached version. Finally, I analyzed how a single webpage with embedded objects (like `.gif` and `.jpg` images) triggers multiple HTTP GET requests.
*   **DNS Tracing & Command Line Tools:** I utilized the Windows Command Prompt to run `nslookup` (querying top-level and non-authoritative DNS servers for IP addresses) and `ipconfig /all` (to view local TCP/IP configurations). Using Wireshark, I traced DNS packets, verifying that DNS operates over the User Datagram Protocol (UDP) using Port 53. I extracted detailed information from "Type A" DNS queries and responses, such as Time-to-Live (TTL) values and Host Addresses.

---

## 2. Reflection

### What I Have Learnt
* Before this, "HTTP" and "DNS" were just acronyms I saw in my web browser. By physically opening the packet envelopes in Wireshark, I was able to see the raw hexadecimal and ASCII data. 
* I learned that DNS acts as the internet's phonebook, translating human-readable domain names into machine-readable IP addresses using UDP Port 53. 
* This lab could be significantly improved by having students perform **live packet sniffing**. Instead of reading pre-recorded data, actively capturing packets while browsing a live, unencrypted HTTP website in real-time would provide a much more dynamic and realistic understanding of network traffic congestion and packet capturing.