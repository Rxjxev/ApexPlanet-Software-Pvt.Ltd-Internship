# Firewall Basics

A firewall is a security mechanism that monitors and controls incoming and outgoing
network traffic based on predefined security rules. Firewalls act as a barrier
between trusted internal networks and untrusted external networks.

Firewalls help prevent unauthorized access, limit attack surfaces, and protect
systems from network-based attacks such as port scanning, brute-force attempts,
and malware communication.

In Linux-based systems, iptables is a commonly used firewall framework that
operates at the kernel level and filters packets based on rules.

---

## Types of Firewalls

- Packet Filtering Firewalls
- Stateful Inspection Firewalls
- Application Layer Firewalls
- Next-Generation Firewalls (NGFW)

iptables is primarily a **stateful packet filtering firewall**.

---

## Tool Used
- iptables

---

## Default Policy

The default policy defines how packets are handled if no rule matches.

iptables -P INPUT DROP  
iptables -P FORWARD DROP  

Setting the default policy to DROP ensures that all incoming traffic is blocked
unless explicitly allowed by firewall rules.

---

## Allow Rules

Allow rules permit specific types of traffic required for system operation.

### Allow SSH
iptables -A INPUT -p tcp --dport 22 -m conntrack --ctstate NEW,ESTABLISHED -j ACCEPT  

Allows secure remote login access to the system.

### Allow HTTP
iptables -A INPUT -p tcp --dport 80 -m conntrack --ctstate NEW,ESTABLISHED -j ACCEPT  

Allows web traffic to reach the server.

---

## Block Rules

Block rules explicitly deny unwanted or risky traffic.

### Block FTP
iptables -A INPUT -p tcp --dport 21 -j DROP  

Blocks FTP service, which is insecure if unencrypted.

### Block Specific IP
iptables -A INPUT -s 203.0.113.5 -j DROP  

Blocks all traffic from a specific suspicious IP address.

---

## Verify Rules
iptables -L -n  

Lists active firewall rules and verifies correct configuration.

---

## Findings
Firewall rules reduce the attack surface by allowing only required services
and blocking unauthorized access.

A properly configured firewall is a critical component of system hardening
and network security.
