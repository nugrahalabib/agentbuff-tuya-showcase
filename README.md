<!-- Showcase repository: the product is real and in use, its source code is private. -->

<a href="https://tuya.agentbuff.id"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg"><img src="assets/banner-light.svg" width="100%" alt="Smart Home for AgentBuff. Control Tuya and Smart Life devices by chatting with your AI agent."></picture></a>

<p align="center"><a href="https://tuya.agentbuff.id"><b>Open tuya.agentbuff.id</b></a> · <a href="https://github.com/nugrahalabib">More of my work</a> · <a href="https://nugrahalabib.com">nugrahalabib.com</a> · <a href="mailto:nugrahalabib@gmail.com">Email</a></p>

<p align="center"><a href="#the-business">The business</a> · <a href="#product-tour">Product tour</a> · <a href="#for-developers">For developers</a></p>

## Overview

Smart Home for AgentBuff links a user's Tuya and Smart Life devices to their AI agent over MCP. Lights, air conditioners, plugs and cameras already in the Smart Life app can be controlled from a chat.

Existing community servers for Tuya need a developer account or only run on the home network. This one is a multi-user web service with login, built on Tuya's end-user API with a single API key.

A web app in the style of Apple Home gives a visual view of the same home.

| | |
| --- | --- |
| **Status** | Live at [tuya.agentbuff.id](https://tuya.agentbuff.id) |
| **Role** | Designed and built by Nugraha Labib Mujaddid as a first-party app on the AgentBuff marketplace. |
| **Period** | Since Oct 2026 |
| **Source** | Private. This repository presents the product; the code is not published. |

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/features-dark.svg"><img src="assets/features-light.svg" width="100%" alt="What Smart Home for AgentBuff does: Device control, Confirmation for risky devices, Scenes, Schedules and timers, Event automations, Infrared AC pairing, Encrypted key storage, Sign in with AgentBuff."></picture>

## The business

Buff Tuya (Smart Home for AgentBuff) links the Smart Life and Tuya devices a household already owns to that household's AI agent on AgentBuff. The owner asks in chat to turn off the bedroom lights or set the AC to 24 degrees, and the agent does it through an MCP server with 31 tools. A web app in the style of Apple Home shows the same home by room, with scenes, schedules, automations and an activity log. Nugraha Labib Mujaddid designed and built it as CEO of AgentBuff, as an app sold on the AgentBuff marketplace.

### The problem

Many Indonesian homes already run lights, plugs, ACs and cameras through the Smart Life or Tuya Smart app. Controlling them still means opening the app and tapping through rooms. People who use an AI agent every day want to say "turn off all the bedroom lights" in chat instead.

The community MCP servers for Tuya were built for developers. They need a Tuya developer cloud project that must be renewed every six months, or they run on the home network next to the devices. None of them is a multi-user web service with a login that a non-technical owner can buy and connect in a few minutes.

Tuya's end-user API also leaves gaps that matter in a real home: it has no scenes, it answers success when the cloud accepts a command rather than when the device acts, and an AC that only has an infrared remote cannot be controlled by an outside app without its remote codes.

### Who uses it

| Role | What they do with it |
| --- | --- |
| **Home owner** | Buys the app in the AgentBuff marketplace, connects the home once with a key from tuya.ai, then controls devices by chat or in the web app. |
| **The owner's AI agent** | Calls the MCP tools to read the home, control devices, save scenes, set schedules and automations, and reports results honestly, including commands the device did not confirm. |
| **AgentBuff platform** | Signs the owner in, answers whether the owner still has access, and installs the connector on the agent automatically after purchase. |
| **Advanced user with another MCP client** | Creates a manual token on the Agent page and points any MCP client at the same server. |

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/before-after-dark.svg"><img src="assets/before-after-light.svg" width="100%" alt="Before and after: Open the Smart Life app and tap through rooms to switch things off. becomes Say &quot;turn off the bedroom lights&quot; in chat and the agent does it.; Community Tuya MCP servers need a developer cloud project or a computer on the home network. becomes One end-user key from tuya.ai, pasted once into a 3-step wizard. The service runs in the cloud behind a login.; An AC with only an infrared remote stays outside every routine. becomes Pick the AC brand, test a remote code once, and the AC works from the app and from chat like any other AC.; Tuya's end-user API has no scenes and no rules that react to sensors. becomes Scenes, schedules and if-this-then-that automations are stored and run by the service.; An agent says &quot;done&quot; when the cloud only accepted the command. becomes The server reads the device state back and tells the agent when a change is not confirmed yet.."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/journey-dark.svg"><img src="assets/journey-light.svg" width="100%" alt="How work flows: Buy the app, Connector installed, Sign in, Get the home key, Paste and discover, Ask in chat, Agent acts, Home runs itself."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/value-dark.svg"><img src="assets/value-light.svg" width="100%" alt="What it changes: 31 MCP tools for one home; 3 steps to connect a home, no developer account; 324 AC remote code sets in the library; 2 languages in the app, Indonesian and English."></picture>

### Model and status

Buff Tuya is a paid app on the AgentBuff marketplace. The public page at tuya.agentbuff.id shows the price as Rp49.000, paid once. It needs an AgentBuff account, and access follows the owner's AgentBuff entitlement.

After purchase, AgentBuff installs the connector and a companion skill on the owner's agent, so the agent already knows the tools. The agent cannot control anything until the owner connects a home on the web app.

What the agent cannot do is stated to it in the server instructions and sent back to the owner: Tuya's API does not allow unlocking door locks, live video, pairing new devices, firmware updates or editing homes and rooms, so those stay in the Smart Life app.

The product is live at tuya.agentbuff.id. The landing page states that it is not affiliated with Tuya Inc.

## Product tour

### 1. Getting started

The landing page explains the product to AgentBuff users and leads to Sign in with AgentBuff. A 3-step wizard then connects the home: get the app ready, create a key on tuya.ai, paste it. The key is checked with Tuya before it is saved.

- Step 2 walks through tuya.ai sign-in with the Smart Life QR scan and the Toolbox, API Key menu, with small pictures for each step.
- The region badge appears as soon as the key is pasted, read from the two letters after sk-.
- The key is stored encrypted and never shown again; the agent never receives it.
- After discovery the owner sees how many devices, homes and rooms were found.

<img src="assets/screens/01-landing.jpg" width="100%" alt="Landing page with Sign in with AgentBuff and the one-time price.">

<sub>Landing page with Sign in with AgentBuff and the one-time price.</sub>

<p><img src="assets/screens/02-wizard-get-key.jpg" width="49%" alt="Wizard step 2: how to create the home key on tuya.ai."> <img src="assets/screens/03-wizard-paste-key.jpg" width="49%" alt="Wizard step 3: a test key is pasted and the Singapore server is detected (key masked)."></p>

<sub>Left: Wizard step 2: how to create the home key on tuya.ai. · Right: Wizard step 3: a test key is pasted and the Singapore server is detected (key masked).</sub>

<p><img src="assets/screens/04-wizard-connected.jpg" width="100%" alt="Home connected: 22 devices in 2 homes and 6 rooms found on the fake Tuya cloud."></p>

<sub>Home connected: 22 devices in 2 homes and 6 rooms found on the fake Tuya cloud.</sub>

### 2. Home dashboard

The home screen groups devices by room in the order of the Smart Life app, with a short summary of what is still on and what is offline. Tapping a tile switches it; the dots open the device sheet. Light and dark themes are both designed, and on a phone the sidebar becomes a bottom tab bar.

- Summary line with one-tap actions to turn off everything that is on or refresh from Tuya.
- Tabs for each home, a scenes row, and a Turn all off action per room.
- Tiles show live values such as brightness, AC set point, watts and sensor readings.
- Changes from the agent, schedules or sensors reach the browser through server-sent events.

<img src="assets/screens/05-home-overview.jpg" width="100%" alt="Home overview by room on the invented Demo Home.">

<sub>Home overview by room on the invented Demo Home.</sub>

<p><img src="assets/screens/06-home-dark.jpg" width="49%" alt="The same home in the dark theme, with saved scenes."> <img src="assets/screens/07-phone-screens.jpg" width="49%" alt="Phone layout at 390 px: home, a light's control sheet and the scenes list."></p>

<sub>Left: The same home in the dark theme, with saved scenes. · Right: Phone layout at 390 px: home, a light's control sheet and the scenes list.</sub>

### 3. Device control

Each device opens a sheet built from the device's own model, so a light shows mode, brightness, colour and a timer, an AC shows temperature, mode and fan, and a plug shows power use. Readings and extra settings that Tuya exposes appear in plain language.

- Lights: on and off, white or colour mode, brightness, preset colours, warm and cool white, auto-off timer.
- ACs: set point with plus and minus, room temperature, mode, fan speed and swing.
- Plugs: watts now, energy today from Tuya's hourly statistics, voltage, and an hourly bar chart.
- Cameras: take a photo or a 10 second clip, pan and tilt, privacy, night vision and motion settings.

<img src="assets/screens/08-light-sheet.jpg" width="100%" alt="Light sheet with mode, brightness, colours and timer.">

<sub>Light sheet with mode, brightness, colours and timer.</sub>

<p><img src="assets/screens/09-ac-sheet.jpg" width="49%" alt="AC sheet with set point, room temperature, mode, fan and swing."> <img src="assets/screens/10-plug-energy.jpg" width="49%" alt="Plug sheet with current watts, energy today and the hourly chart."></p>

<sub>Left: AC sheet with set point, room temperature, mode, fan and swing. · Right: Plug sheet with current watts, energy today and the hourly chart.</sub>

<p><img src="assets/screens/12-camera-sheet.jpg" width="100%" alt="Camera sheet with photo and clip capture, pan controls and settings."></p>

<sub>Camera sheet with photo and clip capture, pan controls and settings.</sub>

### 4. Safety for risky devices

Heaters, kitchen appliances, garage doors, water valves and locks are marked as needing confirmation. The agent may always turn them off, but turning one on, directly or through an automation, needs the owner's yes in chat first. The owner can mark any other device the same way.

- Sensitive types are set in code, and a per-device switch overrides the default.
- A turn-on without confirm: true returns the error code needs_confirmation with a sentence the agent can relay.
- The same rule blocks an automation that would switch on a sensitive device unattended.
- Offline devices and ambiguous names return their own codes, so the agent asks or explains instead of guessing.

<img src="assets/screens/11-kettle-confirm.jpg" width="100%" alt="Kettle sheet with Agent must ask before turning on switched on by default.">

<sub>Kettle sheet with Agent must ask before turning on switched on by default.</sub>

<p><img src="assets/screens/25-mcp-confirm.png" width="100%" alt="Real MCP calls on the local run: refused without confirm, allowed with it, automation refused, offline device."></p>

<sub>Real MCP calls on the local run: refused without confirm, allowed with it, automation refused, offline device.</sub>

### 5. Infrared AC pairing

An AC that only has an infrared remote is controlled through a Tuya IR blaster. The owner picks the brand, optionally searches by model code, then tests codes one by one or lets auto search send them five seconds apart. Once the AC reacts, the code is saved and the AC works like any other.

- Brand list ordered by what is common in Indonesia, from a library built from SmartIR (MIT licence).
- Model code search with pictures showing where the sticker is on the unit and the remote.
- Each test turns the AC on at 27 degrees, high fan and swing, so the owner can see a full match.
- After pairing, the sheet explains that the AC's real state cannot be read back and offers Resend to the AC.

<img src="assets/screens/13-ir-pick-brand.jpg" width="100%" alt="Pick the AC brand or search by model code.">

<sub>Pick the AC brand or search by model code.</sub>

<p><img src="assets/screens/14-ir-code-test.jpg" width="49%" alt="Daikin, code 1 of 20, with auto search or one-by-one testing."> <img src="assets/screens/15-ir-paired.jpg" width="49%" alt="Paired: the AC is controlled through the remote blaster."></p>

<sub>Left: Daikin, code 1 of 20, with auto search or one-by-one testing. · Right: Paired: the AC is controlled through the remote blaster.</sub>

### 6. Scenes

A scene saves the current state of chosen devices under a name, icon and colour, and brings it back with one tap or one sentence to the agent. The agent can also build a scene from explicit settings without changing the devices now.

- Scenes are stored by Buff Tuya because Tuya's end-user API has none.
- Each scene card shows the sentence to tell the agent.
- Scenes can be run from the home screen, the scenes page, a schedule or an automation.

<img src="assets/screens/16-scene-editor.jpg" width="100%" alt="New scene: name, icon, colour and the devices whose current state is saved.">

<sub>New scene: name, icon, colour and the devices whose current state is saved.</sub>

### 7. Schedules and automations

Schedules run a device action or a scene at a time, on chosen weekdays, or as a one-off timer. Automations react to device changes: a door opening, motion, a temperature, CO2 or power reading crossing a value, a device going offline. Both can be made in chat; schedules also in the web app.

- Schedule editor with time, weekdays, timer mode, and a device or scene target.
- Automation actions: device commands, scenes, a notification to the Smart Life app, or a camera photo kept 7 days.
- Rules fire once when the condition becomes true, can be limited to a time window, and wait a cooldown before firing again.
- Items made by the agent are labelled, and each shows its last run and result.

<img src="assets/screens/17-schedule-editor.jpg" width="100%" alt="New schedule: every day at 18:30, turn on the ceiling light.">

<sub>New schedule: every day at 18:30, turn on the ceiling light.</sub>

<p><img src="assets/screens/18-schedules.jpg" width="49%" alt="Schedules list in the Indonesian interface, most made by the agent."> <img src="assets/screens/19-automations.jpg" width="49%" alt="Automations created through MCP; two have already run on simulated sensor events."></p>

<sub>Left: Schedules list in the Indonesian interface, most made by the agent. · Right: Automations created through MCP; two have already run on simulated sensor events.</sub>

### 8. Agent connection and activity

The Agent page shows example sentences, a recent activity log and, for advanced users, the MCP address and manual tokens. Every action records who asked for it: the owner on the web, the agent, a schedule, a scene, an automation or the system.

- Activity entries show the source with an icon and a relative time.
- Manual tokens are shown once, listed by prefix and expiry, and can be revoked.
- The server publishes its tools with read-only and destructive hints for MCP clients.

<img src="assets/screens/20-activity.jpg" width="100%" alt="Activity log in Indonesian: owner, agent, schedule and automation actions.">

<sub>Activity log in Indonesian: owner, agent, schedule and automation actions.</sub>

<p><img src="assets/screens/21-mcp-token.jpg" width="49%" alt="Manual MCP token panel; address, token and prefix masked."> <img src="assets/screens/24-mcp-tools.png" width="49%" alt="The 31 tools from tools/list, grouped by purpose, with their MCP hints."></p>

<sub>Left: Manual MCP token panel; address, token and prefix masked. · Right: The 31 tools from tools/list, grouped by purpose, with their MCP hints.</sub>

### 9. Access and settings

Settings show the connected key only in masked form, the Tuya server region, theme, language and time zone. When the owner's AgentBuff access ends, the web app shows a paused screen and the MCP server refuses tools with access_frozen, while homes, scenes and schedules are kept.

- Update key or disconnect the home from Settings.
- Indonesian and English interface, three Indonesian time zones.
- Access paused screen with Reactivate and Check again; data is never deleted because of access status.

<img src="assets/screens/22-frozen.jpg" width="100%" alt="Access paused after the fake entitlement service answered that access had ended.">

<sub>Access paused after the fake entitlement service answered that access had ended.</sub>

<p><img src="assets/screens/23-settings.jpg" width="100%" alt="Settings: masked key, region, theme, language and time zone."></p>

<sub>Settings: masked key, region, theme, language and time zone.</sub>

## For developers

### Architecture

Buff Tuya is a single Next.js 16 app with React 19, TypeScript and Tailwind 4, backed by PostgreSQL 16 through Drizzle ORM. A separate Node worker built from the same code runs schedules, holds one Tuya WebSocket per connected home, refreshes device lists and cleans old data. The browser receives changes through server-sent events.

The MCP server lives at /mcp on the same app. It uses the official MCP TypeScript server SDK in stateless Streamable HTTP mode, with bearer tokens per owner. Tool names and descriptions are in English, while result text is in Indonesian so the agent can pass it to the user as is. Each tool is classed as read or write, and destructive tools carry the MCP destructive hint.

Every Tuya call uses the owner's end-user key. The region is taken from the two letters after sk-, so the owner never picks a data center. Devices are mirrored in a table with their model, so the app and the agent can describe capabilities in plain language and translate friendly commands such as brightness 20, warm into the exact Tuya properties of that device.

Sign in with AgentBuff is OpenID Connect with the authorization code flow, PKCE S256 and ES256 ID tokens with a pairwise subject. Access is checked against AgentBuff on every entry point with a 10 minute cache. AgentBuff can also connect the agent automatically by sending a signed assertion, for which the service issues a normal MCP token.

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/architecture-dark.svg"><img src="assets/architecture-light.svg" width="100%" alt="How Smart Home for AgentBuff is built."></picture>

### Data model

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/data-model-dark.svg"><img src="assets/data-model-light.svg" width="100%" alt="Data model: pengguna (owner), sesi (session), status_hak (entitlement), token_mcp (MCP token), jti_terpakai (used assertion), sambungan_tuya (Tuya connection), perangkat (device), suasana (scene), jadwal (schedule), otomasi (automation), foto_kamera (camera photo), aktivitas (activity)."></picture>

### Key flows

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-1-dark.svg"><img src="assets/flow-1-light.svg" width="100%" alt="Connecting a home: The owner pastes the key; the shape sk- plus two letters is checked and the region is resolved. Then The server calls Tuya for homes, rooms and devices to prove the key works. Then The key is sealed with envelope AES-256-GCM: a fresh data key per secret, wrapped by a master key from the environment, with the owner's id as additional data. Then Devices and models are mirrored, the masked key is stored for display, and the activity log records the connection."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-2-dark.svg"><img src="assets/flow-2-light.svg" width="100%" alt="Agent turns on a device: The agent sends tools/call with its bearer token; the server hashes it and finds the token under a token-hash database context. Then Per-token limits apply (120 calls and 40 writes a minute), then the owner's access is checked. Then The device name is resolved fuzzily; several matches return ambiguous with the candidates. Then A sensitive device being turned on without confirm: true returns needs_confirmation. Then The friendly command is translated with the device model and sent to Tuya. Then The server reads the device state back and answers confirmed or not confirmed, then logs the action as from the agent."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-3-dark.svg"><img src="assets/flow-3-light.svg" width="100%" alt="Automatic connection from AgentBuff: AgentBuff signs an ES256 assertion for the owner and posts it to the service. Then The service verifies it against AgentBuff's published keys, checks its age and stores its jti so it works once. Then Access is checked without cache; an owner who never opened the web app gets an account created. Then A 90 day MCP token is issued; only its hash is stored and the raw token goes back to AgentBuff once."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-4-dark.svg"><img src="assets/flow-4-light.svg" width="100%" alt="A sensor event fires an automation: The worker keeps one WebSocket to Tuya per active home and receives a device property change. Then Messages for the same device are processed in order and merged into the mirror with a jsonb merge. Then Rules are checked on the edge from false to true, inside their time window and after their cooldown. Then Actions run (device command, scene, notification or camera photo) and each is logged with the source automation."></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/flow-5-dark.svg"><img src="assets/flow-5-light.svg" width="100%" alt="Schedules run on time: Every 20 seconds the worker claims due schedules with FOR UPDATE SKIP LOCKED. Then The stored friendly command is translated at run time, so a model update from Tuya does not break it. Then The result is stored, the next run is computed, and a one-time schedule switches itself off."></picture>

### Security

- The Tuya key is encrypted with AES-256-GCM in an envelope bound to its owner, opened only on the server right before a Tuya call, never sent to the browser and never written to logs.
- Session cookies use the __Host- prefix, httpOnly, Secure and SameSite=Lax, and the database stores only a hash of the session id, so a leaked backup cannot be used to sign in.
- MCP tokens are 256-bit random values shown once and stored as sha256 hashes; a missing or revoked token gets HTTP 401 with WWW-Authenticate before any JSON-RPC is parsed.
- Row level security is enabled and forced on every owner table, application roles have no BYPASSRLS, and the owner context is set per transaction; the worker has its own policies.
- Turning on heaters, kitchen appliances, garage doors, valves, locks or any device the owner marks needs an explicit confirm from the agent, while turning off is always allowed.
- Camera files are fetched only from public https links to block server-side request forgery, and are kept 7 days behind random links.
- Pages carry a Content Security Policy with a per-request nonce plus standard security headers.
- A frozen account keeps all data; when AgentBuff cannot be reached, the last good answer is used for up to 72 hours so an outage does not switch off someone's home.

### Quality

- 138 tests in 12 files passed in a local run on 26 Nov 2026 (Vitest with PGlite), with the per-test timeout raised to 60 seconds because the machine was under heavy load.
- Integration tests run the real services against a fake Tuya cloud server that records every command and can simulate offline devices, rejected keys and slow camera uploads.
- The deploy RLS test script is also run in the test suite against the real migrations, so a broken policy fails before deploy.
- A guard script runs before every build with 10 guards, each self-tested on a bad sample so a guard that cannot fail is caught: no hard-coded screen text, proxy file placement, no server-only import in shared modules, RLS on every owner table, qualified columns inside SQL subqueries, no plain values imported across the client boundary, one language dictionary per visitor, no control characters, LF line endings in deploy files, no long dashes in product text. All 10 passed locally.
- Unit tests cover device capability parsing, the IR protocol conversion, the AC code library, automation triggers, schedule time math, the reported-state check, property labels, camera file checks, region parsing and key encryption.

### Deployment and operations

Docker Compose with three containers: PostgreSQL 16, the Next.js standalone web app and the worker from the same image. They share an internal network; only the web container joins the reverse proxy network, and no ports are published.

The deploy script backs up the database first and stops if that fails, counts rows in every table, builds the image with the guards, runs additive migrations with a separate migration role, runs the RLS test, starts web and worker, waits for health, then recounts and fails if any table shrank.

A backup script dumps the database every 6 hours, keeps 14 days, and verifies each dump three ways: gzip intact, size above zero and the closing line present. The health endpoint reads the worker's heartbeat rows.

After a release the script asks AgentBuff to refresh the product so owners' agents reload the tool list.

### Decisions

| Decision | Why |
| --- | --- |
| Build on Tuya's end-user API key | One sk- key from tuya.ai covers all homes and devices of an app account, needs no developer project or renewals, and lets one cloud service serve many owners. |
| Never take the key through chat | A key pasted to the agent would sit in chat transcripts and model logs, and it can turn on a heater; the agent always sends the owner to the connect page. |
| Keep scenes, schedules and automations on our side | Tuya's end-user API has no scenes, so the service stores them and runs them in its own worker. |
| Store friendly commands, translate at run time | Schedules and scenes keep working when Tuya updates a device model. |
| Check the reported state after each command | Tuya answers success when the cloud accepts a command, so without a read-back the agent would claim changes that did not happen. |
| Ship an IR code library for ACs | Tuya does not send remote signals for outside apps, so the service builds them from SmartIR codes (MIT) and beams them through the owner's IR blaster. |
| Freeze access, never delete data | Only a clear answer from AgentBuff freezes an owner, outages are tolerated, and homes, scenes and schedules survive a lapse in access. |
| Read the region from the key | The two letters after sk- name the data center, so owners never have to know which Tuya server they use. |

### Built with

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/stack-dark.svg"><img src="assets/stack-light.svg" width="100%" alt="Smart Home for AgentBuff stack."></picture>

### Engineering highlights

- Requests to Tuya go through a per-user queue with exponential backoff when the API rate limits.
- Integration tests run against a fake Tuya server, so device flows are tested without real hardware.
- The Tuya region is chosen from the key itself, so users never pick a data center.
- A frozen account becomes read-only in the web app and the MCP server refuses it.

---

<sub>Built by [Nugraha Labib Mujaddid](https://github.com/nugrahalabib). This page describes a private codebase; questions about the product or a demo are welcome at [nugrahalabib@gmail.com](mailto:nugrahalabib@gmail.com).</sub>
