# PlayFab (playfab)

PlayFab is Microsoft Azure's backend-as-a-service for live games. PlayFab exposes a large REST API surface (Client, Server, Admin, Authentication, CloudScript, Multiplayer, Economy v2, Matchmaking, Insights, Groups, Data, Profiles, Events, Localization) plus first-party SDKs for Unity, Unreal, Cocos, Phaser, JavaScript, C++, C#, Java, Lua, Objective-C, and Python. Every PlayFab game (a "title") gets its own scoped subdomain at https://[titleId].playfabapi.com. Sessions, identity, progression, inventory, leaderboards, segmentation, A/B testing, push, scheduled tasks, CloudScript (Azure Functions), and PlayFab Multiplayer Servers all run on this surface. PlayFab is operated as part of Azure Gaming and the documentation lives at learn.microsoft.com/en-us/gaming/playfab.

**APIs.json:** [https://playfab.com](https://playfab.com)

## Scope

- **Type:** Index
- **Access:** 3rd-Party

## Tags

- Authentication
- Azure
- Backend
- BaaS
- CloudScript
- Economy
- Game Backend
- Game Development
- Games
- Leaderboards
- Matchmaking
- Microsoft
- Multiplayer
- PlayFab
- REST

## Timestamps

- **Created:** 2024-01-01
- **Modified:** 2026-05-30

## APIs

### PlayFab Client API

The PlayFab Client API is the player-facing REST surface used by game clients for login, account linking, virtual currency, inventory, friends, leaderboards, statistics, player data, cloud script execution, multiplayer session lookup, push registration, segmentation triggers, and analytics events. It is scoped per-title at https://[titleId].playfabapi.com/Client and authenticated with a session ticket issued from a Login* call.

- **Human URL:** [https://learn.microsoft.com/en-us/rest/api/playfab/client/](https://learn.microsoft.com/en-us/rest/api/playfab/client/)
- **Base URL:** `https://titleId.playfabapi.com/Client`

#### Tags

- Authentication
- Client
- Leaderboards
- Players

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/rest/api/playfab/client/)
- [Authentication](https://learn.microsoft.com/en-us/gaming/playfab/sdks/playfab-authentication)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab Server API

The PlayFab Server API is the server-trusted REST surface for custom game servers and trusted backends. It mirrors much of the Client API but operates with the title's developer secret key and can act on any player, grant items, adjust currencies, modify read-only data, and issue server-authoritative writes.

- **Human URL:** [https://learn.microsoft.com/en-us/rest/api/playfab/server/](https://learn.microsoft.com/en-us/rest/api/playfab/server/)
- **Base URL:** `https://titleId.playfabapi.com/Server`

#### Tags

- Game Servers
- Server
- Trusted

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/rest/api/playfab/server/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab Admin API

The PlayFab Admin API is the privileged REST surface for studio and ops tooling. It covers title configuration, virtual currency catalogs, catalog items, store configuration, content (CDN) uploads, segments, tasks, policies, players (ban, refund, reset), and CloudScript revisions. Authenticated with the title developer secret key.

- **Human URL:** [https://learn.microsoft.com/en-us/rest/api/playfab/admin/](https://learn.microsoft.com/en-us/rest/api/playfab/admin/)
- **Base URL:** `https://titleId.playfabapi.com/Admin`

#### Tags

- Admin
- LiveOps
- Tooling

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/rest/api/playfab/admin/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab Authentication API

The PlayFab Authentication API issues and validates entity tokens used by the Entity Programming Model that underlies CloudScript using Azure Functions, Groups, Data, Profiles, Events, and Multiplayer. Entity tokens scope calls to a master player, character, title, group, or namespace entity.

- **Human URL:** [https://learn.microsoft.com/en-us/rest/api/playfab/authentication/](https://learn.microsoft.com/en-us/rest/api/playfab/authentication/)
- **Base URL:** `https://titleId.playfabapi.com/Authentication`

#### Tags

- Authentication
- Entity
- Identity
- Tokens

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/rest/api/playfab/authentication/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab CloudScript API

PlayFab CloudScript runs server-authoritative game logic in PlayFab. Modern CloudScript using Azure Functions registers Azure Function endpoints that can be invoked from clients or servers via ExecuteFunction. Legacy CloudScript runs JavaScript revisions stored in the title.

- **Human URL:** [https://learn.microsoft.com/en-us/rest/api/playfab/cloudscript/](https://learn.microsoft.com/en-us/rest/api/playfab/cloudscript/)
- **Base URL:** `https://titleId.playfabapi.com/CloudScript`

#### Tags

- Azure Functions
- CloudScript
- Serverless

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/rest/api/playfab/cloudscript/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab Multiplayer API

The PlayFab Multiplayer API powers PlayFab Multiplayer Servers (managed game server hosting on Azure), Party (low-latency voice and data networking), Lobby, and matchmaking server build management.

- **Human URL:** [https://learn.microsoft.com/en-us/rest/api/playfab/multiplayer/](https://learn.microsoft.com/en-us/rest/api/playfab/multiplayer/)
- **Base URL:** `https://titleId.playfabapi.com/Multiplayer`

#### Tags

- Game Servers
- Lobby
- Multiplayer
- Party

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/rest/api/playfab/multiplayer/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab Matchmaking API

The PlayFab Matchmaking API exposes ticket-based matchmaking, queue management, match results, and matchmaking rule configuration on top of PlayFab Multiplayer.

- **Human URL:** [https://learn.microsoft.com/en-us/rest/api/playfab/matchmaker/](https://learn.microsoft.com/en-us/rest/api/playfab/matchmaker/)
- **Base URL:** `https://titleId.playfabapi.com/Match`

#### Tags

- Matchmaking
- Multiplayer
- Queues

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/rest/api/playfab/matchmaker/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab Economy (Catalog / Inventory) API

PlayFab Economy v2 is the modern catalog, inventory, store, and virtual-currency surface. It covers catalog item authoring, inventory transactions, transactional and subscription stores, item search, and content review workflows for UGC.

- **Human URL:** [https://learn.microsoft.com/en-us/gaming/playfab/features/economy-v2/](https://learn.microsoft.com/en-us/gaming/playfab/features/economy-v2/)
- **Base URL:** `https://titleId.playfabapi.com/Catalog`

#### Tags

- Catalog
- Currency
- Economy
- Inventory
- Store
- UGC

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/gaming/playfab/features/economy-v2/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab Data API

The PlayFab Data API stores arbitrary file and object data attached to any entity (player, title, character, group). It exposes GetFiles, GetObjects, InitiateFileUploads, AbortFileUploads, FinalizeFileUploads, SetObjects, and DeleteFiles, used for save games, UGC blobs, and per-entity JSON state.

- **Human URL:** [https://learn.microsoft.com/en-us/rest/api/playfab/data/](https://learn.microsoft.com/en-us/rest/api/playfab/data/)
- **Base URL:** `https://titleId.playfabapi.com/File`

#### Tags

- Data
- Entity
- Files
- Save Data

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/rest/api/playfab/data/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab Groups API

The PlayFab Groups API supports guilds, clans, parties, and other player-managed organizations on the Entity model with roles, memberships, applications, and invitations.

- **Human URL:** [https://learn.microsoft.com/en-us/rest/api/playfab/groups/](https://learn.microsoft.com/en-us/rest/api/playfab/groups/)
- **Base URL:** `https://titleId.playfabapi.com/Group`

#### Tags

- Clans
- Groups
- Guilds
- Social

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/rest/api/playfab/groups/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab Profiles API

The PlayFab Profiles API reads and writes Entity Profiles, including display name, language, lineage, and per-entity policies (ACLs) used across the Entity-model APIs.

- **Human URL:** [https://learn.microsoft.com/en-us/rest/api/playfab/profiles/](https://learn.microsoft.com/en-us/rest/api/playfab/profiles/)
- **Base URL:** `https://titleId.playfabapi.com/Profile`

#### Tags

- Entity
- Permissions
- Profiles

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/rest/api/playfab/profiles/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab Events API

The PlayFab Events API writes PlayStream and custom telemetry events into PlayFab's pipeline for downstream segmentation, rules, and Insights analytics.

- **Human URL:** [https://learn.microsoft.com/en-us/rest/api/playfab/events/](https://learn.microsoft.com/en-us/rest/api/playfab/events/)
- **Base URL:** `https://titleId.playfabapi.com/Event`

#### Tags

- Analytics
- Events
- PlayStream
- Telemetry

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/rest/api/playfab/events/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab Insights API

PlayFab Insights is the managed analytics surface (built on Azure Data Explorer / Kusto) for querying telemetry generated by PlayFab titles. The Insights API manages Insights performance levels and submits analytics queries.

- **Human URL:** [https://learn.microsoft.com/en-us/gaming/playfab/features/analytics/insights/](https://learn.microsoft.com/en-us/gaming/playfab/features/analytics/insights/)
- **Base URL:** `https://insights.playfab.com`

#### Tags

- Analytics
- Insights
- Kusto
- Reporting

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/gaming/playfab/features/analytics/insights/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### PlayFab Localization API

The PlayFab Localization API returns the set of languages supported by the title and is used by clients to negotiate locale.

- **Human URL:** [https://learn.microsoft.com/en-us/rest/api/playfab/localization/](https://learn.microsoft.com/en-us/rest/api/playfab/localization/)
- **Base URL:** `https://titleId.playfabapi.com/Locale`

#### Tags

- i18n
- Localization

#### Properties

- [Documentation](https://learn.microsoft.com/en-us/rest/api/playfab/localization/)
- [Postman Collection](collections/playfab.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/playfab.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://playfab.com)
- [Portal](https://developer.playfab.com)
- [Documentation](https://learn.microsoft.com/en-us/gaming/playfab/)
- [API Reference](https://learn.microsoft.com/en-us/rest/api/playfab/)
- [SDK](https://learn.microsoft.com/en-us/gaming/playfab/sdks/)
- [Getting Started](https://learn.microsoft.com/en-us/gaming/playfab/personas/developer)
- [Pricing](https://learn.microsoft.com/en-us/gaming/playfab/features/pricing/)
- [Release Notes](https://learn.microsoft.com/en-us/gaming/playfab/personas/release-notes)
- [Status](https://status.playfab.com)
- [Forum](https://community.playfab.com)
- [GitHub Organization](https://github.com/PlayFab)
- [Blog](https://blog.playfab.com)
- [Terms of Service](https://www.microsoft.com/en-us/servicesagreement/)
- [Privacy Policy](https://privacy.microsoft.com/en-us/privacystatement)
- [X (Twitter)](https://x.com/AzurePlayFab)
- [LinkedIn](https://www.linkedin.com/showcase/microsoft-azure)
- [Review](review.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
