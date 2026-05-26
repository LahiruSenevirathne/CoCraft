# CoCraft — Study Plan & Roadmap

The learning journey and the build are the same thing: **Suivi**, a household management app, built one vertical slice at a time in the **CoCraft** project, as the vehicle for learning fullstack development.

- **Language** is defined in [`CONTEXT.md`](./CONTEXT.md) — the glossary every PRD and ADR is held to.
- **Hard decisions** live in [`docs/adr/`](./docs/adr/) — stack ([0001](./docs/adr/0001-typescript-end-to-end-spa-plus-api.md)) and methodology ([0002](./docs/adr/0002-spine-and-modules-taught-socratically.md)).
- **Per-feature plans** live in `docs/prd/`, numbered like ADRs.

## The loop (every module runs this)

1. **PRD.** The agent drafts a PRD in `docs/prd/` (problem · user story · in-scope / out-of-scope · acceptance criteria · learning objectives · new domain terms). The learner refines it.
2. **Grill.** Interrogate scope, sharpen `CONTEXT.md` terms, write an ADR if a decision clears the bar (hard to reverse · surprising · a real trade-off).
3. **Learn by building (JIT).** Concepts are introduced exactly when the module needs them. The learner writes **all** frontend + unfamiliar backend (Socratic: escalating hints, never the solution — except on an explicit "show me"). The agent writes infra/deploy; the learner reviews.
4. **Ship.** Build → review → it works end-to-end. Then the next module.

## Sequence

**React primer** *(pre-spine, ~1 sitting)* — the mental model only: declarative UI, `UI = f(state)`, components, JSX.

| # | Module | Unlocks |
|---|--------|---------|
| 0001 | **Expense spine** | The whole machine, thin: components, controlled forms, list rendering, `useState`; Hono REST; Prisma schema + migration; fetch + loading/error states; **types shared across the wire**; a monthly total. *How a full vertical slice fits together.* |
| 0002 | **Categories** | A second entity and your first **relation** (Expense → Category), CRUD UI, select inputs. *Relations and a second resource; reinforces the spine pattern.* |
| 0003 | **Households & auth** | Signup/login, password hashing, sessions/JWT, scoping all data to a Household; frontend auth context, protected routes. *Identity, access control, multi-tenancy — placed early so the data model learns scoping while small.* |
| 0004 | **Bills** | Recurring obligations, due dates, **background jobs/scheduling**, reminders; paying a Bill creates an Expense. *Time, async work, scheduled tasks.* |
| 0005 | **Purchases, Items & Warranties** | **File/image upload** (receipts, warranty PDFs) + blob storage; the Expense → Purchase → Item → Warranty chain; expiry alerts. *File handling and richer domain modeling.* |
| 0006 | **Dashboard** | Spend by category/month, trends; **aggregation queries** + charts. *Data aggregation and visualization.* |
| 0007 | **Pets** *(capstone)* | Pet profiles, vet visits, vaccination schedules. Built **near-solo** to prove the training took. *Consolidation.* |

## Deployment

Woven in, not a phase. The spine ships to real infrastructure early — the agent writes the Docker/CI/k8s (the learner's home turf), the learner reviews — so the app is *live* fast and new knowledge connects to existing mastery. Specific target decided at the spine's deploy step.

## Stack

TypeScript end-to-end (see ADR 0001): **Vite + React** SPA ↔ **Node + Hono** API ↔ **Postgres** (Docker) via **Prisma**.

---

**Status:** Plan complete. Next up → React primer, then the agent drafts **PRD 0001 — Expense spine**.
