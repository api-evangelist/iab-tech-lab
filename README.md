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

## What is in this profile

- **openapi/** — OpenDirect 1.5.1 (Swagger 2.0, 51 ops), Ad Seller System API (OpenAPI 3.1, 87 ops), Ad Buyer Agent API (14 ops), IAB Agentic Advertising API (13 ops) — verbatim from the two IAB Tech Lab GitHub organizations (originals in `openapi/_original/`).
- **grpc/** — OpenRTB 2.6-202606 protobuf, AdCOM 1.0 protobufs, Agentic RTB Framework gRPC service.
- **xsd/** — VAST 4.1 / 4.2 / 4.4 and VMAP 1.0 XML Schemas. **json-schema/** — sixteen agentic primitives.
- **mcp/** — the three self-hosted MCP servers (seller-agent 46 tools, OpenDirect 33 tools with inputSchemas, ARTF) and a tool-to-REST crosswalk. No IAB Tech Lab-hosted MCP or A2A endpoint exists.
- **conventions/, errors/, lifecycle/, conformance/, changelog/, cli/, data-model/, packages/, plans/, rate-limits/, skills/, llms/, overlays/, authentication/, scopes/, security/, well-known/** — the runtime-semantics tier derived from those contracts and the provider's docs.
- The only hosted API, the Supply Chain API, sits behind the Tools Portal login; its contract could not be read.
