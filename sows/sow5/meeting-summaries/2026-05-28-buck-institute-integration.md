---
date: 2026-05-28
sow: sow5
attendees: [Ana Maximo, Jon Trigueiro, Jose Pereira, chris@pac.vc, todd@focushealthspan.com]
type: client
---

# Focus Implementation — Discuss Buck Institute Integration — 2026-05-28

## Key Takeaways
- **Not rebuilding the Buck engine in 2026**: Buck team treated as a development stream under Loka's direction; their engine is "ML Team 2"
- **Loka ingests raw Tempest data**: Focus Healthspan system will ingest and store raw Tempest IDAT files (2 IDAT + 1 VDF annotation file, ~100MB each); Buck accesses from within the managed environment — Loka does NOT hand off the APIs to Buck
- **Push not pull**: Loka pushes data to Buck for analysis; Buck does not pull directly from Loka's data sources
- **Three data inputs**: genetic (Tempest IDAT), blood biomarkers (Junction), demographics — first two require consent and can each run independently with demographics
- **Plug-and-play architecture**: Buck is the first example of a modular "engine bay" — future engines (nutrition, fitness) will follow the same input/output pattern
- **Engine must work without Buck data**: genetic/blood results take up to 4 weeks; system must generate recommendations from demographics/wearables while waiting
- **Buck components**: "Vault" (genetic data storage) and "Adidal" (analysis engine) — delivered via CloudFormation scripts into Loka's environment
- **Multi-stage VPC**: Jon and José to propose dev/staging/prod environment architecture for the Buck integration
- **JSON taxonomy**: need to define input/output specs for data exchange (nested JSON for standard data; IDAT files via S3)
- **Wearable data**: attractive long-term via Junction, but explicitly deferred — start with genetics + blood + demographics only
- **AirVail historical context**: this project is essentially AirVail 2.0 — prior company that tried to do this with human coaching; AI replaces the human coach to make it scalable

## Decisions Made
- Buck Engine: not rebuilt in 2026; Buck team treated as directed development stream
- Loka ingests raw Tempest data and stores it; Buck accesses from within managed environment
- Loka owns and controls all data ingestion (not Buck); push model to Buck for analysis
- System must function without Buck data (fallback to demographics/wearables)
- Plug-and-play modular engine architecture adopted

## Action Items

| Action | Owner | Due |
|--------|-------|-----|
| Propose multi-stage VPC environment architecture for Buck integration | Jon Trigueiro, José Pereira | ASAP |
| Define data taxonomy: input/output specs, file formats (nested JSON, IDAT) | Jon Trigueiro, José Pereira | ASAP |
| Review Tempest IDAT sample files and Junction sandbox API documentation | Jon Trigueiro, José Pereira | ASAP |
| Send architecture/environment proposal to Buck | Jon Trigueiro | ASAP |
| Create high-level data flow diagram | Ana Maximo | ASAP |
| Pre-think internal architecture for data flow system | The group | ASAP |

## Notes

Deep-dive session on Buck Institute integration strategy. C Fur provided full historical context: project is AirVail 2.0, replacing human coaching with AI at scale. Key clarification: Loka controls all data ingestion — Buck does not call Tempest/Junction directly. Consent gates Buck data flow (no consent = no data sent to Buck, but recommendations still work from demographics). Jon and José first meeting together on this technical architecture. Very productive for aligning the new tech leads.
