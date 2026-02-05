# File Inclusion Attacks

## Introduction
File Inclusion is a web application vulnerability that occurs when an application allows users to include files on the server without proper validation. This can lead to disclosure of sensitive files or execution of malicious code.

---

## Types of File Inclusion

### Local File Inclusion (LFI)
Local File Inclusion allows attackers to read sensitive files present on the server by manipulating file path parameters.

Common examples include:
- `/etc/passwd`
- `/etc/shadow`
- `/etc/os`
- `/etc/hosts`
- `/etc/hostname`
- Application configuration files

### Remote File Inclusion (RFI)
Remote File Inclusion occurs when an application allows inclusion of files from remote servers. This can lead to remote code execution.

---

## Impact of File Inclusion
- Disclosure of sensitive system files  
- Source code exposure  
- Remote code execution  
- Complete server compromise  

---

## File Inclusion in DVWA
DVWA provides a File Inclusion module to demonstrate both LFI and RFI attacks.

At **Low Security Level**, file paths are not validated, making the application vulnerable to inclusion attacks.

---

## Prevention Techniques
- Validate and sanitize file paths  
- Disable remote file inclusion in PHP  
- Use allowlists for file inclusion  
- Apply least privilege permissions  

---

## Conclusion
File Inclusion vulnerabilities can have severe consequences if exploited. Proper validation and secure server configuration are critical to prevent such attacks.

---
