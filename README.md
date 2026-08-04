# Garmin (garmin)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Garmin is the global leader in GPS-enabled wearables, cycling computers, outdoor handhelds, marine electronics, aviation avionics, and automotive navigation. Garmin's developer surface spans the Connect IQ wearable app platform (Monkey C, watch faces, data fields, widgets, device apps), the Garmin Connect Developer Program cloud APIs (Health, Activity, Women's Health, Training, Courses), the Health SDK for direct BLE streaming from wearables, the FIT SDK that defines the industry's de-facto endurance data interchange format, Navionics marine cartography, inReach satellite messaging, the ANT/ANT+ wireless protocol, and specialized APIs for golf, aviation flight data, fleet telematics, and custom outdoor maps.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/garmin/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - GPS, Fitness, Wearables, Outdoor, Connect IQ, Health, Cycling, Marine, Aviation, Automotive, FIT, ANT

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Garmin Connect IQ Platform
Open wearable app platform — five app categories (watch faces, data fields, widgets, device apps, audio content providers), Monkey C language, VS Code extension, device simulators, and companion Android/iOS SDKs. Apps ship through the Connect IQ Store. Current SDK 9.1.0 (May 2026).

**Human URL:** [https://developer.garmin.com/connect-iq/](https://developer.garmin.com/connect-iq/)

- [Documentation](https://developer.garmin.com/connect-iq/overview/)
- [SDK — Connect IQ SDK](https://developer.garmin.com/connect-iq/sdk/)
- [Documentation — Monkey C](https://developer.garmin.com/connect-iq/monkey-c/)
- [App Marketplace — Connect IQ Store](https://apps.garmin.com/)
- [SDK — Android](https://github.com/garmin/connectiq-android-sdk)
- [SDK — iOS Companion](https://github.com/garmin/connectiq-companion-app-sdk-ios)

### Garmin Connect Health API
Inbound cloud API for receiving all-day health summary metrics — daily summaries, sleep, heart rate, steps, stress, Body Battery, pulse ox, respiration, and user-logged metrics. Partner approval and OAuth required.

**Human URL:** [https://developer.garmin.com/gc-developer-program/health-api/](https://developer.garmin.com/gc-developer-program/health-api/)

### Garmin Connect Activity API
Inbound cloud API for complete workout/activity data across 30+ categories with GPS tracks, FIT file fetch, lap details, and per-activity metrics.

**Human URL:** [https://developer.garmin.com/gc-developer-program/activity-api/](https://developer.garmin.com/gc-developer-program/activity-api/)

### Garmin Connect Women's Health API
Inbound cloud API exposing menstrual cycle tracking and pregnancy data captured in Garmin Connect.

**Human URL:** [https://developer.garmin.com/gc-developer-program/womens-health-api/](https://developer.garmin.com/gc-developer-program/womens-health-api/)

### Garmin Connect Training API
Outbound cloud API for pushing structured workouts and training plans (warmup, intervals, repeats, cool down) from partner platforms onto a user's Garmin device.

**Human URL:** [https://developer.garmin.com/gc-developer-program/training-api/](https://developer.garmin.com/gc-developer-program/training-api/)

### Garmin Connect Courses API
Outbound cloud API for pushing GPS courses and routes from partner platforms (Komoot, Strava, Ride with GPS pattern) onto Garmin wearables and Edge cycling computers.

**Human URL:** [https://developer.garmin.com/gc-developer-program/courses-api/](https://developer.garmin.com/gc-developer-program/courses-api/)

### Garmin Health SDK
iOS and Android SDKs that pair directly with Garmin wearables over BLE and stream raw real-time sensor data — accelerometer, HR, pulse ox, respiration, stress, calories, steps, Body Battery, plus advanced streams (gyroscope, actigraphy, beat-to-beat). Standard variant is HIPAA-compliant; Companion variant combines streaming with the cloud Health API.

**Human URL:** [https://developer.garmin.com/health-sdk/overview/](https://developer.garmin.com/health-sdk/overview/)

### Garmin FIT SDK
The Flexible and Interoperable Data Transfer (FIT) protocol — Garmin's compact binary format for sport, fitness, and health data. SDKs in eight languages (C, C++, C#, Java, JavaScript, Objective-C, Python, Swift), the FitCSVTool for binary-to-text inspection, FitGen for profile customization, and the canonical Profile.xlsx. FIT is the de-facto interchange format across Strava, TrainingPeaks, Komoot, Wahoo, Polar, Suunto, Apple Health, and Google Fit.

**Human URL:** [https://developer.garmin.com/fit/overview/](https://developer.garmin.com/fit/overview/)

- [SDK — Python](https://github.com/garmin/fit-python-sdk)
- [SDK — JavaScript](https://github.com/garmin/fit-javascript-sdk)
- [SDK — Java](https://github.com/garmin/fit-java-sdk)
- [SDK — Swift](https://github.com/garmin/fit-swift-sdk)
- [SDK — C](https://github.com/garmin/fit-c-sdk)
- [SDK — C++](https://github.com/garmin/fit-cpp-sdk)
- [SDK — C#](https://github.com/garmin/fit-csharp-sdk)
- [SDK — Objective-C](https://github.com/garmin/fit-objective-c-sdk)
- [Tools — FIT SDK Tools](https://github.com/garmin/fit-sdk-tools)

### Garmin Golf API
Premium partner API providing scorecard data (par, strokes/hole, fairway hits, putts), Garmin launch monitor metrics (Approach R10/R50), and per-shot GPS data.

**Human URL:** [https://developer.garmin.com/golf-api/overview/](https://developer.garmin.com/golf-api/overview/)

### Garmin Navionics Marine Charts and Maps
Navionics marine cartography Web API and iOS/Android mobile SDK — HD contour depth data, spot soundings, detailed shorelines, navigational objects, and daily updates.

**Human URL:** [https://developer.garmin.com/marine-charts/overview/](https://developer.garmin.com/marine-charts/overview/)

### Garmin inReach Portal Connect
Enterprise integration for inReach satellite communicators — two-way messaging, location tracking, MapShare, and SOS events over the Iridium satellite network.

**Human URL:** [https://developer.garmin.com/inreach-portal/](https://developer.garmin.com/inreach-portal/)

### Garmin ANT Wireless Network
ANT and ANT+ ultra-low-power 2.4GHz wireless protocol with standardized device profiles (heart rate, power, speed/cadence, stride, FE-C trainer, blood pressure, weight scale) implemented across the fitness sensor industry.

**Human URL:** [https://www.thisisant.com/](https://www.thisisant.com/)

### Garmin Tacx Trainer Communication
ANT+ FE-C and Bluetooth FTMS protocol documentation for controlling Tacx smart trainers (NEO, Flux, Boost) from third-party indoor cycling apps.

**Human URL:** [https://developer.garmin.com/tacx-trainer/](https://developer.garmin.com/tacx-trainer/)

### Garmin Radar Data BLE Program
BLE GATT service letting third-party head units, phones, and cycling-safety apps receive vehicle-approach data (count, distance, speed) from Garmin Varia rearview radars (RTL515, RCT715).

**Human URL:** [https://developer.garmin.com/radar-data-ble/](https://developer.garmin.com/radar-data-ble/)

### Garmin Aviation Flight Data Log API
Access flight data logs (FDL/FDM) generated by Garmin avionics — G1000/G3000/G5000 integrated flight decks and G500/G600 TXi displays — for fleet operators, training organizations, and safety management programs.

**Human URL:** [https://developer.garmin.com/flight-data-log/](https://developer.garmin.com/flight-data-log/)

### Garmin Fleet Management Platform
Developer integration for Garmin Fleet purpose-built commercial vehicle navigators — dispatch, routing, messaging, and stop integration with third-party fleet software.

**Human URL:** [https://developer.garmin.com/fleet-management/](https://developer.garmin.com/fleet-management/)

### Garmin Custom Maps API
KMZ-based custom maps for Garmin outdoor handhelds and fitness watches — used by parks, search-and-rescue teams, race organizers, and event operators.

**Human URL:** [https://developer.garmin.com/custom-maps/](https://developer.garmin.com/custom-maps/)

## Common Properties

- [Portal — garmin.com](https://www.garmin.com)
- [Portal — Garmin Developer](https://developer.garmin.com/)
- [Documentation — Connect IQ](https://developer.garmin.com/connect-iq/overview/)
- [GitHubOrganization](https://github.com/garmin)
- [Forum — Garmin Developer Forums](https://forums.garmin.com/developer/)
- [SignUp — Garmin Connect Developer Program](https://developer.garmin.com/gc-developer-program/overview/)
- [AppMarketplace — Connect IQ Store](https://apps.garmin.com/)
- [StatusPage — Garmin Connect](https://connect.garmin.com/status/)
- [SDK — Connect IQ Apps](https://github.com/garmin/connectiq-apps)
- [SDK — Connect IQ Android](https://github.com/garmin/connectiq-android-sdk)
- [SDK — Connect IQ iOS Companion](https://github.com/garmin/connectiq-companion-app-sdk-ios)
- [SDK — FIT Python](https://github.com/garmin/fit-python-sdk)
- [SDK — FIT JavaScript](https://github.com/garmin/fit-javascript-sdk)
- [SDK — FIT Java](https://github.com/garmin/fit-java-sdk)
- [SDK — FIT Swift](https://github.com/garmin/fit-swift-sdk)
- [SDK — FIT C](https://github.com/garmin/fit-c-sdk)
- [SDK — FIT C++](https://github.com/garmin/fit-cpp-sdk)
- [SDK — FIT C#](https://github.com/garmin/fit-csharp-sdk)
- [SDK — FIT Objective-C](https://github.com/garmin/fit-objective-c-sdk)
- [Tools — FIT SDK Tools](https://github.com/garmin/fit-sdk-tools)
- [Tools — LIDAR-Lite Arduino Library](https://github.com/garmin/LIDARLite_Arduino_Library)
- [Blog — Garmin Blog](https://www.garmin.com/en-US/blog/)
- [Press — Garmin Newsroom](https://www.garmin.com/en-US/newsroom/)
- [LinkedIn](https://www.linkedin.com/company/garmin-international)
- [Twitter](https://twitter.com/Garmin)
- [YouTube](https://www.youtube.com/user/garmin)
- [PrivacyPolicy](https://www.garmin.com/en-US/privacy/connect/)
- [TermsOfService](https://www.garmin.com/en-US/legal/connect-terms-of-use/)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
