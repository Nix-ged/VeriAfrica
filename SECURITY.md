# SECURITY.md
Project: VeriAfrica  
Purpose: Security principles and safeguards

---

## 1. Security Philosophy

Security is built into the system design, not added later.

---

## 2. Data Protection

- No sensitive personal data is required for basic usage
- User data is stored using secure, industry-standard practices
- Access to internal systems is restricted by role

---

## 3. API Security

- Public APIs are read-only
- Admin APIs require authentication
- System jobs use isolated credentials

---

## 4. Abuse Prevention

- Rate limiting on public endpoints
- Logging of suspicious activity
- Manual override for critical actions

---

## 5. Disclosure

Security issues should be reported privately to the project owner.
