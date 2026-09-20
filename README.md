<<<<<<< HEAD
# Lumbol Lawrence Tityem — Portfolio Website

A single-page portfolio showcasing backend engineering work in fintech —
distributed systems, event-driven architecture, and production-mindset
observability — alongside teaching experience and certifications.

## 🚀 Live Demo
https://lawrence-tityem-portfolio.vercel.app

## 📌 About
B.Sc. Computer Science graduate (University of Jos, 2025) and NYSC State
Honors Awardee, focused on backend engineering: distributed systems,
event-driven architecture, idempotency, and observability. Also a
digital technology teacher for secondary and primary school students in Nigeria.

## 🛠 Built With
- **HTML5** — semantic structure, native `<details>`/`<summary>` for
  expandable case studies (no JavaScript needed for that interaction)
- **CSS3** — custom properties (design tokens), CSS Grid, Flexbox,
  responsive media queries, `prefers-reduced-motion` support
- **Vanilla JavaScript** — none required yet; added only if future
  interactivity (e.g. live architecture diagrams) needs it
- **Fonts** — Fraunces, IBM Plex Sans, IBM Plex Mono, loaded via Google
  Fonts CDN

**Deliberately zero build step and zero npm dependencies.** Everything
lives in one `index.html` file: no framework, no bundler, no
`node_modules`. This means the entire site can be opened directly in a
browser, edited by hand, and deployed with no configuration at all —
a decision made specifically to keep the whole codebase legible and
independently maintainable.

> Earlier drafts of this README described a Next.js/Tailwind/TypeScript
> stack. That no longer reflects what's actually built and has been
> corrected here — this site intentionally does not use a framework.

## 🎨 Design Approach
A restrained "engineering ledger" aesthetic — left-aligned single
column, hairline dividers instead of card-and-shadow UI, a serif
display face reserved for one moment (the name), and a muted gold
accent used only for verified/passing signals. The goal is a page that
reads like a systems report, not a marketing landing page.

## 📂 Sections
1. **Hero** — name, role, one-line pitch, key links
. **Selected Systems** — expandable case studies for flagship projects
3. **Stack** — skills grouped by category, matched to what's actually
   used in the featured projects
4. **Certifications & Honors**
5. **Also Built** — supporting project (proves range without competing
   for attention with the backend/fintech focus)
6. **Teaching**
7. **Contact**

## 🎯 Projects Featured
1. **Sentinel Financial Ecosystem** — production-grade distributed
   fintech backend: wallet transfers, fraud detection, observability.
   9.2/10 mentor rating, 49 passing tests.
   GitHub: https://github.com/lawrence-tityem/Sentinel-Financial-Ecosystem 
2. **Event-Driven Order Processing System** — Kafka-based event-driven
   companion system demonstrating the dual-write problem and idempotent
   consumption. In progress.
   GitHub: https://github.com/lawrence-github 
3. **api-gateway-system** — in progress, not yet added to the live site.
   Will be added once complete.

## 🏅 Certifications & Honors
- B.Sc. Computer Science — University of Jos, Nigeria (2024)
- NYSC State Honors Awardee — Adamawa State (2025)
- Cybersecurity Certificate — Cisco Networking Academy

## 🖥 Running Locally
No install, no server, no dependencies:

```
Just double-click index.html — it opens directly in your browser.
```

## ☁️ Deployment
Deployed on **Vercel (free tier)**:
1. Push this repo to GitHub.
2. Import the repo in Vercel.
3. Vercel auto-detects it as a static site — no build command, no
   environment variables, no configuration needed.
4. Live in under a minute.

## 🤝 Connect
- **Email**: lumbolt@gmail.com
- **GitHub**: https://github.com/lawrence-tityem
- **LinkedIn**: https://linkedin.com/in/lawrence-tityem
- **Location**: Anambra State, Nigeria

## 🔜 Not Yet Done
Listed honestly rather than omitted:
- Real LinkedIn URL still a placeholder
- Project GitHub links currently point to the profile, not the actual
  repos — update once repo names are finalized
- `api-gateway-system` project not yet added to the live site
- No Open Graph/social preview image yet, so link shares (LinkedIn,
  Twitter) currently show no thumbnail
=======
# Lawrence Lumbol Tityem
**Backend Engineer | Distributed Systems | Fintech**

I'm a backend engineer based in Nigeria, focused on building reliable systems where correctness matters.

My work is centered around problems such as:
- Concurrent state changes and transaction integrity
- Idempotency and duplicate request handling
- Event-driven systems and asynchronous workflows
- Retries, dead-letter queues, and failure recovery
- API reliability, rate limiting, and service boundaries
- PostgreSQL-backed systems and data consistency
- Observability, testing, and operational visibility

