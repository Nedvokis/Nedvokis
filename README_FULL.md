# Denis Khilkov

**Fullstack Developer**

## Contact

- **Email:** d.khilkov@gmail.com
- **Telegram:** @Nedvokis
- **GitHub:** github.com/Nedvokis

## Professional Summary

Pragmatic Fullstack Developer with 4+ years of hands-on experience building business-critical web services in Go and Node.js, with a strong backend focus and production frontend work in React and Vue. Deep experience designing and shipping REST APIs on Fiber and Echo with GORM and PostgreSQL, JWT authentication and refresh-token rotation, and OpenAPI documentation generated from code via Swaggo. Proven track record integrating customer-facing portals with payment and fiscalization providers, banking APIs covering multiple lenders for online mortgage origination, and with the company's internal CRM and ERP systems for deals and electronic document workflow. Comfortable evolving monolithic services into focused Go microservices on gRPC, hardening reliability with RabbitMQ, and containerizing the full stack with Docker behind Nginx. Remote-first, immediately available, ready to own product features end-to-end from API design and data modeling through deployment.

## Core Competencies

- **Backend:** Go (Fiber, Echo, GORM), Node.js, Express, JWT (auth-token + refresh-token), OpenAPI/Swagger via Swaggo, Gothenberg (PDF generation), gRPC
- **Frontend:** React, Vue, HTML, CSS, SPA → SSR migration
- **Databases & Caching:** PostgreSQL, MySQL, MongoDB, Redis
- **Messaging & RPC:** RabbitMQ, gRPC, REST API
- **Integrations:** internal CRM, internal ERP (accreditation, document workflow), banking APIs, online cash register / fiscal-data providers, SMS gateways, generic third-party REST APIs
- **Quality & Tooling:** Git, Docker, Nginx, Linux
- **Practices:** REST API design, microservices decomposition, schema migrations, asynchronous integration with unreliable upstreams

## Selected Achievements

- **DOGMA:** Built the customer account portal in Go from scratch — JWT authentication, SMS-code registration via a third-party SMS gateway, favorites, live deal status from the upstream CRM — and grew it into the company's main customer-facing product.
- **DOGMA:** Delivered paid online apartment reservations integrated with an online cash register API and a fiscal-data provider for receipt generation.
- **DOGMA:** Implemented online mortgage origination inside the customer portal, integrated with multiple banking APIs covering different lenders.
- **DOGMA:** Refactored the customer portal monolith into focused Go microservices (deals service, upstream-CRM mirror service) communicating over gRPC.
- **DOGMA:** Introduced RabbitMQ as the backbone for talking to the internal CRM, internal ERP, and third-party APIs — eliminating data-loss scenarios on outages and decoupling external integrations from request paths.
- **DOGMA:** Designed and ran the automated migration of the apartment catalog from a legacy CRM into PostgreSQL, unblocking filtered search and modern UX features.

## Professional Experience

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
