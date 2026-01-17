# Packet Analysis with Wireshark

Wireshark is a powerful network packet analyzer used to capture and inspect
network traffic at a very detailed level. It allows security analysts and
network administrators to view packets in real time and analyze protocol behavior.

Packet analysis is essential for detecting network anomalies, insecure protocols,
malicious traffic, and troubleshooting connectivity issues.

---

## Why Packet Analysis Is Important

- Detects unencrypted credentials
- Identifies suspicious network behavior
- Helps investigate network attacks
- Supports forensic investigations

---

## Traffic Types Analyzed
- ICMP
- HTTP
- FTP
- DNS
- TCP Handshake

Each protocol provides different insights into network communication.

---

## Capture Process
1. Select network interface
2. Start capture
3. Generate traffic
4. Stop and analyze packets

This process ensures accurate packet inspection.

---

## Example Commands

tcpdump -i eth0 icmp  

Captures ICMP packets such as ping requests and replies.

tshark -i eth0 -f "port 53"  

Captures DNS traffic.

tshark -r traffic.pcap -Y "http.request"  

Filters HTTP requests from a saved packet capture file.

---

## Filters
icmp  
http  
dns  
ftp  

Filters help isolate specific traffic for focused analysis.

---

## Attack Simulation
- SYN flood analysis using hping3 (lab only)

Packet analysis can be used to identify abnormal traffic patterns
generated during DoS/DDoS attacks.

---

## Findings
Packet analysis provides deep visibility into network behavior, highlights
unencrypted traffic, and aids in network troubleshooting and forensic analysis.

Understanding packet-level communication is a core skill in cybersecurity.
