# Cybersecurity Tools Overview

Cybersecurity tools are used to analyze networks, identify vulnerabilities, monitor traffic, and test system security. These tools help security professionals understand how attackers operate and how systems can be defended.

---

## Wireshark

Wireshark is a network packet analyzer used to capture and inspect network traffic in real time.

### Purpose
- Monitor network traffic
- Analyze packets at protocol level
- Detect suspicious activity

### Key Features
- Live packet capture
- Protocol filtering
- Packet inspection
- Supports hundreds of protocols

### Common Use Cases
- Analyzing ICMP, TCP, UDP packets
- Troubleshooting network issues
- Detecting malware communication

### Basic Usage
- Select active network interface
- Start packet capture
- Apply filters (e.g., `icmp`, `http`)

---

## Nmap (Network Mapper)

Nmap is a powerful network scanning tool used for discovering hosts and services on a network.

### Purpose
- Identify live hosts
- Detect open ports
- Identify running services

### Key Features
- Port scanning
- Service version detection
- OS fingerprinting

### Common Use Cases
- Network reconnaissance
- Vulnerability assessment
- Security auditing

### Basic Commands
nmap target-ip  
nmap -sS target-ip  
nmap -sV target-ip  

---

## Burp Suite

Burp Suite is a web application security testing tool used to analyze HTTP and HTTPS traffic.

### Purpose
- Intercept and analyze web traffic
- Test web application vulnerabilities

### Key Features
- Intercepting proxy
- Request/response modification
- Repeater and Intruder tools

### Common Use Cases
- Testing login forms
- Identifying SQL injection and XSS
- Session analysis

### Basic Usage
- Configure browser proxy
- Enable intercept
- Analyze HTTP requests

---

## Netcat

Netcat is a versatile networking utility used for reading and writing data across network connections.

### Purpose
- Debug network services
- Create simple client-server connections

### Key Features
- Port listening
- File transfer
- Banner grabbing

### Common Use Cases
- Backdoor testing
- Port connectivity testing
- Reverse shells (ethical labs only)

### Basic Commands
nc -lvnp 4444  
nc target-ip 4444  

---

## OpenSSL

OpenSSL is a cryptographic toolkit used to implement SSL/TLS and perform encryption operations.

### Purpose
- Encrypt and decrypt files
- Generate hashes
- Test SSL/TLS connections

### Key Features
- Supports multiple encryption algorithms
- Certificate generation
- Secure communications

### Common Use Cases
- Encrypting sensitive data
- Verifying file integrity
- SSL certificate analysis

### Basic Commands
md5sum file.txt  
sha256sum file.txt  
openssl enc -aes-256-cbc -in file.txt -out encrypted.txt  
openssl enc -aes-256-cbc -d -in encrypted.txt -out decrypted.txt  

---

## Summary

These tools form the core toolkit for ethical hacking and cybersecurity analysis. Understanding their usage and purpose is essential for identifying vulnerabilities, securing networks, and conducting ethical security assessments.
