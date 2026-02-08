#  Task 5: Capstone Project & Incident Response  
**Cybersecurity & Ethical Hacking Internship – ApexPlanet Software Pvt. Ltd.**

---

##  Overview

Task 5 represents the capstone of the ApexPlanet Cybersecurity & Ethical Hacking Internship. This task focuses on applying all the skills learned throughout the internship into a real-world security assessment, followed by a structured incident response simulation using industry-standard tools and methodologies.

---

##  Objective

- Apply cybersecurity concepts in a real-world capstone project  
- Perform a controlled security assessment on a vulnerable web application  
- Identify, analyze, and document security vulnerabilities  
- Simulate a complete incident response lifecycle  
- Produce professional technical documentation  

---

##  Theory

###  Capstone Project in Cybersecurity

A capstone project is a practical implementation that integrates multiple cybersecurity domains such as reconnaissance, vulnerability assessment, exploitation, logging, monitoring, and mitigation. It reflects how security professionals assess systems, respond to incidents, and improve defenses in an ethical and controlled environment.

---

###  Incident Response Overview

Incident Response (IR) is a structured approach used to manage and respond to security incidents such as unauthorized access, malware infections, or data breaches. A well-defined IR process minimizes damage, reduces downtime, and strengthens future security posture.

#### **Key Phases of Incident Response**
1. **Preparation** – Setting up tools, logging mechanisms, and response plans  
2. **Identification** – Detecting suspicious activities through scans and logs  
3. **Containment** – Isolating affected systems to prevent further impact  
4. **Eradication** – Removing vulnerabilities and attack vectors  
5. **Recovery** – Restoring systems to secure normal operation  
6. **Lessons Learned** – Documenting findings and improving defenses  

---

##  Tools & Technologies Used

- **Kali Linux** – Penetration testing environment  
- **DVWA / Metasploitable2 / Mutillidae** – Vulnerable target applications  
- **Nmap** – Network and service scanning  
- **Burp Suite** – Web application testing  
- **OWASP ZAP (Checkmarx)** – Automated vulnerability scanning  
- **ELK Stack (Optional)** – Log analysis and monitoring  
- **Linux Logs** – Incident detection and investigation  

---

##  Practical Implementation

###  Project Selection

** Web Application Vulnerability Assessment & Incident Response**

The project involved testing intentionally vulnerable web applications hosted in a local lab environment to identify security flaws and simulate an incident response based on the findings.

---

###  Project Planning

- **Scope**: Local vulnerable web application environment  
- **Target IP**: `192.168.56.103`  
- **Attack Types**: SQL Injection, Cross-Site Scripting (XSS), Security Misconfigurations  
- **Output**: Vulnerability assessment report and incident response documentation  

---

###  Reconnaissance & Scanning

- Conducted network and service scanning using `nmap`  
- Identified open ports, running services, and application endpoints  
- Analyzed application structure and possible attack surfaces  

```bash
nmap -sV <target-ip>
```

---

###  Vulnerability Exploitation

- **SQL Injection** used to extract backend database information  
- **Cross-Site Scripting (XSS)** tested via user input fields  
- Evidence captured using screenshots, tool outputs, and logs  

All exploitation activities were strictly performed in a controlled and ethical lab environment.

---

##  Vulnerability Scanning (OWASP ZAP)

An automated vulnerability scan was conducted using **OWASP ZAP v2.16.1**, covering High, Medium, Low, and Informational risk levels.

###  Scan Summary

| Risk Level | Alerts |
|-----------|--------|
| High | 2 |
| Medium | 6 |
| Low | 8 |
| Informational | 7 |
| **Total** | **23 Alerts** |

---

###  Key Vulnerabilities Identified

**High Risk**
- Hash Disclosure – MD5 Crypt  
- Path Traversal (access to sensitive system files)

**Medium Risk**
- Absence of Anti-CSRF Tokens  
- Content Security Policy (CSP) Header Not Set  
- Directory Browsing Enabled  
- Missing Anti-Clickjacking Headers  
- Vulnerable JavaScript Libraries  

**Low & Informational**
- Insecure cookie flags (`HttpOnly`, `SameSite`)  
- Server and framework version disclosure  
- Debug error messages  
- Timestamp and private IP disclosure  
- Potential XSS via user-controllable attributes  

---

##  Incident Response Simulation

###  Detection

- Vulnerabilities identified through automated ZAP scans  
- Suspicious endpoints and insecure headers detected  
- Findings correlated with application logs  

---

###  Containment

- Restricted access to vulnerable directories  
- Disabled unnecessary services and features  
- Reduced exposure of sensitive information  

---

###  Mitigation & Recommendations

- Replace weak hashing with bcrypt / SHA-256  
- Implement prepared statements and strict input validation  
- Add essential security headers:
  - `Content-Security-Policy`
  - `X-Frame-Options`
  - `X-Content-Type-Options`
- Enable CSRF protection mechanisms  
- Harden cookie attributes and server configurations  

---

###  Post-Incident Analysis

- **Root Cause**: Security misconfigurations and lack of input validation  
- **Impact**: Information disclosure and potential unauthorized access  
- **Outcome**: Actionable security improvements documented  

---

##  Deliverables

- ✔ OWASP ZAP Vulnerability Scanning Report  
- ✔ Incident Response Documentation  
- ✔ Screenshots and Technical Evidence  
- ✔ GitHub Repository with methodology and notes  
- ✔ Final Presentation / Demonstration Video  

---

##  Key Learnings

- Hands-on experience with real-world vulnerability scanning  
- Practical understanding of OWASP Top 10 risks  
- Importance of incident response and structured documentation  
- Improved analytical and reporting skills  

---

##  Conclusion

This capstone project successfully demonstrated the practical application of cybersecurity principles in a real-world testing environment. By combining vulnerability assessment with an incident response simulation, the task strengthened both technical expertise and professional reporting skills, preparing me for real-world cybersecurity roles.

---
