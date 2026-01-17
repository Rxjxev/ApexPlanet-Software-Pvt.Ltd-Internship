# Port and Service Scanning

Port scanning is a technique used to identify open ports and services
running on a target system. Open ports represent potential entry points
that attackers may exploit.

Understanding exposed services is critical for both attackers and defenders.

---

## Why Port Scanning Is Important

- Identifies exposed network services
- Helps assess attack surface
- Supports vulnerability assessment
- Validates firewall effectiveness

---

## TCP Scanning

### SYN Scan (Stealth Scan)
nmap -sS 10.0.0.5

Performs a half-open scan that does not complete the TCP handshake.

### TCP Connect Scan
nmap -sT -p- 10.0.0.5

Scans all TCP ports using full connections.

---

## UDP Scanning
nmap -sU 10.0.0.5

Identifies services running over UDP, which are often overlooked.

---

## Service Version Detection
nmap -sV 10.0.0.5

Identifies software versions running on open ports.

---

## OS Detection
nmap -O 10.0.0.5

Attempts to identify the operating system based on network behavior.

---

## Output Details
- Open ports
- Running services
- Service versions
- Operating system fingerprint

---

## Findings
Port and service scanning reveals exposed services and software versions,
helping prioritize vulnerability assessment and security hardening.

Reducing unnecessary open ports improves overall system security.
