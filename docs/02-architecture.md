# System Architecture

This document explains the **high-level architecture** of Velyn.Cash.
It focuses on clarity and separation of responsibilities.

---

## 1) High-Level Structure

Velyn.Cash is structured as a modular client–server platform:

- **Client Layer**
  - Web app (UI + flows)
  - Mobile app (device features like camera/NFC)

- **Backend Layer**
  - Authentication and sessions
  - Payment processing and validation
  - Transaction records and analytics data

---

## 2) Core Flow

User
↓
Web/Mobile UI
↓ (authenticated requests)
Backend API
↓
Core services (auth, payments, records, analytics)


The backend is the **single source of truth** for critical rules.

---

## 3) Client Responsibilities

Client applications should:
- Render UI and manage screen state
- Collect user inputs (amount, recipient, confirmations)
- Call backend APIs and display results

Clients should NOT:
- Decide critical payment outcomes
- Store secrets
- Bypass backend validation

---

## 4) Payment Architecture (Modular)

Payment methods are designed as modules:
- QR
- NFC
- Card transactions
- RFID flows (planned)

All methods should produce:
- Consistent transaction records
- Clear statuses
- Unified history view

---

## 5) Scalability Principles

The system is designed to scale by:
- Clear module boundaries
- Stateless API patterns (where applicable)
- Incremental rollouts per feature

---

## 6) Summary

Velyn.Cash architecture prioritizes:
- Separation of concerns
- Backend-enforced security
- Modular feature development
- Long-term maintainability
