# 🚨 [CRITICAL] Issue #12: Real-Time Dispatch Integrity & Trust Ledger

Establish a tamper-resistant trust ledger that validates route authenticity, seals custody events, and provides a public integrity index across the ReGenX network.

---

## 🎯 Objective
- Create a **Trust Ledger** that records immutable custody events for each dispatch lifecycle (`localStorage: trust-ledger`).
- Implement **Integrity Scans** that detect GPS drift, route deviation, and time gaps.
- Provide **Trust Timeline** visualization per order (Provider/Rider/Plant).
- Auto-seal custody with a cryptographic hash on plant intake.
- Display a **Public Trust Index** summary widget on all dashboards.

---

## ✅ Core Requirements
- **Ledger Schema**
  - `{ id, orderId, event, ts, lat, lng, actorRole, actorId, trustScore, hash }`
- **Anomaly Detection**
  - Route deviation > 1.5 km from expected path
  - Time gap > 45 mins between events
- **UI**
  - Glassmorphic Trust Timeline
  - Badge-based integrity status (Green/Amber/Red)
  - Integrity Scan button with spinner

---

## 🧠 Proposed Modules
- `src/trust.js` — integrity scoring + deviation checks
- `src/app.js` — ledger writes and lifecycle hooks
- `src/styles.css` — timeline + scan micro-animations

---

## ✅ Quality Standards (Exceptional)
- Full **JSDoc** coverage for new helpers
- Zero console errors
- Responsive UI across roles
- Glassmorphism + micro-animations

---

## ✅ Acceptance Criteria
- Ledger persists in `localStorage` and updates on each order status change.
- Integrity Scan shows timeline and trust score within 1 second.
- Public Trust Index visible on Provider, Rider, and Plant dashboards.
- No regression in existing order flow.
