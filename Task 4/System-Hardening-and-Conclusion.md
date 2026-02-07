##  System Hardening

###  Theory

**System Hardening** is the process of securing an operating system by reducing its attack surface. This is achieved by removing unnecessary services, applying security patches, enforcing strict access controls, and configuring security mechanisms such as firewalls.

The primary goal of system hardening is to minimize vulnerabilities that attackers could exploit and to strengthen the overall security posture of a system.

System hardening is a critical defensive practice that complements exploitation and penetration testing by ensuring that discovered vulnerabilities are properly mitigated.

---

###  Key Objectives of System Hardening
- Reduce the number of attack vectors
- Prevent unauthorized access
- Limit system exposure to threats
- Improve system stability and reliability
- Enforce security best practices

---

###  Apply Security Updates

Keeping the system updated is one of the most important hardening steps, as updates often contain fixes for known vulnerabilities.

```bash
sudo apt update && sudo apt upgrade
```

**Explanation:**
- `apt update` refreshes the package list
- `apt upgrade` installs the latest security patches and updates

Regular updates prevent attackers from exploiting publicly known vulnerabilities.

---

###  Configure Firewall (UFW)

A firewall controls incoming and outgoing network traffic based on predefined security rules.

```bash
sudo ufw enable
```

Enables the Uncomplicated Firewall (UFW).

```bash
sudo ufw deny 23
```

Blocks **Telnet (port 23)**, an insecure and unencrypted service.

```bash
sudo ufw allow 22
```

Allows **SSH (port 22)** for secure remote access.

```bash
sudo ufw status verbose
```

Displays the current firewall rules and status.

---

### 🔹 Disable Unused Services

Unused or unnecessary services increase the attack surface and should be disabled.

```bash
sudo systemctl stop telnet
```

Stops the Telnet service immediately.

```bash
sudo systemctl disable telnet
```

Prevents the Telnet service from starting automatically on boot.

```bash
systemctl list-units --type=service
```

Lists all active services, helping identify services that can be disabled.

---

###  Additional Hardening Measures

- Enforce strong password policies
- Use role-based access control (RBAC)
- Enable automatic security updates
- Deploy intrusion detection/prevention systems (IDS/IPS)
- Monitor system logs regularly
- Apply the principle of least privilege

---

##  Conclusion

This task provided hands-on experience with exploitation techniques and defensive security practices. By applying system hardening measures such as patch management, firewall configuration, and service minimization, the importance of proactive defense and ethical penetration testing was reinforced.
