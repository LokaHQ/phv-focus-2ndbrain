---
date: 2026-05-06
sow: sow5
attendees: [Ana Maximo, Sushmitha Regulapati, Jon Trigueiro, chris@pac.vc, todd@focushealthspan.com]
type: client
---

# Loka <> Focus — FOCUS Forward V1 PRFAQ — 2026-05-06

## Key Takeaways
- August launch roadmap confirmed: core resident app features + data integration are the priority
- Staff application will be developed as a web version first (faster iteration, no App Store dependency)
- Buck Institute integration: data via S3 buckets; "black box" architecture — Loka controls ingestion, Buck processes, results returned to Focus
- Pre-work on Buck integration needs to start immediately
- B2B pricing model framing discussed for the press release

## Decisions Made
- Staff app = web-first for the August pilot
- Buck Institute data integration: Loka ingests from Tempest → stores in Focus → Buck accesses → processed results returned
- August launch is the target anchor date for the press release / PRFAQ framing

## Action Items

| Action | Owner | Due |
|--------|-------|-----|
| Contact Nick (Human Good); connect Loka team for data clarification | Sushmitha Regulapati | ASAP |
| Define input/output standards for Buck Institute data integration (JSON structure) | C Fur, Jon Trigueiro, Ana Maximo | ASAP |
| Begin development of Focus Activate staff app (web view) | Team | Sprint 2 |

## Notes

Session focused on reviewing the press release / FAQ document and aligning on August launch strategy. The Buck Institute integration architecture was clarified as a "black box" model where Loka controls the data pipeline on both sides. Staff app to be web-first to reduce App Store dependency.
