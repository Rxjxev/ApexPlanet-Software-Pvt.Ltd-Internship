# Networking Basics

Networking is the foundation of cybersecurity. It enables communication between computers, servers, and devices using defined rules called protocols. Understanding networking is essential to identify attacks, secure data transmission, and analyze traffic.

---

## OSI Model

The OSI (Open Systems Interconnection) model divides network communication into seven layers. Each layer has a specific function and helps in troubleshooting network issues.

### 1. Physical Layer
- Responsible for physical transmission of data
- Includes cables, connectors, signals, voltage levels
- Deals with bits (0s and 1s)

**Example:** Ethernet cables, fiber optics

---

### 2. Data Link Layer
- Ensures reliable data transfer between directly connected nodes
- Uses MAC (Media Access Control) addresses
- Handles error detection

**Devices:** Switches  
**Protocols:** Ethernet, ARP

---

### 3. Network Layer
- Handles logical addressing and routing
- Determines best path for data transfer

**Devices:** Routers  
**Protocols:** IP, ICMP

---

### 4. Transport Layer
- Ensures end-to-end communication
- Manages data segmentation and reassembly
- Uses port numbers

**Protocols:** TCP, UDP

---

### 5. Session Layer
- Establishes, manages, and terminates communication sessions
- Controls session checkpoints

**Example:** Login sessions

---

### 6. Presentation Layer
- Translates data formats
- Handles encryption and compression

**Example:** SSL/TLS encryption

---

### 7. Application Layer
- Provides network services directly to user applications

**Protocols:** HTTP, FTP, SMTP, DNS

---

## TCP vs UDP

### TCP (Transmission Control Protocol)
TCP is a reliable, connection-oriented protocol.

**Characteristics:**
- Three-way handshake
- Error detection and correction
- Guaranteed data delivery
- Slower but accurate

**Used in:**
- HTTP/HTTPS
- FTP
- Email services

---

### UDP (User Datagram Protocol)
UDP is a fast, connectionless protocol.

**Characteristics:**
- No handshake
- No error correction
- Faster transmission

**Used in:**
- DNS
- Online gaming
- Video streaming

---

## DNS (Domain Name System)

DNS translates human-readable domain names into IP addresses so machines can communicate.

### DNS Resolution Process:
1. User enters domain name
2. DNS server searches IP
3. IP address returned
4. Connection established

**Example:**
google.com → 142.250.x.x

---

## HTTP vs HTTPS

### HTTP (HyperText Transfer Protocol)
- Data transmitted in plain text
- Vulnerable to eavesdropping and MITM attacks

---

### HTTPS (Secure HTTP)
- Uses SSL/TLS encryption
- Protects data confidentiality and integrity
- Prevents man-in-the-middle attacks

**Used in:** Banking, login portals

---

## IP Addressing

### IPv4
- 32-bit address
- Example: 192.168.1.1

### IPv6
- 128-bit address
- Example: 2001:db8::1

### Private IP Ranges
- 10.0.0.0 – 10.255.255.255
- 172.16.0.0 – 172.31.255.255
- 192.168.0.0 – 192.168.255.255

---

## NAT (Network Address Translation)

NAT allows multiple private devices to access the internet using a single public IP address.

### Types of NAT:
- Static NAT
- Dynamic NAT
- PAT (Port Address Translation)

**Used in:** Home and corporate routers
