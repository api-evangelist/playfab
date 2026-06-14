# Azure PlayFab GraphQL Schema

## Overview

This conceptual GraphQL schema models the Azure PlayFab game backend REST API surface across all major service areas: Client, Server, Admin, Authentication, CloudScript, Multiplayer, Economy v2, Matchmaking, Insights, Groups, Data, Profiles, Events, and Localization.

PlayFab is Microsoft Azure's backend-as-a-service (BaaS) for live games. Every game title (identified by a `titleId`) gets its own scoped endpoint at `https://[titleId].playfabapi.com`. The schema below translates PlayFab's REST resources into a unified GraphQL type system that spans the full API surface.

Reference: https://learn.microsoft.com/en-us/rest/api/playfab/

---

## Schema File

[playfab-schema.graphql](playfab-schema.graphql)

---

## Type Coverage

### Entity Model (6 types)
| Type | Description |
|------|-------------|
| `EntityKey` | Typed key (`id` + `type`) used across the Entity Programming Model |
| `EntityType` | Named entity type descriptor |
| `EntityToken` | Short-lived token for entity-scoped API calls (Authentication API) |
| `EntityDetails` | Full entity descriptor including lineage chain |
| `EntityLineage` | Ancestry chain: master player → title player → character → group |
| `Entity` | Lightweight entity reference |

### Authentication & Login (6 types)
| Type | Description |
|------|-------------|
| `Auth` | Result of any login or token exchange |
| `AuthDetails` | Login request parameters |
| `Login` | Login request wrapper |
| `LoginResult` | Full login result including session ticket and entity token |
| `UserSettings` | Per-player device/attribution settings negotiated at login |
| `PlayerCombinedInfo` | Aggregated payload returned in `InfoRequestParameters` login responses |

### Player (6 types)
| Type | Description |
|------|-------------|
| `Player` | Core player/account record |
| `PlayerDetails` | Detailed account information including linked provider records |
| `PlayerData` | Mutable title-scoped key-value data bucket |
| `PlayerProfile` | Entity-profile-level record (Profiles API) |
| `PlayerStatistic` | Single named statistic value with version |
| `PlayerLocation` | Geographic location from session metadata |

### Identity Providers (6 types)
| Type | Description |
|------|-------------|
| `CustomId` | Developer-assigned custom identifier |
| `LinkedAccount` | External identity provider link |
| `EmailInfo` | Email address with verification status |
| `FacebookInfo` | Facebook account link |
| `GoogleInfo` | Google account link |
| `AppleInfo` | Sign in with Apple link |
| `XboxInfo` | Xbox Live account link |
| `SteamInfo` | Steam account link |

### CloudScript (4 types)
| Type | Description |
|------|-------------|
| `CloudScript` | Execution request (function name, parameters, revision selection) |
| `CloudScriptResult` | Full execution result including logs, timing, and error |
| `LogStatement` | Single log line emitted during CloudScript execution |
| `ScriptExecutionError` | Error detail from a failed CloudScript execution |

### Catalog & Economy (9 types)
| Type | Description |
|------|-------------|
| `ItemDetails` | Full catalog item descriptor |
| `CatalogConsumable` | Consumable behavior for an item |
| `CatalogContainer` | Container/loot-box behavior for an item |
| `CatalogBundle` | Bundle contents descriptor |
| `Catalog` | Top-level catalog with items list |
| `CatalogDetails` | Catalog metadata (default flag, size, timestamps) |
| `Version` | Versioned resource lifecycle record |
| `CatalogVersion` | Named catalog version reference |
| `Economy` | Economy operation request (grant, purchase, consume) |

### Store (5 types)
| Type | Description |
|------|-------------|
| `Store` | Store descriptor with item list |
| `StoreDetails` | Extended store record with timestamps |
| `StoreItem` | Single item listed in a store with override prices |
| `StoreMarketingData` | Display copy attached to a store |
| `StoreSource` | Source that created or populated the store |

### Virtual Currency & Inventory (4 types)
| Type | Description |
|------|-------------|
| `VirtualCurrency` | Virtual currency definition |
| `VirtualCurrencyGrant` | Grant operation result with balance after |
| `UserInventory` | Full player inventory including VC balances |
| `InventoryDetails` | Single inventory item instance |

### Economy Operations (3 types)
| Type | Description |
|------|-------------|
| `GrantItems` | Result of granting catalog items to a player |
| `RedeemCoupon` | Result of redeeming a coupon code |
| `TradeDetails` | Trade offer parameters |
| `Trade` | Active trade record with full lifecycle status |

