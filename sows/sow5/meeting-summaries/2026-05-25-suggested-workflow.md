---
date: 2026-05-25
sow: sow5
attendees: [Ana Maximo, Jon Trigueiro, Jose Pereira, chris@pac.vc, todd@focushealthspan.com]
type: client
---

# Focus Implementation — Go Through Suggested Workflow — 2026-05-25

## Key Takeaways
- **B2B pricing confirmed**: $20/resident/month operator pricing model
- **Product priority order**: resident app → staff app → insights platform
- **Multi-tenant infrastructure**: multi-tenant at the logic layer using infrastructure as code; replicate resources per operator as needed
- **August pilot strategy**: mock data to accelerate frontend; event-based triggers and offline capabilities for facility connectivity issues
- **Community amenities**: LOW priority (Cubigo already handles this)
- **Cognitive training**: HIGH priority for August
- José Pereira joining the project and reviewing architecture

## Decisions Made
- Operator pricing: $20/resident/month
- Development priority: resident app first, then staff, then insights
- Multi-tenant architecture confirmed (logic layer, not infrastructure duplication)
- August pilot: mock data to unblock frontend development

## Action Items

| Action | Owner | Due |
|--------|-------|-----|
| Evaluate provided data source document; align on development goals | Team | ASAP |
| Update branding prototypes to include current logo | Madalena Saraiva | ASAP |
| Review resident data samples received from Chris | José Pereira | ASAP |
| Share activity management design files to Chris for feedback | Ana Maximo | ASAP |
| Evaluate submitted design files | C Fur | ASAP |

## Notes

José Pereira formally joined this session. $20/resident/month B2B pricing confirmed. Clear priority ordering established for the three product surfaces. Multi-tenant architecture confirmed for scalability.
