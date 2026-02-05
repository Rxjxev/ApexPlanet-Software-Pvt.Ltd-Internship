# Cross-Site Scripting (XSS)

## Introduction
Cross-Site Scripting (XSS) is a vulnerability that allows attackers to inject malicious JavaScript code into web pages viewed by other users.

XSS occurs when applications fail to properly validate or encode user-supplied input.

---

## How XSS Works
An attacker injects JavaScript code into input fields. When the application displays this input without sanitization, the script executes in the victim’s browser.

---

## Types of XSS

### Stored XSS
- Malicious script is stored in the database  
- Executes every time a user visits the affected page  

### Reflected XSS
- Script is reflected immediately in the HTTP response  
- Commonly delivered via malicious URLs  

---

## Impact of XSS
- Session hijacking  
- Cookie theft  
- Phishing attacks  
- Defacement of web pages  

---

## XSS in DVWA
DVWA provides separate modules for:
- Stored XSS  
- Reflected XSS  

At **Low Security Level**, user input is directly rendered, allowing script execution.

---

## Prevention Techniques
- Input validation and output encoding  
- Content Security Policy (CSP)  
- Escaping special characters  
- Avoid inline JavaScript  

---

## Conclusion
XSS exploits client-side trust. Strong input handling and browser security mechanisms are essential to prevent this attack.

---
