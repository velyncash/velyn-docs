# Cards Specification

This document explains how **cards work in Velyn.Cash**.
Cards are treated as **controlled payment instruments**, not passive balances.

---

## 1. Card Concept

In Velyn, cards represent **permissioned access to funds**.

Each card:
- Has clear usage rules
- Can be controlled by the user
- Produces transparent transaction records

This design gives users **direct control** over how their money is used.

---

## 2. Card Types

### 2.1 Virtual Cards

Virtual cards are available directly inside the app.

#### Characteristics
- Instantly issued
- Can be used for online payments
- No physical form required

#### Use cases
- Online subscriptions
- One-time payments
- Safer online transactions

---

### 2.2 Physical Cards (Planned)

Physical cards allow **offline and in-store usage**.

#### Characteristics
- Tap or swipe at supported terminals
- Linked to the same account logic
- Subject to the same security rules

Physical cards extend Velyn into real-world daily spending.

---

## 3. Card Controls

Users have visibility and control over their cards.

### Available controls
- Enable / disable card
- View card activity
- Temporarily lock card

These controls are designed to be **simple and immediate**.

---

## 4. Spending Visibility

Card usage is always transparent.

### What users can see
- Transaction history
- Payment amount
- Merchant information (when available)

No hidden fees or unexplained deductions are shown.

---

## 5. Security Model

Card security follows the same **security-by-design principles** as the rest of the app.

### Key protections
- Card usage validated by backend
- PIN confirmation for sensitive actions
- Session-based authorization
- Immediate disable option in case of misuse

Sensitive card logic is never handled only on the client.

---

## 6. Card Lifecycle

High-level lifecycle:
1. Card issued (virtual or physical)
2. Card activated
3. Card used for transactions
4. Card monitored by user
5. Card disabled or replaced if needed

Each step is visible and intentional.

---

## 7. Future Enhancements (Planned)

Planned improvements include:
- Spending limits per card
- Merchant category restrictions
- Temporary virtual cards
- Card usage notifications

These features will be introduced gradually.

---

## 8. Status

Card functionality is:
- Partially implemented (virtual cards)
- Under active development
- Integrated incrementally with payment systems

This document will evolve as card features mature.
