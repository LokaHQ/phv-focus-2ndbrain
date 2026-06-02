---
status: active
started: 2026-04-14
expected_end: 2026-10-13
---

# SOW5 — Reference

## What this SOW is

Loka is delivering the Focus Healthspan platform: two mobile applications ("Focus Forward" for residents, "Focus Activate" for staff) plus a brand identity for Pacific Health Ventures. The platform serves senior living communities with an AI-powered recommendation engine that surfaces personalized wellness activities based on resident goals, functional assessments, genetic data (Buck Institute), and blood biomarkers (Junction). The August 2026 milestone is a Pioneer 100 pilot across PHV communities. Success is defined as resident enrollment, engagement with recommendations, and staff-led health fair data collection at pilot communities.

## Scope

- **Focus Forward** (resident mobile app): Onboarding, vitality score, AI-powered wellness recommendations (cognitive, physical, social), consent management, activity tracking
- **Focus Activate** (staff web/mobile app): Resident enrollment via QR code, consent collection, health fair assessment data entry, resident list and profiles
- **Recommendation Engine**: Hybrid rule-based + LLM; event-based triggers; data from resident goals (onboarding), Cubigo/Human Good (activities/meals), Junction (blood biomarkers), Buck Institute (genomics)
- **Brand Identity**: Logo, colors, marketing website (focuspan.com), presentation templates
- **Buck Institute Integration**: Ingest raw Tempest IDAT genetic files; store in Focus system; provide structured JSON to Buck engine for processing; modular/plug-and-play architecture
- **Infrastructure**: AWS (ECS, ECR, Cognito, Route53, S3, SQS); multi-tenant at logic layer; dev/staging/prod environments
- **Consent**: Two-tier (Non-PHI: basic profile, activity; PHI: Health Fair Assessment results, nutrition); opt-in model

**Out of scope (this SOW):**
- Staff support and engagement moments (removed)
- Clinical trial outcomes and hospitalization tracking (removed)
- HIPAA-regulated medical data in August pilot (deferred)
- Clinical medication recommendations (excluded)
- Rebuilding the Buck genomics engine (Loka builds the integration only)

## Key Deliverables

| Deliverable | Due | Status |
|-------------|-----|--------|
| Brand identity (logo, colors, website) | June 2026 | ⏳ In progress |
| Focus Forward app (MVP onboarding + recommendations) | August 2026 | ⏳ In progress |
| Focus Activate staff app (enrollment + consent + health fair) | August 2026 | ⏳ In progress |
| Buck Institute integration (data ingestion pipeline) | August 2026 | ⏳ In progress |
| Pioneer 100 pilot launch | August 2026 | ⏳ Not started |
| Human Good / Cubigo data integration (API) | July 2026 | ⏳ Blocked (API target Jul 1) |

## Key Dates

| Date | Event |
|------|-------|
| 2026-04-14 | SOW5 start |
| 2026-04-23 | Deep Dive #1 — product vision + Buck architecture |
| 2026-04-27 | Deep Dive #2 — Sprint 1 priorities |
| 2026-04-29 | Implementation kickoff with full team |
| 2026-05-11 | Roadmap alignment — August + November deliverables |
| 2026-05-26 | ML team onboarded |
| 2026-08-XX | Pioneer 100 pilot target |
| 2026-10-13 | SOW5 end |

## Team

**Loka:**
- Ana Maximo — PM / Engagement Lead
- Jon Trigueiro — Backend Lead
- José Pereira — Tech Lead (joined May 26)
- Davor Trifunov — Mobile (iOS/Android)
- Stefanija Zdraveska — Frontend (Staff app)
- Madalena Saraiva — Design
- Tamara Ilieva — Backend / Auth
- Dejan Karadjinski — DevOps
- Ivan Krstev — Backend
- Paolo Pecis — QA
- Marija Dimoska — QA
- Ervin Shaqiri — Mobile
- Miguel Miranda — Mobile
- Dushica Jankovikj — ML
- Sushmitha Regulapati — ML
- Bruno Madeira — Branding/Web

**Client:**
- Chris Fur (chris@pac.vc) — PAC Ventures, primary client contact
- Todd Austin (todd@focushealthspan.com) — Focus Healthspan, product owner
- Emily Kruger — CIO, Focus Healthspan
- Nick (Human Good) — Data engineering, "Doris" data lake / Cubigo API

**Third party:**
- Buck Institute — Genomics engine (Andrew Magis, team of ~8-12)

## Notes

- Domain: focuspan.com — migrated from GoDaddy to AWS Route53 (May 27)
- CodeMagic billing blocked — workaround via Android APK for testing
- DUNS number pending (Apple App Store enrollment blocked as of May 14)
- Azure AD account needed for staff SSO (Chris Fur action item as of Jun 1)
- B2B pricing: $20/resident/month
- Development workflow: dev → QA → staging → Chris review; two-week sprints; Jira (feature-based view from Sprint 3)
- Recommendation engine: static recommendations in UI initially; ML engine integration in parallel

---

## Active Working Sessions

(Maintained by Claude Code. Do not edit manually.)

| Session | Status | Link |
|---------|--------|------|
