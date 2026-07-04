# Access Control — Explained

## What is Access Control?

In simple terms, **Access Control** is a security mechanism that determines whether you are allowed to access a resource and what actions you can perform on it.

For example, it can determine whether you are allowed to enter a manager's office. If you have permission to enter, it also determines what you are allowed to do inside.

### Authentication
**Who are you?**
Verifies your identity. E.g., logging in with a username and password, or a fingerprint. *You prove you are who you claim to be.*

---

### Authorization
**What can you do?**
Determines what actions or resources you're permitted to access after identity is confirmed.
*The system decides what you're allowed to do.*

---

### Access Control
**The full system.**
The broader mechanism that enforces both authentication and authorization policies at every layer.
*The gate, the lock, and the policy combined.*

---

## Why is Access Control important?

Access Control helps protect sensitive data and functionality from unauthorized users. Without proper access control, attackers may access other users' data, perform unauthorized actions, or gain higher privileges within the application.

## How does Access Control work?

1. A user sends a request to the application.
2. The application checks whether the user has permission to perform the requested action.
3. If the user has permission, the request is processed.
4. Otherwise, access is denied and a **403 Forbidden** response is returned.

## Common vulnerabilities caused by Broken Access Control

1. [IDOR (Insecure Direct Object Reference)](IDOR.md)
   Accessing another user's resources.
2. [Privilege Escalation (horizontal / vertical)](Privilege-Escalation.md)
   Gaining permissions that should not be available to the user.
3. [Unprotected Functionality](Unprotected-Functionality.md)
   Accessing sensitive features without proper authorization checks.
4. [Mass Assignment](Mass-Assignment.md)
   Modifying sensitive fields that should not be controlled by the user.

---

> **Correction:** Around the 10-minute mark of the video, the error code was mistakenly said to be **404**. The correct code for an access-denied response is **403 Forbidden**.

---

## References

- [OWASP Top 10 – Broken Access Control](https://owasp.org/Top10/A01_2021-Broken_Access_Control/)
- [OWASP Authorization Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html)
- [OWASP IDOR Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Insecure_Direct_Object_Reference_Prevention_Cheat_Sheet.html)
- [PortSwigger – Access Control](https://portswigger.net/web-security/access-control)
- [NIST SP 800-162 – ABAC Guide](https://csrc.nist.gov/pubs/sp/800/162/upd2/final)
