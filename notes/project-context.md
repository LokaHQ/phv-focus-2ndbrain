---
last_updated: 2026-06-02
generated_by: /bootstrap
sows_processed: [sow5]
---

# Project Context — Pacific Health Ventures / Focus Healthspan

## What this engagement is

Loka is building **Focus Forward** (resident mobile app) and **Focus Activate** (staff web/mobile app) for Pacific Health Ventures — an AI-powered health recommendation platform for senior living residents. The system uses a hybrid rule-based + LLM recommendation engine fed by genetics (Tempest), blood biomarkers (Junction), demographics, and activity data (Human Good "Doris" data lake), with Buck Institute providing a biological analysis engine as an integrated third-party. The 26-week engagement targets an August 2026 pilot with ~100 Pioneer residents across Human Good communities.

## SOW summary

| SOW | Scope | Status | Key dates |
|-----|-------|--------|-----------|
| sow5 | Focus Forward resident app, Focus Activate staff app, hybrid recommendation engine, Buck Institute integration, data ingestion pipeline (Doris + Tempest + Junction) | Active — Sprint 3 starting | Start: 2026-04-14 · August pilot (Pioneer 100) · End: 2026-10-13 |

## Current status (as of 2026-06-02)

Sprint 2 complete; Sprint 3 just kicked off. Backend deployed to AWS/ECR with CI/CD pipeline established. Registration, onboarding, and staff login screens complete on frontend. Two hard blockers: CodeMagic billing (mobile CI/CD blocked) and Azure AD account (SSO blocked, C Fur to create). Buck Institute integration architecture is in progress — Jon and José designing multi-stage VPC; no formal engagement with Buck yet. Doris API not live until July 1; all frontend development using mock data. ML team (Dushica, Miguel, Ervin) onboarded; doing data discovery against Cubigo/JSON exports. Website (static, no CMS) due Wednesday.

## Key people

| Name | Company | Role | SOWs |
|------|---------|------|------|
| C Fur (Chris) | PAC Ventures | Founder / Primary client contact | sow5 |
| Todd Austin | Focus Healthspan | Product Lead / COO | sow5 |
| Emily Kruger | Focus Healthspan | CIO | sow5 |
| Nick | Human Good | Data Engineering / Doris data lake | sow5 |
| Ana Maximo | Loka | TPM / Engagement Lead | sow5 |
| Jon Trigueiro | Loka | Tech Lead (backend) | sow5 |
| José Pereira | Loka | Tech Lead (architecture/Buck) | sow5 |
| Dushica Jankovikj | Loka | ML Lead | sow5 |
| Davor Trifunov | Loka | Frontend Lead (mobile) | sow5 |
| Madalena Saraiva | Loka | Designer | sow5 |

## Open items and blockers

| Item | Owner | Status | Source |
|------|-------|--------|--------|
| CodeMagic billing — mobile CI/CD blocked | Davor Trifunov | Blocked (billing not enabled) | 2026-06-01 weekly planning |
| Azure AD account for SSO staff login | C Fur | C Fur to create; needs phone number | 2026-06-01 weekly planning |
| Buck Institute VPC/architecture design | Jon + José | In progress; must be done before engaging Buck | 2026-05-28 daily, 2026-06-01 daily |
| Define Buck data taxonomy (input/output JSON specs) | Jon + José | In progress | 2026-05-28 buck integration |
| Architecture diagram finalized | José Pereira | Was due EOW 2026-05-30 — status unknown | 2026-05-28 weekly review |
| Doris API live (Human Good / Nick) | Nick (Human Good) | Target: July 1, 2026 | 2026-05-12 daily |
| Junction contract signed | C Fur / Todd | 95% likely; not closed | 2026-05-28 buck integration |
| DUNS number for Apple App Store | C Fur | Was a blocker in Sprint 1; status unknown | 2026-05-14 weekly review |
| Master screen list for August | Ana + C Fur + Todd | Not defined; meeting to be scheduled | 2026-06-01 daily |
| Consent screen update (nutrition tab) | Design team | Not yet done | 2026-05-28 weekly review |

## Key decisions made so far

- **B2B pricing**: $20/resident/month
- **Product priority order**: resident app → staff app → insights platform
- **August pilot (Pioneer 100)**: ~100 residents; HIPAA/PHI data excluded from August; clinical medication recommendations excluded
- **Multi-tenant architecture**: logic layer only; infrastructure replicated per operator via IaC
- **Mock data strategy**: adopted to unblock frontend while data pipeline is finalized
- **Recommendation engine Phase 1**: Wizard of Oz (hard-wired rule-based based on onboarding goals); event-based triggers long-term; static for initial UI
- **Two-tier consent**: Non-PHI (basic profile, activity) + PHI (Health Fair Assessment, nutrition) — opt-in
- **Buck Institute**: NOT rebuilt in 2026; treated as directed development stream; Loka controls all data ingestion (Tempest + Junction); Buck analyses from within Loka's managed environment
- **REMOVED from scope**: staff support moments; outcome/hospitalization tracking
- **Cognitive training**: HIGH priority for August; community amenities LOW priority
- **Sprint 3 goal**: fully connected app (functional end-to-end, not just screens)
- **Domain**: focuspan.com → migrated to AWS Route53 (2026-05-27)
- **Three environments**: dev/staging/prod on same AWS account
- **QA workflow**: internal QA → staging → Chris Jira review

## ⚠ Tensions and gaps

### 1. Buck Institute engagement hasn't started — timeline risk
5 of the 18-month Buck contract have elapsed. As of June 2, Loka hasn't formally engaged Buck yet — no VPC, no taxonomy, no first technical call. C Fur has signaled urgency ("June is here, we need to dig deeper"). Jon and José are designing the architecture, but every week of delay compresses the window. **Risk: Buck integration may not be ready for August or even November milestones.**

### 2. Doris API not live until July 1 — late integration risk
All frontend development is on mock data. If the Doris API slips (Nick-side risk) or the integration is harder than expected, there's very little runway between July 1 and the August pilot to find and fix data issues. **The August pilot is entirely dependent on the Doris integration landing cleanly in July.**

### 3. No master screen list for August
Three months out from the pilot, there is no agreed inventory of screens to ship in August. Teams are building against a moving target. C Fur has asked for this and it hasn't been produced. **Risk of scope creep and misaligned expectations at the August pilot.**

### 4. Emily Kruger (CIO) absent from all meetings
Named in the SOW as a client contact but has not appeared in any of the 22 meetings processed. Unknown whether she is engaged at a governance level or is uninvolved. **Gap: no relationship established with the technical decision-maker at Focus Healthspan.**

### 5. Junction contract not signed
The blood biomarker integration pathway (Junction) is described as "95% likely" but not contracted. This is a primary data input to the Buck engine. **If Junction doesn't close, the biomarker integration path needs a fallback plan.**

### 6. ML codebase may need significant refactoring
Dushica flagged that the existing ML codebase may need to be largely replaced once the backend team takes over data operations. This is a known risk being tracked, but the scope of refactoring effort is unquantified. **May affect August delivery if refactor is larger than expected.**

### 7. "AI coaching" discussed but not clearly scoped
Multiple meetings discussed "behavioral science personality layer" and "AI coaching" as product elements, but these don't map clearly to SOW deliverables. **Risk of scope creep if these are pursued without explicit SOW alignment.**

### 8. Client visibility concern
C Fur has asked for team rosters, roadmaps, and resource breakdowns across multiple meetings. The team hasn't consistently delivered these. **If client trust erodes from lack of visibility, it creates relationship risk going into the August pilot.**
