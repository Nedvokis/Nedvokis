# Denis Khilkov

**Fullstack Developer**

## Contact

- **Email:** d.khilkov@gmail.com
- **Telegram:** @Nedvokis
- **GitHub:** github.com/Nedvokis

## Professional Summary

Pragmatic Fullstack Developer with 5+ years of hands-on experience building business-critical software — web services in Go and Node.js and cross-platform desktop applications on Electron — with a strong backend focus and production frontend work in React and Vue. Deep experience designing and shipping REST APIs on Fiber and Echo with GORM and PostgreSQL, JWT authentication and refresh-token rotation, and OpenAPI documentation generated from code via Swaggo. Proven track record integrating customer-facing portals with payment and fiscalization providers, banking APIs covering multiple lenders for online mortgage origination, and with the company's internal CRM and ERP systems for deals and electronic document workflow. Most recently focused on Electron desktop development and test automation — building a custom scenario-driven E2E framework on Playwright, plus soak/stress and memory-leak testing to keep unattended, always-on software reliable over multi-day runs. Comfortable evolving monolithic services into focused Go microservices on gRPC, hardening reliability with RabbitMQ, and containerizing the full stack with Docker behind Nginx. Remote-first, immediately available, ready to own product features end-to-end from API design and data modeling through deployment.

## Core Competencies

- **Backend:** Go (Fiber, Echo, GORM), Node.js, Express, JWT (auth-token + refresh-token), OpenAPI/Swagger via Swaggo, Gothenberg (PDF generation), gRPC
- **Frontend & Desktop:** React, Vue, HTML, CSS, SPA → SSR migration, Electron (electron-vite, electron-builder), Vite
- **Testing & QA:** Playwright (E2E automation for Electron), custom scenario-driven test frameworks, soak / stress testing, memory-leak diagnosis, manual test planning
- **Databases & Caching:** PostgreSQL, MySQL, MongoDB, Redis
- **Messaging & RPC:** RabbitMQ, gRPC, REST API
- **Integrations:** internal CRM, internal ERP (accreditation, document workflow), banking APIs, online cash register / fiscal-data providers, SMS gateways, generic third-party REST APIs
- **Quality & Tooling:** Git, Docker, Nginx, Linux
- **Practices:** REST API design, microservices decomposition, schema migrations, asynchronous integration with unreliable upstreams, test automation for always-on software

## Selected Achievements

- **TBFF:** Designed a custom scenario-driven E2E testing framework for Electron desktop apps (Playwright + TypeScript) — declarative scenario configs, a runner driving a real app across soak/stress cycles, per-step attribution of console errors, exceptions and crashes, and reproducible video reports with a virtual-cursor overlay.
- **TBFF:** Diagnosed and fixed renderer memory growth over 18+ hour unattended kiosk sessions and audited components for leaking event listeners/timers — hardening the desktop apps for continuous multi-day operation.
- **DOGMA:** Built the customer account portal in Go from scratch — JWT authentication, SMS-code registration via a third-party SMS gateway, favorites, live deal status from the upstream CRM — and grew it into the company's main customer-facing product.
- **DOGMA:** Delivered paid online apartment reservations integrated with an online cash register API and a fiscal-data provider for receipt generation.
- **DOGMA:** Implemented online mortgage origination inside the customer portal, integrated with multiple banking APIs covering different lenders.
- **DOGMA:** Refactored the customer portal monolith into focused Go microservices (deals service, upstream-CRM mirror service) communicating over gRPC.
- **DOGMA:** Introduced RabbitMQ as the backbone for talking to the internal CRM, internal ERP, and third-party APIs — eliminating data-loss scenarios on outages and decoupling external integrations from request paths.
- **DOGMA:** Designed and ran the automated migration of the apartment catalog from a legacy CRM into PostgreSQL, unblocking filtered search and modern UX features.

## Professional Experience

### **TBFF (Talking Birds & Flying Fish)** — Fullstack Developer — _Dec 2025 — May 2026_

Experiential studio building interactive touchscreen kiosk installations for large-scale industry events. Contributed to three cross-platform desktop applications (Electron, React, TypeScript, Vite) that run unattended in kiosk mode on multi-display hardware, with a primary focus on test automation and reliability.

**Desktop application development**

- Built dual-display touchscreen kiosk apps: multi-screen narrative flows, timed interactive mini-games, multilingual content (EN and additional locales), synchronized voice-over/audio, inactivity/idle handling, and self-updating via auto-update.
- Worked across the full Electron surface — main process, IPC channels, renderer (React), configuration/settings, kiosk-mode window management and multi-monitor selection.

