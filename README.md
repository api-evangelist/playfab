# PlayFab

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

PlayFab is Microsoft Azure's backend-as-a-service for live games. PlayFab exposes a large REST API surface (Client, Server, Admin, Authentication, CloudScript, Multiplayer, Economy v2, Matchmaking, Insights, Groups, Data, Profiles, Events, Localization) plus first-party SDKs for Unity, Unreal, Cocos, Phaser, JavaScript, C++, C#, Java, Lua, Objective-C, and Python. Every PlayFab game (a "title") gets its own scoped subdomain at https://[titleId].playfabapi.com. Sessions, identity, progression, inventory, leaderboards, segmentation, A/B testing, push, scheduled tasks, CloudScript (Azure Functions), and PlayFab Multiplayer Servers all run on this surface. PlayFab is operated as part of Azure Gaming and the documentation lives at learn.microsoft.com/en-us/gaming/playfab.

**Areas:** Authentication · Microsoft Azure · Backend · Backend-as-a-Service · CloudScript · Economy · Game Backend · Game Development · Games · Leaderboards · Matchmaking · Microsoft

## PlayFab on APIs.io

Everything profiled for PlayFab is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/playfab/](https://apis.io/providers/playfab/)** — or go straight to one of the APIs or properties below.

### APIs (16)

- [PlayFab Client API](https://apis.io/apis/playfab/playfab-client-api/) — The PlayFab Client API is the player-facing REST surface used by game clients for login, account linking, virtual currency, inventory, friends,…
- [PlayFab Server API](https://apis.io/apis/playfab/playfab-server-api/) — The PlayFab Server API is the server-trusted REST surface for custom game servers and trusted backends. It mirrors much of the Client API but operates with…
- [PlayFab Admin API](https://apis.io/apis/playfab/playfab-admin-api/) — The PlayFab Admin API is the privileged REST surface for studio and ops tooling. It covers title configuration, virtual currency catalogs, catalog items,…
- [PlayFab Authentication API](https://apis.io/apis/playfab/playfab-entity-authentication-api/) — The PlayFab Authentication API issues and validates entity tokens used by the Entity Programming Model that underlies CloudScript using Azure Functions,…
- [PlayFab CloudScript API](https://apis.io/apis/playfab/playfab-cloudscript-api/) — PlayFab CloudScript runs server-authoritative game logic in PlayFab. Modern CloudScript using Azure Functions registers Azure Function endpoints that can be…
- [PlayFab Multiplayer API](https://apis.io/apis/playfab/playfab-multiplayer-api/) — The PlayFab Multiplayer API powers PlayFab Multiplayer Servers (managed game server hosting on Azure), Party (low-latency voice and data networking), Lobby,…
- [PlayFab Matchmaking API](https://apis.io/apis/playfab/playfab-matchmaking-api/) — The PlayFab Matchmaking API exposes ticket-based matchmaking, queue management, match results, and matchmaking rule configuration on top of PlayFab Multiplayer.
- [PlayFab Economy (Catalog / Inventory) API](https://apis.io/apis/playfab/playfab-economy-api/) — PlayFab Economy v2 is the modern catalog, inventory, store, and virtual-currency surface. It covers catalog item authoring, inventory transactions,…
- [PlayFab Data API](https://apis.io/apis/playfab/playfab-data-api/) — The PlayFab Data API stores arbitrary file and object data attached to any entity (player, title, character, group). It exposes GetFiles, GetObjects,…
- [PlayFab Groups API](https://apis.io/apis/playfab/playfab-groups-api/) — The PlayFab Groups API supports guilds, clans, parties, and other player-managed organizations on the Entity model with roles, memberships, applications,…
- [PlayFab Profiles API](https://apis.io/apis/playfab/playfab-profiles-api/) — The PlayFab Profiles API reads and writes Entity Profiles, including display name, language, lineage, and per-entity policies (ACLs) used across the…
- [PlayFab Events API](https://apis.io/apis/playfab/playfab-events-api/) — The PlayFab Events API writes PlayStream and custom telemetry events into PlayFab's pipeline for downstream segmentation, rules, and Insights analytics.
- [PlayFab Insights API](https://apis.io/apis/playfab/playfab-insights-api/) — PlayFab Insights is the managed analytics surface (built on Azure Data Explorer / Kusto) for querying telemetry generated by PlayFab titles. The Insights…
- [PlayFab Localization API](https://apis.io/apis/playfab/playfab-localization-api/) — The PlayFab Localization API returns the set of languages supported by the title and is used by clients to negotiate locale.
- [PlayFab Account API](https://apis.io/apis/playfab/playfab-account-api/) — PlayFab account metadata.
- [PlayFab Authentication API](https://apis.io/apis/playfab/playfab-authentication-api/) — Login, registration, and identity provider sign-in.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/playfab/](https://apis.io/graphqls/playfab/playfab-graphql/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Playfab Agentic Access](https://apis.io/agentic-access/playfab/playfab-agentic-access/)

#### Collections (3)

Postman and Open Collection request collections.

- [PlayFab Client API](https://apis.io/collections/playfab/open-playfab/)
- [PlayFab Client Account API](https://apis.io/collections/playfab/open-playfab-account-api/)
- [PlayFab Client Account Authentication API](https://apis.io/collections/playfab/open-playfab-authentication-api/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Playfab Authentication](https://apis.io/security/playfab/playfab-authentication/)
- [Playfab Domain Security](https://apis.io/security/playfab/playfab-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Playfab Plans Pricing](https://apis.io/plans/playfab/playfab-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Playfab Rate Limits](https://apis.io/rate-limits/playfab/playfab-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Playfab Finops](https://apis.io/finops/playfab/playfab-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://playfab.com)
- [Documentation](https://learn.microsoft.com/en-us/gaming/playfab/)
- [Getting started](https://learn.microsoft.com/en-us/gaming/playfab/personas/developer)
- [API reference](https://learn.microsoft.com/en-us/rest/api/playfab/)
- [Pricing](https://learn.microsoft.com/en-us/gaming/playfab/features/pricing/)
- [Blog](https://blog.playfab.com)
- [Terms of service](https://www.microsoft.com/en-us/servicesagreement/)
- [Privacy policy](https://privacy.microsoft.com/en-us/privacystatement)
- [GitHub](https://github.com/PlayFab)

## API Evangelist rating

**Kin Score 40.1** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 46.2 |
| Contract governance | 0.0 |
| Operational transparency | 26.3 |
| Developer ergonomics | 52.4 |
| Access clarity | 36.8 |

**Agent readiness 19.6** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
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

**Regulatory alignment 19.6** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/playfab/](https://apis.io/providers/playfab/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for PlayFab: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/playfab/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
