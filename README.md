# Denis Khilkov

**Fullstack Developer**

## Contact Information

[Email](mailto:d.khilkov@gmail.com) • [Telegram](https://t.me/Nedvokis) • [GitHub](https://github.com/Nedvokis) • [CV.pdf](https://github.com/Nedvokis/Nedvokis/raw/main/CV.pdf)

## Professional Summary

Pragmatic Fullstack Developer with 5+ years building business-critical software — from web services in Go and Node.js to cross-platform desktop apps on Electron — with a strong backend focus and hands-on frontend experience in React and Vue. Proven track record delivering customer-facing portals and B2B integrations end-to-end: REST APIs on Fiber/Echo with GORM and PostgreSQL, JWT authentication, payment and mortgage integrations, internal CRM/ERP document workflows, and SPA-to-SSR migrations. Most recently focused on desktop application development and test automation — building a custom E2E testing framework on Playwright, plus soak/stress and memory-leak testing for unattended, always-on software. Experienced in evolving monolithic services into microservices on gRPC, hardening reliability with RabbitMQ-backed queues, and containerizing the full stack with Docker and Nginx. Remote-first, available for full-time roles, ready to own product features from API design to production delivery.

## Key Achievements

- **E2E Test Automation Framework**: At TBFF, designed a custom scenario-driven end-to-end testing framework for Electron desktop apps (Playwright + TypeScript) — declarative scenario configs, a runner driving a real app instance across soak/stress cycles, per-step attribution of console errors, exceptions and crashes, and video reports with a virtual-cursor overlay.
- **Reliability of Always-On Software**: Diagnosed and eliminated renderer memory growth over 18+ hour unattended kiosk sessions and fixed leaking event listeners/timers, hardening the apps for continuous multi-day operation.
- **Customer Portal at Scale**: Built and grew the customer account portal at DOGMA from a Go MVP into a feature-rich product covering apartment search, paid online reservations integrated with an online cash register and fiscalization provider, and online mortgage origination integrated with multiple banking APIs.
- **Monolith → Microservices**: Refactored the customer portal monolith into focused Go microservices (deals service, upstream-CRM mirror service) communicating over gRPC, lifting reliability and enabling independent deployments.
- **Resilience via Messaging**: Introduced RabbitMQ as the backbone for talking to internal CRM, internal ERP, and third-party APIs — eliminating data-loss scenarios on outages and decoupling external integrations from request paths.
- **Data Migration**: Designed and ran an automated migration of the apartment catalog from a legacy CRM into PostgreSQL, enabling fast filtered search and unblocking modern UX features.
- **API Tooling**: Stood up a documented REST API on Fiber with Swaggo-generated OpenAPI specs, JWT auth/refresh middleware, GORM-backed PostgreSQL access, and Gothenberg-driven PDF generation; consolidated this stack as the template for new internal services.

## Professional Experience

### **TBFF (Talking Birds & Flying Fish)** — **Fullstack Developer** — _Dec 2025 — May 2026_

_Experiential studio building interactive touchscreen kiosk installations for large-scale industry events_

- Delivered cross-platform desktop applications (Electron, React, TypeScript, Vite) for dual-display touchscreen kiosks running unattended in kiosk mode: multi-screen narrative flows, timed mini-games, multilingual content, voice-over/audio, and auto-update.
- **Test automation**: designed a custom scenario-driven E2E testing framework on Playwright + Electron + TypeScript — declarative scenario configs describe user flows, a runner drives a real Electron instance across configurable soak/stress cycles, and an error-collection layer attributes console errors, exceptions and renderer crashes to the exact failing step.
- Made test runs reproducible and reviewable: video capture with a virtual-cursor overlay (desktopCapturer + ffmpeg WebM→MP4) and centralized `data-testid` selectors with a locator-resolution layer (testid / role / text / css) for specs stable against UI change.
- Built a second Playwright E2E suite for another kiosk app, covering app startup, slide transitions, inactivity/idle behavior, survey flows and token collection.
- **Memory-leak & reliability testing**: diagnosed renderer memory growth over 18+ hour kiosk sessions (soft navigation kept the renderer alive) and moved to a full app reload behind a seamless blackout transition; audited components and fixed a critical video event-listener leak.
- Authored and ran manual QA test plans covering dual-display behavior, full screen sequences, mini-games and the settings/kiosk configuration, complementing the automated suites.

### **DOGMA** — **Backend Developer** — _Sep 2019 — Jan 2024_

_Real-estate developer; in-house portfolio of customer, agency and counterparty portals integrated with the company's internal CRM and ERP systems_

- Started full-stack on Node.js / Express with React and Vue: redesigned company landing pages and the main site, migrated from a SPA to SSR for faster first paint and SEO, and moved hosting from static web-hosting to Dockerized services behind Nginx.
- Transitioned fully to Go backend: launched the company's first Go service — an apartment catalog with filtered search — and ran an automated migration of apartment data from the legacy CRM into PostgreSQL.
- Built the customer account portal in Go: JWT authentication, SMS-code registration via a third-party SMS gateway, favorites, and live status of the customer's deals from the upstream CRM.
- Delivered paid online apartment reservations (4-day hold) integrated with an online cash register API and a fiscal-data provider for receipts.
- Implemented online mortgage origination inside the customer portal, integrated with multiple banking APIs covering different lenders.
- Built the counterparty portal: deal status, and electronic document workflow with the company's internal ERP system for counterparty accreditation.
- Designed and shipped the realtor-agency portal: REST API initially on Echo, later migrated to Fiber for throughput; OpenAPI documentation via Swaggo; JWT auth-token + refresh-token middleware; PostgreSQL access through GORM; PDF generation via Gothenberg.
- Released a translation service used by mobile and frontend teams across the company.
- Adopted RabbitMQ for asynchronous communication with internal CRM, internal ERP, and third-party APIs, improving fault tolerance for bursty and unreliable upstreams.
- Refactored the customer portal monolith into Go microservices (deals service, upstream-CRM mirror service) communicating over gRPC.
- Onboarded one frontend engineer and one backend engineer; transferred ownership of legacy areas.

### **ShtrafovNet.ru** — **Backend Developer** — _Feb 2024 — Apr 2024_

_Service for tracking and resolving traffic fines_

- Built and refactored the REST API powering the public website and the web application.
- Streamlined endpoint contracts and internal data flows for faster, more predictable response times.

## Technical Skills

**Programming Languages**: Go, JavaScript, TypeScript
**Backend**: Go (Fiber, Echo, GORM), Node.js, Express, JWT (auth-token + refresh-token), OpenAPI/Swagger via Swaggo, Gothenberg (PDF generation), gRPC
**Frontend & Desktop**: React, Vue, HTML, CSS, Electron (electron-vite, electron-builder), Vite
**Testing & QA**: Playwright (E2E automation), Electron app testing, scenario / soak / stress testing, memory-leak diagnosis, manual test planning
**Databases & Caching**: PostgreSQL, MySQL, MongoDB, Redis
**Messaging & RPC**: RabbitMQ, gRPC, REST API
**APIs & Integrations**: internal CRM, internal ERP (accreditation, document workflow), banking APIs, online cash register / fiscal-data providers, SMS gateways, generic third-party REST APIs
**DevOps & Tooling**: Docker, Nginx, Linux, Git, SSR migration

## Education

**KAIT 20 — College of Automation and Information Technologies** — _2015_
_Industrial Automation Systems_

## Languages

- Russian — Native
- English — B1 (Intermediate)

## Additional Information

- **Availability**: Immediately available for Backend / Fullstack Developer roles at product companies.
- **Work Preferences**: Remote-first, full-time. Not available for business trips.
- **Target Stack**: Go services, REST/gRPC APIs, PostgreSQL/Redis, RabbitMQ, Docker, with frontend on React or Vue when needed.

---

[Full CV.pdf](https://github.com/Nedvokis/Nedvokis/raw/main/CV_FULL.pdf)
