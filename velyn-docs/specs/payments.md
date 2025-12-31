# Payments Specification

This document describes how **payments work in Velyn.Cash**.
The focus is on **real-world usability**, **clear flows**, and **consistent user experience**.

---

## 1. Payment Philosophy

Payments in Velyn are designed to be:
- Fast
- Clear
- Familiar
- Secure by default

Users should always understand **what they are paying**, **how**, and **when a transaction is completed**.

---

## 2. Supported Payment Methods

Velyn.Cash supports multiple payment methods to cover daily use cases.

### 2.1 QR Payments

QR payments allow users to **scan and pay instantly**.

#### Flow
1. User opens the payment screen
2. Scans a QR code
3. Confirms amount and recipient
4. Enters PIN (if required)
5. Transaction is completed

#### Design goals
- Minimal steps
- Clear confirmation
- Visible transaction result

---

### 2.2 NFC (Contactless Payments)

NFC enables **tap-to-pay** functionality on supported devices.

#### Flow
1. User enables contactless mode
2. Taps device on payment terminal
3. Transaction is verified
4. Payment confirmation is shown

#### Notes
- Device capability dependent
- Uses secure system-level APIs
- PIN confirmation may be required for higher amounts

---

### 2.3 Card Payments

Velyn supports **card-based transactions** for online and offline use.

#### Card types
- Virtual cards
- Physical cards (planned)

#### Card controls
- Enable / disable card
- Spending visibility
- Usage history

Cards are treated as **controlled payment instruments**, not passive balances.

---

### 2.4 RFID-Based Transactions

RFID cards enable **fast identification-based payments**.

#### Use cases
- Access-based payments
- Tap-and-go scenarios
- Controlled environments

RFID usage is limited by predefined rules and security checks.

---

## 3. Transaction Confirmation

Every payment follows a **confirmation-first model**.

### Confirmation methods
- Visual confirmation
- Transaction summary
- PIN verification (when applicable)

Users always receive feedback about the transaction status.

---

## 4. Transaction Records

Each transaction produces a **clear record**.

### Transaction details
- Date & time
- Amount
- Payment method
- Status

Records are displayed in a readable format without unnecessary complexity.

---

## 5. Error Handling

Payment errors are handled gracefully.

Examples:
- Insufficient balance
- Invalid QR
- Contactless failure
- Network issues

Error messages are:
- Clear
- Non-technical
- Actionable

---

## 6. Security Considerations

Payment security includes:
- Encrypted requests
- Session validation
- PIN-based confirmation
- Backend-side verification

Sensitive logic never runs only on the client.

---

## 7. Limits & Controls (Planned)

Future improvements include:
- Per-transaction limits
- Daily spending limits
- Method-specific restrictions

These controls will be configurable by users.

---

## 8. Status

Payment features are:
- Actively implemented
- Being integrated with backend services
- Expanded incrementally

This specification will be updated as payment methods mature.