**Test automation (primary focus)**

- Designed a custom scenario-driven E2E testing framework on Playwright + Electron + TypeScript: declarative scenario configs describe user flows; a runner launches a real Electron instance (temp userData, config overrides) and executes steps across configurable cycles for soak and stress testing.
- Built an error-collection layer that captures console errors, uncaught exceptions and renderer crashes and attributes each to the exact failing step, turning flaky end-to-end runs into actionable reports.
- Added reproducible visual reporting: in-app video capture (desktopCapturer + MediaRecorder) with a smooth virtual-cursor overlay, converted WebM → MP4 via ffmpeg and attached as test artifacts.
- Centralized `data-testid` selectors and a locator-resolution layer (testid / role / text / css) so specs stayed stable against UI change; spec files stayed one to two lines by delegating to the scenario runner.
- Built a second Playwright E2E suite for another kiosk app, covering app startup, slide transitions, inactivity/idle screens, survey flows and token collection.

**Reliability & memory-leak testing**

- Diagnosed renderer memory growth over 18+ hour unattended kiosk sessions caused by soft in-app navigation keeping the renderer alive; moved reset paths to a full application reload behind a seamless CSS blackout transition, eliminating the leak while preserving a polished visual experience.
- Audited components for leaking event listeners and timers and fixed a critical video event-listener leak (listener re-added without removal on ref change).

**Manual QA**

- Authored and executed manual test plans covering dual-display behavior, full multi-screen sequences, the interactive mini-games, audio, and the password-protected settings / kiosk configuration — complementing the automated suites where end-to-end coverage was not yet in place.

### **DOGMA** — Backend Developer — _Sep 2019 — Jan 2024_

Real-estate developer with an in-house portfolio of customer, agency and counterparty portals integrated with the company's internal CRM and ERP systems.

#### 2019 — 2020

Joined as a full-stack engineer (Node.js / Express on the backend; React and Vue on the frontend).

- Redesigned company landing pages and the main corporate site.
- Optimized customer-facing sites by migrating from a SPA to SSR — better first paint, better SEO, fewer regressions on shaky mobile networks.
- Moved hosting from a static web-hosting server to Dockerized services behind Nginx.

#### 2020 — 2021

Transitioned fully to Go backend.

- Onboarded the new frontend engineer responsible for the company sites.
- Launched the company's first Go service in production: an apartment catalog with filtered search.
- Designed and ran an automated migration of the apartment data from a legacy CRM into PostgreSQL.
- In the second half of the year, shipped the customer account portal: JWT authentication, SMS-code registration via a third-party SMS gateway, favorites for shortlisted apartments, and live status of the customer's deals at DOGMA.
- Onboarded the new backend engineer at the end of the year.

#### 2021 — 2022

Expanded the customer portal and started the counterparty portal.

- Added paid online apartment reservations (4-day hold) integrated with an online cash register API; receipts generated through a fiscal-data provider.
- Implemented online mortgage origination inside the customer portal, integrated with multiple banking APIs covering different lenders.
- Designed and shipped the counterparty portal: deal status, and electronic document workflow with the company's internal ERP system for counterparty accreditation.

#### 2022 — 2024

Stood up the agency portal, hardened cross-system integrations, and decomposed the monolith.

- Started development of the realtor-agency portal. Built the REST API initially on the Echo framework, then migrated to Fiber for higher throughput; documented the API with Swagger via Swaggo; introduced auth-token + refresh-token JWT middleware for Fiber; used GORM for PostgreSQL access; used Gothenberg for PDF document generation.
- Released a translation service used by the company's mobile and frontend projects.
- Adopted RabbitMQ across projects to improve fault tolerance when talking to the internal CRM and ERP APIs as well as third-party APIs.
- Refactored the customer portal monolith into focused Go microservices: a deals service, an upstream-CRM mirror service. Microservices communicate over gRPC.

### **ShtrafovNet.ru** — Backend Developer — _Feb 2024 — Apr 2024_

Service for tracking and resolving traffic fines.

- Built and refactored the REST API that powers the public website and the web application.
- Streamlined endpoint contracts and internal data flows for faster, more predictable response times.

## Education

**KAIT 20 — College of Automation and Information Technologies** — _2015_
Specialization: Industrial Automation Systems.

## Languages

- Russian — Native
- English — B1 (Intermediate)

## Availability & Preferences

- Remote-first; full-time employment.
- Immediately available.
- Not available for business trips.
- Open to product companies in fintech, real-estate, B2B SaaS, and developer-tooling.
