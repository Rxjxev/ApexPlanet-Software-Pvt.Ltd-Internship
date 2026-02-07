## Password Attacks

### Overview

Password attacks are techniques used to gain unauthorized access to systems by targeting weak, reused, or poorly protected passwords. These attacks exploit human behavior and weak authentication mechanisms rather than software vulnerabilities.

Password attacks are commonly observed during penetration testing to demonstrate the importance of strong password policies and secure authentication practices.

---

## Hydra Brute-Force Attack

### Theory

**Hydra** is a fast and flexible online password-cracking tool that supports numerous protocols such as SSH, FTP, HTTP, SMB, and more. It works by systematically trying multiple username and password combinations until valid credentials are found.

Brute-force attacks are effective when:
- Weak passwords are used
- No account lockout policy is implemented
- Rate limiting is absent

---

### Practical: SSH Brute-Force Using Hydra

```bash
hydra -l msfadmin -P /usr/share/wordlists/rockyou.txt ssh://192.168.56.102
```

### Command Explanation
- `hydra` → Launches the Hydra tool  
- `-l msfadmin` → Specifies the target username  
- `-P /usr/share/wordlists/rockyou.txt` → Uses a password wordlist  
- `ssh://` → Target protocol  
- `192.168.56.102` → Target system IP address  

If successful, Hydra displays the valid username and password combination.

---

### Security Risk Demonstrated
- Unauthorized system access
- Potential privilege escalation
- Lateral movement across the network

---

## Password Cracking Using John the Ripper

### Theory

**John the Ripper** is an offline password-cracking tool used to crack hashed passwords extracted from compromised systems. Unlike brute-force attacks, John works offline, making it faster and stealthier.

Password cracking highlights weaknesses in:
- Poor hashing algorithms
- Unsalted hashes
- Weak passwords

---

### Practical: Cracking Password Hashes

```bash
john hashes.txt
```

This command initiates the password cracking process on the hash file.

```bash
john --show hashes.txt
```

Displays successfully cracked passwords.

---

### Security Implications
- Exposure of user credentials
- Compromise of multiple services using reused passwords
- Full system takeover in worst-case scenarios

---

### Mitigation & Prevention
- Enforce strong password policies
- Implement account lockout mechanisms
- Use salted and strong hashing algorithms (bcrypt, Argon2)
- Enable multi-factor authentication (MFA)

---
