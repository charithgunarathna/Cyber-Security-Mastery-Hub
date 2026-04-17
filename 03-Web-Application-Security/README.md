# 🕸️ Module 03: Advanced Web Application Security

![Level](https://img.shields.io/badge/Level-Advanced-red)
![Focus](https://img.shields.io/badge/Focus-AppSec_%26_Exploitation-blue)

Web applications are highly complex, making them the primary attack vector for modern threat actors. We will dive deep into advanced web vulnerabilities beyond the basic OWASP Top 10.

---

## 💉 Deep Dive: SQL Injection (SQLi) Varieties

SQLi is not just bypassing logins. Advanced attackers use it to exfiltrate entire databases or gain remote code execution (RCE).

1. **In-Band SQLi (Classic):** The attacker uses the same communication channel to launch the attack and gather results (e.g., Error-based SQLi, Union-based SQLi).
2. **Blind SQLi (Inferential):** The application does not return database errors. The attacker must ask True/False questions.
   * *Boolean-based:* Observing if the page content changes based on a True or False SQL query.
   * *Time-based:* Injecting `SLEEP(10)`. If the server takes 10 seconds to respond, the vulnerability is confirmed.
3. **Out-of-Band SQLi:** Used when the server cannot send responses directly to the attacker. The attacker forces the database to make a DNS or HTTP request to an external server they control.

---

## 🎭 Cross-Site Scripting (XSS) Demystified

XSS targets the user's browser, not the server. It allows attackers to steal session cookies, log keystrokes, or deface websites.

| Type | Mechanism | Impact Level |
| :--- | :--- | :--- |
| **Reflected XSS** | Payload is embedded in a malicious link. The server reflects it back to the victim. | High (Requires Social Engineering) |
| **Stored XSS** | Payload is saved permanently in the database (e.g., in a forum post). Executes when anyone views the page. | Critical (Mass exploitation) |
| **DOM-based XSS** | The vulnerability exists purely in the client-side JavaScript. The payload never reaches the server. | High (Hard for WAFs to detect) |

---

## 🔓 Advanced Modern Vulnerabilities

### 1. SSRF (Server-Side Request Forgery)
The attacker abuses functionality on the server to read or update internal resources. The attacker can force the web server to make HTTP requests to internal, highly secure endpoints (e.g., AWS Metadata URLs `http://169.254.169.254/latest/meta-data/` to steal cloud credentials).

### 2. IDOR (Insecure Direct Object Reference)
Occurs when an application provides direct access to objects based on user-supplied input. 
* *Example:* Changing a URL parameter from `user_id=101` to `user_id=102` allows an attacker to view another user's private financial records without proper authorization checks.

### 3. CSRF (Cross-Site Request Forgery)
Forcing an authenticated user to execute unwanted actions on a web application in which they are currently authenticated. Mitigated by using anti-CSRF tokens.

---
⬅️ **[Back to Module 02](../02-Network-Security/README.md)** | ➡️ **[Proceed to Module 04](../04-Ethical-Hacking-Labs/README.md)**
