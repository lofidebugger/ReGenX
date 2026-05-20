# 🚨 [CRITICAL] Issue #18: Route Emissions Tracker & Offset Ledger

Introduce a route emissions tracker that estimates logistics CO₂ emissions and compares them against verified offsets.

---

## 🎯 Objective
- Create a persistent **Emissions Ledger** (`localStorage: emissions-ledger`).
- Log emissions entries on plant intake confirmation.
- Provide an **Emissions Tracker** view for all roles.
- Add an **Emissions Widget** to Provider/Rider/Plant dashboards.

---

## ✅ Core Requirements
- **Ledger Schema**
  - `{ id, orderId, org, distanceKm, emissionKg, offsetKg, score, ts }`
- **Emissions Model**
  - $\text{emissionKg} = \text{distanceKm} \times 0.21$
- **Scoring**
  - Score = offset vs emissions ratio
- **UI**
  - Glassmorphic tracker cards and efficiency bar
  - Recent route list with score badges

---

## 🧠 Proposed Modules
- `src/app.js` — ledger helpers, scoring, view rendering
- `src/styles.css` — emissions tracker styling

---

## ✅ Quality Standards (Exceptional)
- Full **JSDoc** on new helpers
- Zero console errors
- Responsive layout across roles
- Glassmorphism + micro-animations

---

## ✅ Acceptance Criteria
- Emissions entries created after plant intake.
- Emissions Tracker view and widget visible for all roles.
- Scores update based on emissions vs offsets.
