# Garmin

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

Garmin is the global leader in GPS-enabled wearables, cycling computers, outdoor handhelds, marine electronics, aviation avionics, and automotive navigation. Garmin's developer surface spans the Connect IQ wearable app platform (Monkey C, watch faces, data fields, widgets, device apps), the Garmin Connect Developer Program cloud APIs (Health, Activity, Women's Health, Training, Courses), the Health SDK for direct BLE streaming from wearables, the FIT SDK that defines the industry's de-facto endurance data interchange format, Navionics marine cartography, inReach satellite messaging, the ANT/ANT+ wireless protocol, and specialized APIs for golf, aviation flight data, fleet telematics, and custom outdoor maps.

**Areas:** GPS · Fitness · Wearables · Outdoor · Connect IQ · Health · Cycling · Marine · Aviation · Automotive · FIT · ANT

## Garmin on APIs.io

Everything profiled for Garmin is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/garmin/](https://apis.io/providers/garmin/)** — or go straight to one of the APIs or properties below.

### APIs (17)

- [Garmin Connect IQ Platform](https://apis.io/apis/garmin/garmin-connect-iq/) — Connect IQ is Garmin's open platform for building wearable apps that run on Garmin watches and cycling computers. Developers write apps in Monkey C —…
- [Garmin Connect Health API](https://apis.io/apis/garmin/garmin-connect-health-api/) — Inbound cloud API for receiving all-day health summary metrics from Garmin wearables — daily summaries, epoch summaries, sleep data, heart rate, steps,…
- [Garmin Connect Activity API](https://apis.io/apis/garmin/garmin-connect-activity-api/) — Inbound cloud API providing comprehensive workout and activity data across 30+ activity categories — GPS tracks, FIT file fetch, manually entered…
- [Garmin Connect Women's Health API](https://apis.io/apis/garmin/garmin-connect-womens-health-api/) — Inbound cloud API exposing menstrual cycle tracking and pregnancy data captured in the Garmin Connect mobile app. Partner-only access requiring approval;…
- [Garmin Connect Training API](https://apis.io/apis/garmin/garmin-connect-training-api/) — Outbound cloud API for pushing structured workouts and training plans from partner platforms to a user's Garmin device. Supports the full Garmin workout…
- [Garmin Connect Courses API](https://apis.io/apis/garmin/garmin-connect-courses-api/) — Outbound cloud API for pushing GPS courses and routes from partner platforms (Komoot, Strava, Ride with GPS, etc. pattern) to a user's Garmin wearable or…
- [Garmin Health SDK](https://apis.io/apis/garmin/garmin-health-sdk/) — Mobile SDKs for iOS and Android that pair directly with Garmin wearables over BLE and stream raw real-time sensor data — accelerometer, heart rate, pulse…
- [Garmin FIT SDK](https://apis.io/apis/garmin/garmin-fit-sdk/) — The Flexible and Interoperable Data Transfer (FIT) protocol is Garmin's compact binary file format for sport, fitness, and health data — activities,…
- [Garmin Golf API](https://apis.io/apis/garmin/garmin-golf-api/) — Premium partner API exposing data from the Garmin Golf app — scorecard data (par, strokes per hole, fairway hits, putts), Garmin launch monitor metrics…
- [Garmin Navionics Marine Charts and Maps](https://apis.io/apis/garmin/garmin-navionics-marine-api/) — Web API and iOS/Android mobile SDK for embedding Navionics marine cartography — HD contour depth data, spot soundings, detailed shorelines, navigational…
- [Garmin inReach Portal Connect](https://apis.io/apis/garmin/garmin-inreach-portal-connect/) — Enterprise API for organizations to integrate inReach satellite communicator data — two-way messaging, location tracking, MapShare, SOS events — into their…
- [Garmin ANT Wireless Network](https://apis.io/apis/garmin/garmin-ant-wireless/) — Garmin (via dynastream) operates the ANT and ANT+ ultra-low-power 2.4GHz wireless protocol used across cycling, running, fitness, and health sensors…
- [Garmin Tacx Trainer Communication](https://apis.io/apis/garmin/garmin-tacx-trainer-api/) — Communication protocol documentation for controlling Tacx smart trainers (NEO, Flux, Boost line) over ANT+ FE-C and Bluetooth FTMS for indoor cycling and…
- [Garmin Radar Data BLE Program](https://apis.io/apis/garmin/garmin-radar-data-ble/) — BLE GATT service that allows third-party head units, smartphones, and cycling-safety apps to receive vehicle-approach data from Garmin Varia rearview radars…
- [Garmin Aviation Flight Data Log API](https://apis.io/apis/garmin/garmin-flight-data-log-api/) — Aviation API for accessing flight data logs (FDL/FDM) generated by Garmin avionics — G1000/G3000/G5000 integrated flight decks and G500/G600 TXi displays —…
- [Garmin Fleet Management Platform](https://apis.io/apis/garmin/garmin-fleet-management/) — Developer integration for Garmin Fleet purpose-built truck and commercial vehicle navigators, enabling dispatch, route, message, and stop integration…
- [Garmin Custom Maps API](https://apis.io/apis/garmin/garmin-custom-maps/) — Specification for creating KMZ-based custom maps that load on Garmin outdoor handhelds and fitness watches — used by parks, search-and-rescue teams, race…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/garmin/](https://apis.io/graphqls/garmin/garmin-graphql/)

#### Security (1)

Authentication, trust centre, and vulnerability disclosure.

- [Garmin Domain Security](https://apis.io/security/garmin/garmin-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.garmin.com/)
- [Documentation](https://developer.garmin.com/connect-iq/overview/)
- [Blog](https://www.garmin.com/en-US/blog/)
- [Terms of service](https://www.garmin.com/en-US/legal/connect-terms-of-use/)
- [Privacy policy](https://www.garmin.com/en-US/privacy/connect/)
- [GitHub](https://github.com/garmin)
- [Status](https://connect.garmin.com/status/)

## API Evangelist rating

**Kin Score 21.4** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 63.4 |
| Contract quality | 0.0 |
| Contract governance | 0.0 |
| Operational transparency | 18.4 |
| Developer ergonomics | 42.9 |
| Access clarity | 23.7 |

**Agent readiness 0.0** — human-only

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | — |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
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

**Regulatory alignment 7.8** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/garmin/](https://apis.io/providers/garmin/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Garmin: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/garmin/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
