---
date: 2026-05-13
sow: sow5
attendees: [Ana Maximo, Jon Trigueiro, chris@pac.vc, todd@focushealthspan.com]
type: client
---

# Loka <> PHV Focus — Evaluate Vision Roadmap — 2026-05-13

## Key Takeaways
- **Wizard of Oz approach**: hard-wired, rule-based recommendations based on onboarding goals for the initial phase before the full ML engine is operational
- **Two-tier consent architecture**: Non-PHI consent (basic profile, activity data) and PHI consent (Health Fair Assessment results, nutrition) — opt-in model
- **Pilot size**: ~100 residents across communities (Pioneer 100)
- Automated S3 bucket file processing will replace manual data entry for data ingestion
- Nested JSON files confirmed for backend data integration
- Jon Trigueiro authorized to define and lead the technical data pipeline architecture

## Decisions Made
- Recommendation approach for initial phase: Wizard of Oz (hard-wired, rule-based, based on onboarding goals)
- Jon Trigueiro leads technical data pipeline architecture
- Pilot: ~100 residents
- Two-tier consent: Non-PHI and PHI (opt-in)

## Action Items

| Action | Owner | Due |
|--------|-------|-----|
| Write comprehensive document explaining V1 deliverables | Ana Maximo | ASAP |
| Generate 6 recommendation examples tied to each onboarding goal | C Fur | ASAP |
| Create simple recommendation base using onboarding results | Jon Trigueiro | Sprint 2 |
| Define best approach for automated data ingestion (S3 → nested JSON) | Jon Trigueiro | ASAP |

## Notes

This session evaluated the roadmap from a product/vision perspective after the PR/PRFAQ work. Key output: Wizard of Oz approach confirmed for Phase 1 recommendations. Two-tier consent model formalized. Jon has full authority over the data pipeline technical decisions.