I completed a B.Sc. in Computer Science at the University of Jos in 2025 and I'm currently looking for my first professional backend engineering role.

---

## Selected Work

### [Sentinel Financial Ecosystem](https://github.com/lawrence-tityem/sentinel-financial-ecosystem)
A distributed fintech backend for peer-to-peer wallet transfers. The system deals with concurrent balance mutations, idempotent transaction requests, fraud-service failures, asynchronous notifications, rate limiting, and observability.

**Key engineering decisions**
- PostgreSQL row-level locking with deterministic lock ordering
- Redis-backed idempotency for mutating requests
- Fraud detection with bounded retries and explicit failure behaviour
- Asynchronous notification processing with Celery
- Prometheus, Grafana, OpenTelemetry, and structured logging
- 49 passing tests across authentication, wallet, transfer, fraud, and rate-limiting paths

### [Event-Driven Order Processing System](https://github.com/lawrence-tityem/event-driven-order-processing-system)
A Kafka-based microservice system where independently owned services communicate through events rather than a shared database. Explores the difficult parts of event-driven architecture: at-least-once delivery, idempotent consumers, service-owned data, rejected orders, dead-letter handling, and the dual-write problem.

**Key engineering decisions**
- Kafka KRaft for event transport
- Database-per-service architecture
- Idempotent event consumers
- Explicit retry and dead-letter paths
- Payment processing triggered by inventory reservation rather than order creation
- Notification processing for rejected orders
- Documented trade-offs around transactional consistency and event publication

### [Distributed Job Queue System](https://github.com/lawrence-tityem/distributed-job-queue-system)
A PostgreSQL-native background job queue designed to explore reliable work distribution without introducing Redis or Kafka as another infrastructure dependency.

**Key engineering decisions**
- PostgreSQL as both queue and source of truth
- `SELECT ... FOR UPDATE SKIP LOCKED` for concurrent worker claims
- Priority ordering with FIFO behaviour within priority levels
- Visibility timeouts for crash recovery
- Exponential backoff and dead-lettered jobs
- 21 passing tests, including a real-concurrency proof against live PostgreSQL

### [API Gateway & Request Processing System](https://github.com/lawrence-tityem/api-gateway-and-request-processing-system)
A production-style gateway for backend services that centralizes concerns that otherwise get duplicated across individual services.

**Focus areas**
- JWT authentication
- Request routing
- Rate limiting
- Timeouts and retries
- Circuit breaking
- Correlation IDs
- Structured logging
- Centralized error handling

One deliberate reliability rule: non-idempotent POST requests are not blindly retried, because a lost response does not necessarily mean the original request failed.

---

## Technical Focus

**Backend:** Python · FastAPI · SQLAlchemy · Pydantic
**Data:** PostgreSQL · Redis · asyncpg
**Messaging & Distributed Systems:** Kafka · Kafka KRaft · event-driven architecture · idempotent consumers · retries · DLQs · asynchronous workers
**Reliability & Observability:** Prometheus · Grafana · OpenTelemetry · structured logging · rate limiting · circuit breakers
**Infrastructure:** Docker · Docker Compose
**Testing:** pytest · pytest-asyncio · integration testing · concurrency testing

---

## How I Think About Backend Systems

I care about what happens when the happy path stops being true.

- What happens when the same request arrives twice?
- What happens when two transactions modify the same state concurrently?
- What happens when a downstream service times out after the operation may already have succeeded?
- What happens when a worker crashes halfway through processing a job?
- What happens when a database write succeeds but publishing the corresponding event fails?

Those failure modes are where I currently spend most of my engineering attention.

---

## Background

- B.Sc. Computer Science — University of Jos, Nigeria, 2025
- NYSC State Honors Award — Adamawa State, 2025
- Cybersecurity Certificate — Cisco Networking Academy
- Digital technology teacher in Nigeria

Teaching has also shaped how I approach engineering: I try to make system behaviour, trade-offs, and failure modes understandable rather than hiding them behind abstractions.

---

## Current Direction

I'm looking for my first professional backend engineering opportunity.

Fintech is a strong area of interest because of the engineering constraints around payments, transaction integrity, fraud, consistency, and reliability — but I'm not limiting myself to fintech. I'm interested in teams building serious backend systems, infrastructure, APIs, data-intensive services, and distributed workflows.

📍 Based in Nigeria. Open to local and remote opportunities.
>>>>>>> 97c4c9b12eb28cc0e827562fea10ff8486014acf
