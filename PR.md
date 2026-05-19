# PR: Real-Time Dispatch Integrity & Trust Ledger

## Summary
- Add a public trust ledger for custody events (`trust-ledger`).
- Record integrity events on each order lifecycle transition.
- Provide integrity scan modal with timeline and trust score.
- Display a Public Trust Index widget across all dashboards.

## Changes
- Extend TrustProtocol with integrity scoring and route deviation analysis.
- Add ledger helpers, integrity scoring, and scan UI wiring in `app.js`.
- Add integrity timeline and trust index styles.
- Add new issue spec in `ISSUE-12.md`.

## Testing
- Manual: Create a dispatch, progress through rider/plant steps, then run Integrity Scan.
- Manual: Confirm trust index appears on Provider/Rider/Plant dashboards.

## Checklist
- [x] UI verified across Provider, Rider, Plant.
- [x] No console errors in normal flow.
- [x] Responsive layout preserved.
