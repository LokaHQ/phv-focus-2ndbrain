---
date: 2026-06-01
sow: sow5
attendees: [Ana Maximo, Jon Trigueiro, Tamara Ilieva, Davor Trifunov, Dejan Karadjinski, Stefanija Zdraveska, Ivan Krstev, Madalena Saraiva, Dushica Jankovikj, Ervin Shaqiri, Jose Pereira, Miguel Miranda, Elena Gramatikovska, Paolo Pecis, Marija Dimoska, Sushmitha Regulapati, chris@pac.vc, todd@focushealthspan.com]
type: client
---

# Loka <> PHV Focus — Weekly Planning — 2026-06-01

## Key Takeaways
- **All tasks in Jira**: Jira is now mandatory for all task tracking — no more Slack-only assignments
- **QA → staging → Chris review workflow**: features must pass internal QA, move to staging, then be assigned to Chris for final approval before shipping
- **Sprint 3 goal = fully connected app**: functional backend + frontend; not just UI screens — complete end-to-end flows
- **CodeMagic blocked**: billing not enabled — Davor reported as blocker for mobile CI/CD pipeline
- **Azure AD account needed for SSO**: Jon identified that SSO setup requires a Microsoft Azure AD account with a phone number; C Fur will create the account
- **Static recommendations in UI**: resident app will show static recommendations while ML engine is built; placeholder pattern confirmed
- **Website final version by Wednesday**: static build, no CMS — Anna and Bruno to deliver
- **Buck Institute architecture first step**: draft initial contract/diagram before engaging Buck — internal homework before external call
- **No new data in Jira from Chris yet**: C Fur confirmed closing tickets and assigning to Ana works as the tracking loop

## Decisions Made
- Jira = sole task tracking mechanism (not Slack)
- QA → staging → Chris review deployment workflow
- Sprint 3 scope: fully connected app (not partial)
- Website final version: Wednesday deadline
- Static recommendations displayed in UI pending ML engine completion
- C Fur to create Microsoft Azure AD account for SSO

## Action Items

| Action | Owner | Due |
|--------|-------|-----|
| Document steps for Microsoft Azure AD account creation and share with Chris | Dejan Karadjinski | ASAP |
| Draft list of infrastructure/architectural requirements for Buck Institute meeting | The group | ASAP |
| Review C Fur's project momentum notes to prepare for team meeting | The group | ASAP |

## Notes

Sprint 3 kickoff planning with full team. Key themes: workflow discipline (Jira mandatory), clear deployment chain (QA → staging → Chris), and two hard blockers surfaced — CodeMagic billing and Azure AD account. C Fur took ownership of the Azure AD account creation. Buck Institute pre-work assigned: draft architecture/contract before reaching out. Website on final stretch for Wednesday.
