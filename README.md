# IAB Tech Lab

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

IAB Technology Laboratory (IAB Tech Lab) is the non-profit consortium that writes the technical standards the digital advertising supply chain runs on — OpenRTB (real-time bidding), AdCOM, OpenDirect (programmatic direct), VAST and VMAP (video ad serving), the Transparency and Consent Framework and Global Privacy Platform (consent signals), ads.txt, app-ads.txt and sellers.json (supply-chain transparency), the Open Measurement SDK and the content/audience/ad-product taxonomies. Its machine-readable contracts are published in the open on GitHub: an OpenRTB 2.x Protocol Buffers definition, the AdCOM protobuf, an OpenDirect Swagger specification, VAST XSDs, and an agentic-advertising stack (buyer-agent, seller-agent, Deals API, Agentic RTB Framework gRPC) that ships OpenAPI 3.1 contracts, JSON Schema primitives, MCP servers and A2A agent cards as reference implementations. The Tech Lab Tools Portal and its Core API sit behind a member login.

**Areas:** Company · Advertising · AdTech · Standards · Programmatic · Real-Time Bidding · Consent · Privacy · Video Ads · Agentic Advertising · Non-Profit

## IAB Tech Lab on APIs.io

Everything profiled for IAB Tech Lab is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/iab-tech-lab/](https://apis.io/providers/iab-tech-lab/)** — or go straight to one of the APIs or properties below.

### APIs (43)

- [OpenRTB 2.x Protocol](https://apis.io/apis/iab-tech-lab/openrtb/) — OpenRTB is the real-time bidding protocol between ad exchanges and bidders. IAB Tech Lab publishes the 2.x specification (current release 2.6-202606) with a…
- [AdCOM Protobuf](https://apis.io/apis/iab-tech-lab/adcom/) — Advertising Common Object Model (AdCOM) 1.0 is the shared object layer beneath OpenRTB 3.0, OpenDirect and the Ad Management API — media (ads, assets),…
- [Agentic RTB Framework gRPC](https://apis.io/apis/iab-tech-lab/agentic-rtb-framework/) — The Agentic Real-Time Framework (ARTF) 1.0 defines gRPC extension points an exchange calls during an auction so that agents can mutate the bidstream. The…
- [VAST and VMAP Schemas](https://apis.io/apis/iab-tech-lab/vast/) — Video Ad Serving Template (VAST) is the XML contract between video players and ad servers; VMAP (Video Multiple Ad Playlist) schedules ad breaks around…
- [Supply Chain API](https://apis.io/apis/iab-tech-lab/supply-chain-api/) — IAB Tech Lab's hosted, subscription API for aggregated supply-chain data: crawled and validated ads.txt, app-ads.txt and sellers.json files, plus the…
- [IAB Tech Lab A2a API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-a2a-api/) — The A2a API from IAB Tech Lab — 1 operation(s) for a2a.
- [IAB Tech Lab Accounts API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-accounts-api/) — The Accounts API from IAB Tech Lab — 2 operation(s) for accounts.
- [IAB Tech Lab Agent Registry API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-agent-registry-api/) — A2A agent discovery and trust management
- [IAB Tech Lab Approvals API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-approvals-api/) — Human-in-the-loop approval workflow
- [IAB Tech Lab Assignments API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-assignments-api/) — The Assignments API from IAB Tech Lab — 3 operation(s) for assignments.
- [IAB Tech Lab Audience API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-audience-api/) — The Audience API from IAB Tech Lab — 1 operation(s) for audience.
- [IAB Tech Lab Audit API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-audit-api/) — Order audit logs and operational reports
- [IAB Tech Lab Authentication API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-authentication-api/) — API key lifecycle management
- [IAB Tech Lab Bookings API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-bookings-api/) — Campaign booking workflow lifecycle
- [IAB Tech Lab Bulk Operations API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-bulk-operations-api/) — Batch deal create/update/cancel
- [IAB Tech Lab Buyer Orders API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-buyer-orders-api/) — The Buyer Orders API from IAB Tech Lab — 2 operation(s) for buyer orders.
- [IAB Tech Lab Change Requests API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-change-requests-api/) — The Change Requests API from IAB Tech Lab — 8 operation(s) for change requests.
- [IAB Tech Lab Change Requests Lines API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-change-requests-lines-api/) — The Change Requests Lines API from IAB Tech Lab — 2 operation(s) for change requests lines.
- [IAB Tech Lab Core API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-core-api/) — Health check and API root
- [IAB Tech Lab Creatives API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-creatives-api/) — The Creatives API from IAB Tech Lab — 2 operation(s) for creatives.
- [IAB Tech Lab Curators API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-curators-api/) — The Curators API from IAB Tech Lab — 3 operation(s) for curators.
- [IAB Tech Lab Deal Booking API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-deal-booking-api/) — Quote-to-deal booking (IAB Deals API v1.0)
- [IAB Tech Lab Deal Performance API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-deal-performance-api/) — Deal delivery and performance metrics
- [IAB Tech Lab Deals API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-deals-api/) — The Deals API from IAB Tech Lab — 3 operation(s) for deals.
- [IAB Tech Lab Discovery API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-discovery-api/) — Natural language inventory discovery
- [IAB Tech Lab Events API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-events-api/) — Event bus query endpoints
- [IAB Tech Lab Health API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-health-api/) — Service health and readiness
- [IAB Tech Lab Lines API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-lines-api/) — The Lines API from IAB Tech Lab — 6 operation(s) for lines.
- [IAB Tech Lab Media Kit API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-media-kit-api/) — Public media kit and package catalog
- [IAB Tech Lab Negotiation API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-negotiation-api/) — Multi-round price negotiation
- [IAB Tech Lab Negotiations API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-negotiations-api/) — The Negotiations API from IAB Tech Lab — 2 operation(s) for negotiations.
- [IAB Tech Lab Orders API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-orders-api/) — The Orders API from IAB Tech Lab — 7 operation(s) for orders.
- [IAB Tech Lab Organizations API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-organizations-api/) — The Organizations API from IAB Tech Lab — 2 operation(s) for organizations.
- [IAB Tech Lab Packages API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-packages-api/) — Package management (authenticated/admin)
- [IAB Tech Lab Pricing API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-pricing-api/) — Tiered pricing with buyer context
- [IAB Tech Lab Products API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-products-api/) — The Products API from IAB Tech Lab — 6 operation(s) for products.
- [IAB Tech Lab Proposals API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-proposals-api/) — Proposal submission and evaluation
- [IAB Tech Lab Quotes API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-quotes-api/) — The Quotes API from IAB Tech Lab — 2 operation(s) for quotes.
- [IAB Tech Lab Registry API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-registry-api/) — The Registry API from IAB Tech Lab — 1 operation(s) for registry.
- [IAB Tech Lab Reporting API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-reporting-api/) — The Reporting API from IAB Tech Lab — 7 operation(s) for reporting.
- [IAB Tech Lab Sessions API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-sessions-api/) — Multi-turn buyer conversation sessions
- [IAB Tech Lab Supply Chain API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-supply-chain-api/) — Supply chain transparency (sellers.json-like self-description)
- [IAB Tech Lab .well Known API](https://apis.io/apis/iab-tech-lab/iab-tech-lab-well-known-api/) — The .well Known API from IAB Tech Lab — 1 operation(s) for .well known.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [iab-tech-lab-mcp.yml](https://apis.io/servers/iab-tech-lab/iab-tech-lab-mcp-yml/)

#### JSON Schema (16)

The data models the API reads and writes.

- [Account](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-account/)
- [Agent](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-agent/)
- [Assignment](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-assignment/)
- [ChangeRequest](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-changerequest/)
- [ConsentContext](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-consentcontext/)
- [Creative](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-creative/)
- [CreativeApproval](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-creativeapproval/)
- [Deal](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-deal/)
- [DecisionRecord](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-decisionrecord/)
- [Line](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-line/)
- [MediaKit](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-mediakit/)
- [Negotiation](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-negotiation/)
- [Order](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-order/)
- [Organization](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-organization/)
- [Product](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-product/)
- [Proposal](https://apis.io/schemas/iab-tech-lab/iab-tech-lab-agentic-primitive-proposal/)

#### Overlays (4)

OpenAPI overlays, including conversational phrasing for each operation.

- [Iab Tech Lab Agentic Advertising Api Overlay](https://apis.io/overlays/iab-tech-lab/iab-tech-lab-agentic-advertising-api-overlay/)
- [Iab Tech Lab Buyer Agent Overlay](https://apis.io/overlays/iab-tech-lab/iab-tech-lab-buyer-agent-overlay/)
- [Iab Tech Lab Opendirect 1 5 1 Overlay](https://apis.io/overlays/iab-tech-lab/iab-tech-lab-opendirect-1-5-1-overlay/)
- [Iab Tech Lab Seller Agent Overlay](https://apis.io/overlays/iab-tech-lab/iab-tech-lab-seller-agent-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Iab Tech Lab Authentication](https://apis.io/security/iab-tech-lab/iab-tech-lab-authentication/)
- [Iab Tech Lab Domain Security](https://apis.io/security/iab-tech-lab/iab-tech-lab-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Iab Tech Lab Scopes](https://apis.io/scopes/iab-tech-lab/iab-tech-lab-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Iab Tech Lab Plans Pricing](https://apis.io/plans/iab-tech-lab/iab-tech-lab-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Iab Tech Lab Rate Limits](https://apis.io/rate-limits/iab-tech-lab/iab-tech-lab-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://iabtechlab.com/)
- [Documentation](https://iabtechlab.com/standards/)
- [Pricing](https://iabtechlab.com/membership/)
- [Support](https://iabtechlab.com/contact-us/)
- [Blog](https://iabtechlab.com/category/blog/)
- [Terms of service](https://iabtechlab.com/terms-of-use/)
- [Privacy policy](https://iabtechlab.com/privacy-policy/)
- [GitHub](https://github.com/IABTechLab)

## API Evangelist rating

**Kin Score 50.8** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 62.5 |
| Contract quality | 48.8 |
| Contract governance | 18.2 |
| Operational transparency | 18.4 |
| Developer ergonomics | 61.3 |
| Access clarity | 52.6 |

**Agent readiness 37.6** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | documented (partial credit) |
| Auth Clarity | bearer (partial credit) |
| Idempotency | verified |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 34.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/iab-tech-lab/](https://apis.io/providers/iab-tech-lab/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for IAB Tech Lab: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/iab-tech-lab/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
