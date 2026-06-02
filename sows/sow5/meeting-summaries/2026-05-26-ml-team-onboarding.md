---
date: 2026-05-26
sow: sow5
attendees: [Ana Maximo, Dushica Jankovikj, Jon Trigueiro, Miguel Miranda, Jose Pereira, Ervin Shaqiri, Dejan Karadjinski, chris@pac.vc]
type: client
---

# PHV Focus — ML Team Onboarding — 2026-05-26

## Key Takeaways
- **Existing codebase as starting point**: ML team (Dushica) will refactor as needed once backend team owns data operations
- **Two parallel workstreams**: (1) architecting system outputs, (2) driving data acquisition — run simultaneously
- **Rule-based vs LLM split**: rule-based logic for known patterns; LLMs to interpret biological and functional fitness markers
- **Clinical medication recommendations excluded**: explicitly out of scope
- **Missing profile data as triggers**: engine will prompt users to supply missing functional/genetic metrics to improve future recommendations
- **Cognitive training HIGH priority**: formally designated as high priority
- **Community amenities LOW priority**: Cubigo already handles this
- **Cell phone required**: user accounts require a valid cell phone number for identity verification
- **Jira tracking adopted for ML team**: all ML work items tracked on project Jira board

## Decisions Made
- Existing codebase accepted as starting point (with refactoring rights)
- Clinical medication recommendations excluded from product scope
- Cell phone number required for accounts
- Missing profile data used as recommendation triggers
- Cognitive training = high priority; community amenities = low priority
- ML team tracks work in Jira

## Action Items

| Action | Owner | Due |
|--------|-------|-----|
| Review previous ML documentation and system architecture | José Pereira | ASAP |
| Share implementation and data requirements documents | C Fur | ASAP |
| Audit JSON exports and data tables for missing info/discrepancies | Dushica Jankovikj | ASAP |
| Contact Nick for updated community attendance data | C Fur | ASAP |
| Prepare data gaps summary document | Dushica Jankovikj | ASAP |
| Review Buck Institute SOW | José Pereira, Jon Trigueiro | ASAP |
| Schedule team meeting for Buck Institute technical requirements | The group | ASAP |
| Analyze user roster for valid cell phone numbers | Jon Trigueiro | ASAP |
| Obtain sample file with resident functional/psychosocial test scores | C Fur | ASAP |
| Share initial recommendation ranking thoughts | C Fur | ASAP |
| Obtain Mocha scores and Brain HQ individual metrics for cognitive training | C Fur | ASAP |
| Create ML team epics and labels in Jira | Dushica Jankovikj | ASAP |

## Notes

ML team onboarding session. Dushica, Miguel, and Ervin brought up to speed on the recommendation engine architecture. Key tension: existing codebase may need significant refactoring once Jon's backend team takes over data operations. Mini data discovery phase to validate previous assumptions against actual Cubigo/JSON exports. Separate syncs to be established for ML engine development going forward.
