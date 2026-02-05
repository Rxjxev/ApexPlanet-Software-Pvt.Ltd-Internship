---

# SQL Injection (SQLi)

## Introduction
SQL Injection is a web application vulnerability that allows an attacker to interfere with the SQL queries executed by an application. It occurs when user input is not properly validated or sanitized before being used in SQL statements.

SQL Injection is listed in the OWASP Top 10 due to its severe impact, including data leakage and authentication bypass.

---

## How SQL Injection Works
Applications often take user input and embed it directly into SQL queries. If the input is not handled securely, attackers can manipulate the query logic.

### Vulnerable Query Example
```sql
SELECT * FROM users WHERE id = '$id';
```

If `$id` is controlled by the user, the query logic can be altered.

---

## Impact of SQL Injection
- Unauthorized access to sensitive data  
- Bypass authentication mechanisms  
- Modification or deletion of database records  
- Complete database compromise  

---

## SQL Injection in DVWA
In DVWA, the SQL Injection module demonstrates how unsanitized input can be exploited to extract user information.

The vulnerability is clearly visible at **Low Security Level**, where no input validation is applied.

---

## Types of SQL Injection
- Error-based SQL Injection  
- Boolean-based SQL Injection  
- Union-based SQL Injection  
- Blind SQL Injection  

---

## Prevention Techniques
- Use Prepared Statements (Parameterized Queries)  
- Input validation and sanitization  
- Least privilege database accounts  
- Web Application Firewalls (WAF)  

---

## Conclusion
SQL Injection remains one of the most dangerous web vulnerabilities. Proper secure coding practices and defensive programming can effectively mitigate this risk.

---
