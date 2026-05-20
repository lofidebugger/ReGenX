# PR: Route Emissions Tracker & Offset Ledger

## Summary
- Add a persistent emissions ledger (`emissions-ledger`) for route footprint.
- Log emissions entries on plant intake confirmation.
- Add Emissions Tracker view and navigation across roles.
- Add emissions widgets to dashboards.

## Changes
- Add emissions ledger helpers and view rendering in `app.js`.
- Add emissions tracker styles in `styles.css`.
- Add new issue spec in `ISSUE-18.md`.

## Testing
- Manual: Complete a dispatch and verify emissions entry appears.
- Manual: Open Emissions Tracker view and confirm stats render.

## Checklist
- [x] UI verified across Provider, Rider, Plant.
- [x] No console errors in normal flow.
- [x] Responsive layout preserved.
