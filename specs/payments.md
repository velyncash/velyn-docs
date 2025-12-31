# Payments Specification

## Supported Methods

- QR payments
- NFC (contactless)
- Card transactions
- RFID flows (controlled environments)

---

## Common Payment Flow

1. User selects payment method
2. User confirms recipient & amount
3. PIN confirmation (if required)
4. Backend validates & executes
5. Result returned to UI

---

## QR Payments

- Camera-based scan
- Amount confirmation
- Instant result display

---

## NFC Payments

- Device-level secure APIs
- Tap-to-pay experience
- PIN required for higher amounts

---

## RFID Payments

- Fast identification-based flows
- Restricted environments
- Backend-enforced rules

---

## Error Handling

Errors are:
- Clear
- Non-technical
- Actionable

Examples:
- Invalid QR
- Insufficient balance
- Network failure
