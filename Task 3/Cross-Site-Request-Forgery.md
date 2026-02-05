# Cross-Site Request Forgery (CSRF)

## Introduction
Cross-Site Request Forgery (CSRF) is an attack that forces an authenticated user to perform unintended actions on a web application without their knowledge.

The attack relies on the trust a web application has in the user’s browser.

---

## How CSRF Works
When a user is logged in, their browser automatically includes session cookies with every request. An attacker can exploit this by tricking the user into clicking a crafted URL or visiting a malicious page.

---

## Impact of CSRF
- Unauthorized password changes  
- Account takeover  
- Unauthorized fund transfers  
- Data manipulation  

---

## CSRF in DVWA
DVWA demonstrates CSRF through a password change functionality.

At **Low Security Level**:
- Sensitive actions are performed using GET requests  
- No CSRF tokens are implemented  

This allows attackers to change user passwords using a crafted URL.

---

## Why CSRF Is Dangerous
- No direct interaction required from victim  
- Exploits existing authenticated sessions  
- Difficult for users to detect  

---

## Prevention Techniques
- CSRF tokens  
- SameSite cookie attribute  
- Use POST instead of GET for sensitive actions  
- Re-authentication for critical operations  

---

## Conclusion
CSRF exploits implicit trust between a browser and a web application. Token-based verification is the most effective defense.

---