### Leaderboards & Statistics (6 types)
| Type | Description |
|------|-------------|
| `Leaderboard` | Leaderboard query descriptor |
| `LeaderboardDetails` | Extended leaderboard including entries and reset time |
| `Entry` | Single leaderboard entry with player profile |
| `Rank` | Player rank on a named leaderboard |
| `Statistics` | Statistics container for a player |
| `StatisticVersion` | Versioned statistic definition with schedule |
| `Achievement` | Achievement definition tied to a statistic |

### Segments & Cohorts (3 types)
| Type | Description |
|------|-------------|
| `SegmentDetails` | Extended segment definition with filter and member count |
| `Segment` | Lightweight segment reference |
| `CohortDetails` | A/B testing cohort record |
| `UserSegment` | Segment membership record for an entity |

### Groups (4 types)
| Type | Description |
|------|-------------|
| `Group` | Group entity (guild, clan, party) |
| `GroupDetails` | Extended group record with members and roles |
| `GroupMembership` | Link between an entity and a group with role |
| `GroupRole` | Role definition within a group |

### Characters (3 types)
| Type | Description |
|------|-------------|
| `CharacterDetails` | Character record under a player account |
| `CharacterData` | Key-value data attached to a character |
| `CharacterStatistic` | Statistic value scoped to a character |

### Events & Telemetry (3 types)
| Type | Description |
|------|-------------|
| `Events` | Batch of events to write to PlayStream |
| `EventData` | Single telemetry / PlayStream event |
| `PlayerEvent` | Player-scoped PlayStream event record |

### Title & API Keys (3 types)
| Type | Description |
|------|-------------|
| `TitleData` | Title-level key-value data entry |
| `APIKey` | API key associated with a title |
| `SecretKey` | Developer secret key reference (never exposes raw secret) |

---

## Query Operations

The `Query` type covers read operations across all service areas:

- **Player** — `getPlayer`, `getPlayerDetails`, `getPlayerProfile`, `getPlayerData`, `getPlayerStatistics`
- **Auth** — `getEntityToken`, `getEntityDetails`
- **Catalog / Economy** — `getCatalogItems`, `getCatalogDetails`, `getStoreItems`, `getStoreDetails`, `getVirtualCurrencies`
- **Inventory** — `getUserInventory`, `getInventoryItem`
- **Characters** — `getCharacters`, `getCharacterData`, `getCharacterStatistics`
- **Leaderboards** — `getLeaderboard`, `getPlayerRank`, `getLeaderboardAroundPlayer`
- **Trades** — `getTrade`, `getPlayerTrades`
- **CloudScript** — `getCloudScriptRevision`
- **Groups** — `getGroup`, `listGroupMembers`
- **Segments** — `getSegments`, `getSegmentDetails`, `getPlayersInSegment`
- **Title Data** — `getTitleData`
- **Events** — `getPlayerEvents`

## Mutation Operations

The `Mutation` type covers write operations:

- **Authentication** — `loginWithCustomId`, `loginWithEmailAddress`, `loginWithFacebook`, `loginWithGoogle`, `loginWithApple`, `loginWithXbox`, `loginWithSteam`
- **Player Data** — `updatePlayerData`, `updatePlayerStatistics`
- **Virtual Currency** — `addVirtualCurrency`, `subtractVirtualCurrency`
- **Inventory** — `grantItemsToPlayer`, `redeemCoupon`, `consumeItem`, `revokeInventoryItem`
- **Characters** — `grantCharacter`, `updateCharacterData`, `updateCharacterStatistics`, `deleteCharacter`
- **Trades** — `openTrade`, `acceptTrade`, `cancelTrade`
- **CloudScript** — `executeCloudScript`, `executeFunction`
- **Groups** — `createGroup`, `deleteGroup`, `addGroupMembers`, `removeGroupMembers`, `updateGroupRole`
- **Events** — `writePlayerEvent`, `writeEvents`
- **Title Data** — `setTitleData`
- **Player Admin** — `banPlayer`, `unbanPlayer`, `resetPassword`, `deletePlayer`

---

## Notes

- PlayFab does not expose a native GraphQL endpoint. This schema is a conceptual model derived from the PlayFab REST API surface and is intended for developer tooling, API documentation, and schema-driven code generation.
- The `JSON` scalar covers the arbitrary key-value maps that PlayFab uses extensively for player data, title data, custom data, and event bodies.
- Entity tokens expire and must be refreshed; the schema models this via `EntityToken.tokenExpiration`.
- The `SecretKey` type deliberately omits the raw secret value to match PlayFab's security model where keys are only shown once at creation time.
- Economy v2 (Catalog v2) introduces inventory transactions and a different data model from the classic v1 catalog; both coexist in this schema via shared `ItemDetails`/`Catalog` types.
