---
last_updated: 2026-06-02
channels: "#pacific-health-ventures-sow4-implementation, #loka-pacific-health-ventures, #external-loka-pacific-health-ventures"
---

# Slack Context — sow5

## Summary
The internal team channel shows a project in active early-sprint execution: backend and IaC are up, CI/CD pipelines are running, and the ML team just joined in late May. The primary client concern is visibility into progress — addressed via Jira tracking and a sprint overview doc. The external channel with Nick Lindberg (HumanGood/Cubigo) is the data pipeline thread; first data dumps have arrived and ML is already asking clarifying questions.

## Key Themes
- **Delivery timeline pressure**: Jun 12 homepage deadline, end-of-August target for both apps + recommendation engine running
- **Data dependency**: ML team blocked or constrained by data quality/availability; José raised concern that SQL won't scale for ML query load — data lake discussion open
- **Client visibility**: Chris repeatedly asking for project progress visibility → Jira board shared, sprint overview doc created, Confluence page → migrated to Google Docs
- **Architecture bootstrap**: most of May was heavy lifting to get infra running (ECS, Cognito, CI/CD, NPM client); team expects "cruise speed" from here
- **ML team onboarding**: ML team (Dushica, Ervin, Miguel Miranda) officially joined late May; data analysis started but questions about data provenance and structure still open

## Decisions / Agreements
- **Meeting cadence**: weekly planning at start of week + end-of-week close-out with Chris; daily with Chris limited to Ana Maximo + Jon; internal syncs Mon & Wed
- **Source of truth for tasks**: Jira (`PFI-*` board) — not Slack; Chris also tracking via Slack Lists
- **Architecture docs**: migrated from Confluence to Google Docs (José's call, 2026-05-29)
- **ML team to be added to `#loka-pacific-health-ventures` internal channel** (José requested, 2026-05-26)
- **Brand + website prototype tracked in Jira** under the same board (`PFI-91`, `PFI-92`)
- **Azure SSO for staff login** agreed as next step for Jon + Dejan
- **Phone numbers must be US-based** (standardized via E164 in BE)
- **AI tooling (GitHub Copilot + Claude Code)**: approved by client per Sushmitha (2026-04-23)
- **Jon's Fridays off** (microvacations for vacation balance); Fridays are no-meeting days for the team

## Open Items / Blockers
- **Dejan** → Update env variables (`PFI-118`) and fix Cognito permissions for ECS ECS access to admin methods (`PFI-117`) — this is **mandatory for the base system to work**
- **Azure ID client** for staff SSO login — Jon + Dejan
- **DNS migration** to Route53 — Jon + Dejan + Chris coordination needed
- **Data lake vs SQL decision** — open; José flagged Dorus data dump scale (activities 236K rows, activity_history 2.3M rows) as potentially too large for the main app DB
- **Cubigo data questions** — Dushica asked Nick whether `activities.csv` is the same source as the POC export (2026-06-01, unanswered)
- **Buck Institute involvement** — what is Loka's role? Possibly a separate SOW; José flagged it as unclear
- **Device procurement** — iPads + Android tablets for FE (Davor), testing devices for QA (Marija/Elena); pending client confirmation on spec
- **QA column in Jira** — Marija asked for it to be created for QA validation workflow
- **TestRail + Jira integration** ticket created (`PFI-29`)
- **README files missing** for some repos — José flagged as mandatory for handover

## Active People
| Name | Slack handle / role | What they're focused on |
|------|---------------------|------------------------|
| Ana Maximo | PM | Stakeholder mgmt, sprint visibility docs, Jira board, client comms |
| Jon Trigueiro | BE Tech Lead | Django backend, CI/CD, Cognito, NPM client for FE |
| Dejan Karadjinski | DevOps | AWS IaC, ECS, Cognito permissions, CI/CD pipelines |
| Tamara | BE | Onboarding assessment routes, backend features |
| Davor | FE (Resident App) | Login/onboarding flow, re-registration screen |
| Paolo / Stefanija | FE | Frontend (both apps) |
| Ivan Krstev | FE | NPM client for FE → BE API |
| Madalena | Design | Figma designs, UseBerry user testing, branding |
| Dushica | ML TL | Data analysis, Dorus data dump, Cubigo data questions |
| Ervin / Miguel Miranda | ML | Data analysis |
| Marija Dimoska / Elena G. | QA | Test case definition, Jira QA column, device procurement |
| José Pereira | Tech Lead | Architecture, cross-team alignment, data concerns, roadmap |
| Chris Furmanski | Client (PHV) | Visibility, priorities, product direction |
| Nick Lindberg | Client (HumanGood) | Cubigo data dumps and API access |
| Todd Austin | Client (PHV) | Design feedback on staff app |
| Sushmitha Regulapati | Loka Sales/Engagement | SOW coordination, ML team onboarding |

## GitHub Repos
- `LokaHQ/pacific_health_be_focus_core` — Django backend
- `LokaHQ/pacific_health_iac` — Infrastructure as Code
- `LokaHQ/pacific_health_fe_focus_forward` — Resident app (Focus Forward)
- `LokaHQ/pacific_health_fe_focus_activate` — Staff app (Focus Activate)
- `LokaHQ/loka-pacific-health-sow3` — prior SOW reference

## Dev Environment
- Admin: https://app-dev.focushealthspan.com/admin/ (user: `loka.staff`, pass: 1Password)
- Swagger: https://app-dev.focushealthspan.com/api/docs
