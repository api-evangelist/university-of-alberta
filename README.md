# University of Alberta (university-of-alberta)

The University of Alberta is a public research university in Edmonton, Alberta, Canada, ranked #67 in the QS World University Rankings 2025. This repository catalogs the institution's public developer/API footprint as an [APIs.json](https://apisjson.org) provider profile. The footprint is modest and decentralized: the central `api.ualberta.ca` site is a pre-launch placeholder, with the strongest confirmed programmatic access being research data through the Borealis (Canadian Dataverse) repository.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-alberta/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-alberta-api-evangelist&utm_content=repo

## Type

- Index / Consumer / 3rd-Party

## Tags

Education, Higher Education, University, Research Data, Open Data, Library, Canada

## APIs

- **University of Alberta Research Data (Borealis Dataverse) API** — REST Native/Search API for the UAlberta research data collection on Borealis. Docs: https://borealisdata.ca/guides/en/latest/api/index.html | Collection: https://borealisdata.ca/dataverse/ualberta
- **University of Alberta Borealis OAI-PMH Metadata Harvesting** — OAI-PMH endpoint for harvesting published UAlberta dataset metadata. Docs: https://borealisdata.ca/guides/en/latest/admin/discoverability.html
- **University of Alberta Library Open Source (GitHub)** — Library open-source code and API-integration tooling. Docs: https://www.library.ualberta.ca/about/open-data | GitHub: https://github.com/ualbertalib

## Plans

- [plans/university-of-alberta-plans-pricing.yml](plans/university-of-alberta-plans-pricing.yml)

## Rate Limits

- [rate-limits/university-of-alberta-rate-limits.yml](rate-limits/university-of-alberta-rate-limits.yml)

## FinOps

- [finops/university-of-alberta-finops.yml](finops/university-of-alberta-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.ualberta.ca/
- Developer Portal (placeholder / pre-launch): https://api.ualberta.ca/
- GitHub: https://github.com/ualbertalib
- LinkedIn: https://www.linkedin.com/school/university-of-alberta/

## Notes

- `api.ualberta.ca` is live (HTTP 200) but is only a placeholder stating the institution is "currently working to improve the way data is cataloged, shared, and governed." No self-service developer portal or documented institutional APIs exist yet.
- Borealis is a shared national platform (Scholars Portal / OCUL); the UAlberta presence is the institution's research data collection (subtree `ualberta`) on it. The Search API and OAI-PMH endpoint were both probed live (HTTP 200).
- There is no official course/timetable/SIS API. The course catalogue and Bear Tracks are web-only. A third-party unofficial scraping API (Heroku) is dead (HTTP 404) and is not cataloged as an institutional API.
- The legacy `dataverse.library.ualberta.ca` host did not resolve (migrated to Borealis).
- No endpoints were fabricated; every cataloged API was verified live on 2026-06-03.

## Maintainers

- Kin Lane — kin@apievangelist.com
