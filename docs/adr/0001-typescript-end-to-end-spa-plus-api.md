# 0001 — TypeScript end-to-end: Vite React SPA + separate Hono API, Postgres + Prisma

CoCraft is a from-scratch learning vehicle for an engineer who is new to frontend, rusty on backend, and strong on ops. The goal is to *understand* fullstack mechanics, not to ship fastest. We chose TypeScript everywhere: a React SPA built with Vite, talking over HTTP/JSON to a separate Node + TypeScript API (Hono), backed by Postgres (run locally via Docker) through Prisma.

## Considered options & why

- **SPA + separate API instead of Next.js.** A meta-framework deliberately blurs the client/server boundary. We keep it explicit so the learner can watch HTTP requests cross the wire and form a correct mental model. Next.js is deferred to a later module ("how a meta-framework collapses this boundary").
- **Node + TypeScript backend instead of Go/Python, which the learner already knows.** One language end-to-end lets us share types across the wire (define `Expense` once) and removes language context-switching while the learner is loaded with React. Coasting on a familiar backend was rejected because backend fluency in the JS ecosystem is part of the goal.
- **Postgres over SQLite.** The usual beginner "avoid ops friction" argument for SQLite doesn't apply — this learner runs databases trivially, and Postgres is what they'll actually deploy. **Prisma** for schema clarity, migrations, and type-safety that extends the shared-type story.

## Consequences

Next.js, React Server Components, and the broader JS server ecosystem beyond Hono are intentionally *unlearned for now*, to be picked up deliberately as later modules.
