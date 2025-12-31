# Security by Design

This document describes security principles for Velyn.Cash.
Security is treated as a default requirement, not a feature toggle.

---

## 1) Core Principles

- **Defense in depth:** multiple layers of protection  
- **Least privilege:** access only what is necessary  
- **Backend authority:** critical rules enforced server-side  
- **Minimal exposure:** reduce sensitive data displayed or stored  

---

## 2) Authentication & Access

- Username/password login
- PIN confirmation for secure access and sensitive actions
- Session-based authorization with expiration

---

## 3) Client Security Rules

Client apps follow strict rules:
- No secrets in the frontend
- No sensitive logging
- Config via environment files
- UI is a presentation layer, not a rules engine

---

## 4) Payment Security

Payment actions follow intentional confirmation:
- Clear transaction preview before execution
- PIN confirmation when required
- Backend validation for every payment request

---

## 5) Data Protection

- Sensitive data minimized
- Data access controlled via auth/session validation
- No unnecessary third-party exposure by default

---

## 6) Operational Practices

- CI checks to prevent broken builds
- Dependency monitoring (updates reviewed before merge)
- Incremental releases, tested before expanding access

---

## 7) Summary

Velyn.Cash security aims for:
- clarity for users
- safe-by-default behavior
- consistent protections across all payment methods
