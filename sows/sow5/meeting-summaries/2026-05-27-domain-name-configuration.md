---
date: 2026-05-27
sow: sow5
attendees: [Ana Maximo, Dejan Karadjinski, Jon Trigueiro, chris@pac.vc]
type: client
---

# PHV Focus — Domain Name Configuration (GoDaddy → Route53) — 2026-05-27

## Key Takeaways
- **focuspan.com confirmed**: www.focuspan.com is the primary domain for all environments; subdomains for dev and prod
- **GoDaddy → AWS Route53 migration**: Dejan proposed and team approved moving DNS configuration to Route53; GoDaddy will no longer be the host
- **Automated export incomplete**: GoDaddy's automated DNS export missed records for Google Workspace and Figma — must be migrated manually
- **Dejan got delegated access**: C Fur gave Dejan delegated access to the GoDaddy account to handle remaining steps
- **Brief downtime expected**: name server change will cause a short period of web app downtime

## Decisions Made
- focuspan.com confirmed as the primary domain
- Domain infrastructure migrated to AWS Route53

## Action Items

| Action | Owner | Due |
|--------|-------|-----|
| Manually copy DNS records from GoDaddy into a text file and share for review | C Fur | ASAP |
| Transfer domain to AWS Route53 after gathering required DNS records | Dejan Karadjinski | ASAP |

## Notes

Short technical meeting (under 15 minutes). Primary outcome: domain confirmed, migration approach agreed, and Dejan unblocked with delegated GoDaddy access. The automated export gap (missing Google Workspace + Figma records) was the only complication — resolved by delegated manual access.
