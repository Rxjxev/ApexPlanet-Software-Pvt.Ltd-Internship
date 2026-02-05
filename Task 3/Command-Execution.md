# Command Execution

## Introduction
Command Execution is a web application vulnerability that allows an attacker to execute arbitrary system commands on the server through a vulnerable application. This usually occurs when user-supplied input is directly passed to system-level functions without proper validation.

---

## How Command Execution Works
Web applications sometimes use system commands to perform operations such as pinging an IP address or retrieving system information. If user input is not sanitized, attackers can inject additional commands.

Example vulnerable code logic:
```
ping -c 4 <user_input>
```

If `<user_input>` is attacker-controlled, additional commands can be appended.

---

## Impact of Command Execution
- Execution of arbitrary system commands  
- Unauthorized access to server resources  
- Data theft or manipulation  
- Installation of malware or backdoors  
- Complete server compromise  

---

## Command Execution in DVWA
DVWA includes a **Command Execution** module that demonstrates this vulnerability clearly.

At **Low Security Level**:
- User input is directly passed to system commands
- No input filtering or validation is applied

Attackers can chain commands using separators like `;`, `&&`, or `|`.

---

## Prevention Techniques
- Avoid using system commands with user input  
- Validate and sanitize all user input  
- Use allowlists for acceptable input values  
- Implement least privilege for application processes  
- Disable dangerous system functions where possible  

---
