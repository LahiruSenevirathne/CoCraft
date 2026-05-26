# Suivi — Skills Map

The *what-to-learn* view. [`ROADMAP.md`](./ROADMAP.md) is the build sequence; this is the cross-cutting inventory of fullstack **skills** you acquire along the way, independent of which feature they appear in.

This is a **map + tracker, not a syllabus** — it respects the just-in-time decision (ADR 0002). Skills are tagged with the module where they *first* show up, but they're learned when the build reaches them, not on a schedule. The `/teacher` and `/pair` personas and `/log-progress` keep the statuses current.

**Mastery:** ⬜ Not yet · 🟡 Learning · ✅ Can do unaided
**First in:** the module (per ROADMAP) where the skill first appears — `Primer`, `0001`…`0007`

## React & frontend

| Skill | First in | Status |
|---|---|---|
| Declarative UI mental model (`UI = f(state)`) | Primer | ⬜ |
| JSX | Primer | ⬜ |
| Components & composition | Primer | ⬜ |
| Props | 0001 | ⬜ |
| State with `useState` | 0001 | ⬜ |
| Rendering lists & keys | 0001 | ⬜ |
| Controlled form inputs | 0001 | ⬜ |
| Conditional rendering | 0001 | ⬜ |
| Side effects with `useEffect` | 0001 | ⬜ |
| Data fetching + loading/error UI | 0001 | ⬜ |
| Basic CSS & layout | 0001 | ⬜ |
| Lifting state up | 0002 | ⬜ |
| Client-side routing | 0003 | ⬜ |
| Global state via Context (auth) | 0003 | ⬜ |
| File upload UI | 0005 | ⬜ |
| Charts / data viz | 0006 | ⬜ |

## TypeScript

| Skill | First in | Status |
|---|---|---|
| Basic types & interfaces | Primer | ⬜ |
| Typing component props | 0001 | ⬜ |
| Typing API request/response shapes | 0001 | ⬜ |
| **Shared types across the wire** (client ↔ server) | 0001 | ⬜ |
| Generics (basics) | 0001 | ⬜ |
| Unions & narrowing | 0003 | ⬜ |

## Backend — Node & Hono

| Skill | First in | Status |
|---|---|---|
| HTTP & REST fundamentals | 0001 | ⬜ |
| Routing & handlers (Hono) | 0001 | ⬜ |
| Request parsing & JSON responses | 0001 | ⬜ |
| Input validation | 0001 | ⬜ |
| Error handling & status codes | 0001 | ⬜ |
| Middleware | 0003 | ⬜ |
| Auth: sessions/JWT, password hashing | 0003 | ⬜ |
| Authorization & multi-tenant scoping | 0003 | ⬜ |
| Background jobs / scheduling | 0004 | ⬜ |
| File upload handling & blob storage | 0005 | ⬜ |

## Data — Postgres & Prisma

| Skill | First in | Status |
|---|---|---|
| Schema modeling (Prisma schema) | 0001 | ⬜ |
| Migrations | 0001 | ⬜ |
| CRUD queries (Prisma Client) | 0001 | ⬜ |
| Relations & foreign keys | 0002 | ⬜ |
| Querying across relations | 0002 | ⬜ |
| Aggregation / grouping queries | 0006 | ⬜ |
| Indexing basics | 0006 | ⬜ |

## Fullstack wiring

| Skill | First in | Status |
|---|---|---|
| The client/server contract (request → wire → handler) | 0001 | ⬜ |
| End-to-end loading & error states | 0001 | ⬜ |
| Environment config & secrets | 0001 | ⬜ |
| CORS / dev proxy | 0001 | ⬜ |
| Optimistic updates | 0006 | ⬜ |

## Ops & deploy — *existing strength (apply & review, not learn)*

| Skill | First in | Status |
|---|---|---|
| Dockerize frontend + API | deploy | ✅ |
| docker-compose (incl. Postgres) | 0001 | ✅ |
| CI pipeline | deploy | ✅ |
| Deploy to cloud / k8s | deploy | ✅ |

## Product & process

| Skill | First in | Status |
|---|---|---|
| Refining a PRD (scope, acceptance criteria) | 0001 | ⬜ |
| Scope discipline (in / out of scope) | 0001 | ⬜ |
| Recognizing an ADR-worthy decision | ongoing | 🟡 |
| Domain language / glossary discipline | ongoing | 🟡 |
