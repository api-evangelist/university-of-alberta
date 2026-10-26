# University of Alberta (university-of-alberta)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

The University of Alberta is a public research university in Edmonton, Alberta, Canada, and a member of the U15 Group of Canadian Research Universities. This repository catalogs the institution's public developer/API footprint as an [APIs.json](https://apisjson.org) provider profile.

**The university operates no public API product.** Re-profiled 2026-08-30 under the API Evangelist university pipeline, which settles *who operates* each surface before saving any contract. The only machine-readable contract the institution both writes and runs is its SAML 2.0 identity provider metadata at `login.ualberta.ca`. Everything else that looks like a University of Alberta API is a tenancy on someone else's platform.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-alberta/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-alberta-api-evangelist&utm_content=repo

## Type

- University / Public Research University / Index / Consumer / 3rd-Party

## Tags

Education, Higher Education, University, Canada, U15 Group of Canadian Research Universities, Research Data, Research Repository, Library, Identity Federation, OAI-PMH

## Surfaces

Every entry carries an operator. `institution` means the university runs the thing the artifact describes; `tenant` means the data is the university's but the contract and the platform are a vendor's.

- **SAML 2.0 Identity Provider Metadata** — *institution* — https://login.ualberta.ca/saml2/idp/metadata.php (200, `application/samlmetadata+xml`). entityID, IDPSSODescriptor, SSO/SLO endpoints, `shibmd:Scope` of `ualberta.ca`, `mdrpi:RegistrationInfo` `urn:mace:ualberta.ca`.
- **ERA — Education and Research Archive** — *tenant* — https://ualberta.scholaris.ca (DSpace 8.4 on Scholaris, the OCUL/Scholars Portal national service). REST at `/server/api`, OAI-PMH at `/server/oai/request`. The library's own `era.library.ualberta.ca` now redirects here.
- **Research data collection on Borealis** — *tenant* — https://borealisdata.ca/dataverse/ualberta (Canadian Dataverse Repository, OCUL/Scholars Portal). Five other institutions in the cohort point at the same host.
- **Library catalogue (Alma Z39.50 + Primo VE)** — *tenant* — `ualberta.alma.exlibrisgroup.com:1921` db `01UOA_INST`, documented by the library itself; discovery at https://search.library.ualberta.ca.
- **DOI registration (DataCite)** — *tenant* — client `ualberta.library`, 90,338 DOIs.
- **University of Alberta Library open source** — *institution* — https://github.com/ualbertalib, 138 public repositories, including its own OAI-PMH implementation (`oaisys`) and DSpace/DataCite client tooling.

## Conformance

- [conformance/university-of-alberta-conformance.yml](conformance/university-of-alberta-conformance.yml) — `education` regime standards, each with the URL fetched and the status it returned: `saml` (institution), `shibboleth` (partial, institution), `oai-pmh` (tenant), `datacite` (tenant), `z39.50` (tenant); `orcid` and `lti` unknown; `scim`, `oneroster`, `ed-fi`, `caliper`, `qti`, `crossref` absent.

## Plans

- [plans/university-of-alberta-plans-pricing.yml](plans/university-of-alberta-plans-pricing.yml)

## Rate Limits

- [rate-limits/university-of-alberta-rate-limits.yml](rate-limits/university-of-alberta-rate-limits.yml)

## FinOps

- [finops/university-of-alberta-finops.yml](finops/university-of-alberta-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-08-30

## Common Properties

- Website: https://www.ualberta.ca/
- Developer Portal (placeholder — no portal, no catalog, no key issuance): https://api.ualberta.ca/
- Identity Federation: https://login.ualberta.ca/saml2/idp/metadata.php
- Research Repository: https://ualberta.scholaris.ca/
- Open Data: https://www.ualberta.ca/en/library/research-support/open-data/index.html
- Library Catalog: https://search.library.ualberta.ca/
- Course Catalog (HTML only): https://apps.ualberta.ca/catalogue
- AI Policy: https://www.ualberta.ca/en/artificial-intelligence/artificial-intelligence-framework.html
- GitHub: https://github.com/ualbertalib
- Privacy: https://www.ualberta.ca/en/privacy.html
- LinkedIn: https://www.linkedin.com/school/university-of-alberta/

## Notes

- **Twenty files were removed on 2026-08-30.** Two OpenAPI documents describing the Borealis/Dataverse Native and Search API had been saved here as the university's, along with the pristine original, the refine report, and sixteen artifacts derived from them (collections, JSON Schema, JSON Structure, examples, rulesets, vocabulary, JSON-LD context, authentication and agentic-access). `borealisdata.ca` is a shared consortium host claimed by six institutions in this catalog; the contract is Dataverse's software API, not the University of Alberta's engineering. The tenant relationship is kept; the misattributed contract is not.
- `api.ualberta.ca` is live (HTTP 200) but is a placeholder stating the institution is "currently working to improve the way data is cataloged, shared, and governed", with an email address and nothing else. `data.ualberta.ca` serves the byte-identical page.
- ERA migrated off the library's own Jupiter application onto Scholaris; the library's DataCite record documents the March 2025 credential handover in its own words.
- There is no official course/timetable/SIS API. `apps.ualberta.ca/api` returns 404 and every `.json` path on the catalogue returns 410, which is why the third-party UAlberta course APIs that exist are HTML scrapers.
- The library's Open Journal Systems installation is gone — `journals.library.ualberta.ca` 302s to a library publishing page — so there is no institution-operated Crossref depositing surface.
- `library.ualberta.ca/peel/api` returns HTTP 200 but the body is the generic library page: a soft-404, not a surface.
- No endpoints were fabricated. Every surface above was probed live on 2026-08-30 and every status code is recorded in `x-coverage.evidence` in `apis.yml`.

## Maintainers

- Kin Lane — kin@apievangelist.com
