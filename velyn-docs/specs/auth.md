# Authentication & Access Specification

This document explains how **authentication and access control** work in Velyn.Cash.
The focus is on **clarity, security, and simplicity**.

---

## 1. Authentication Model

Velyn.Cash uses a **two-layer authentication model**:

1. Account credentials (username & password)
2. PIN-based confirmation for secure access

This model balances **ease of use** and **security** without overcomplicating the user experience.

---

## 2. Sign Up Flow

### User steps
1. User chooses a username
2. User sets a password
3. User sets a numeric PIN (4–6 digits)
4. Account is created

### Design intention
- Fast onboarding
- No unnecessary personal data
- Clear responsibility on the user side

---

## 3. Sign In Flow

### User steps
1. Enter username & password
2. Proceed to PIN confirmation
3. Access granted to main app

### Why PIN is separate
- Adds protection if credentials are compromised
- Prevents accidental access
- Keeps sensitive actions gated

---

## 4. PIN Verification

### PIN rules
- Numeric only
- 4 to 6 digits
- Never displayed in plain text
- Never logged in UI or console

### Usage
- App unlock
- Sensitive actions (future)
- Session confirmation

---

## 5. Session Handling (High-Level)

- Sessions are temporary
- Session validity is checked on app launch
- Expired sessions require re-authentication

> Exact session mechanics are handled by backend services and are not exposed in the UI layer.

---

## 6. Error Handling

Authentication errors are designed to be **clear but not revealing**.

Examples:
- “Invalid credentials”
- “PIN incorrect”
- “Session expired”

The system avoids exposing technical details to users.

---

## 7. Security Considerations

Key security practices:
- No credentials stored in plain text
- No PIN stored or logged in UI
- Environment-based configuration
- Clear separation between UI and backend logic

---

## 8. Future Enhancements (Planned)

- Biometric authentication (Face ID / Fingerprint)
- Device-based trust
- Session activity overview
- Multi-device management

---

## 9. Status

Authentication flows are **implemented at UI level** and **under active backend integration**.

This specification will evolve as the system matures.
