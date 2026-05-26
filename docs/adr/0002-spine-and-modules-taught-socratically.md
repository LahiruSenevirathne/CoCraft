# 0002 — Spine-and-modules build, taught Socratically

CoCraft exists to *teach* fullstack development, not merely to be built — so how it's built is a first-class decision. We build one vertical slice end-to-end before adding anything else, and we teach by having the learner write the code.

## Decision

- **Spine and modules.** Build the Expense spine all the way through — DB → API → UI → deployed — before adding any module. Each later module (Bills, Purchases/Warranties, Pets, multi-user, dashboards, …) is added one at a time, each via its own PRD, and an ADR when the decision clears the bar. The project stays shippable at every step.
- **Pure Socratic on the gap.** For the learning gap (frontend + unfamiliar backend) the learner writes *every line*; the agent explains concepts, points at docs, reviews, and gives escalating hints — but not solutions, except on an explicit "show me."
- **Agent-authored on strengths.** For the learner's existing expertise (Docker, CI/CD, k8s, IaC) the agent writes the code and the learner reviews. No wasted reps re-deriving mastered skills.
- **The agent drafts PRDs; the learner refines.** Each module's PRD is authored by the agent and refined/critiqued by the learner (the learner's deliberate choice — reaffirmed when offered a blank-page alternative). Product thinking is practised through critique rather than authoring.

## Why

A thin end-to-end spine keeps the project shippable and motivating and avoids the classic "four shallow half-features, nothing deployed" death of learning projects. Socratic-on-the-gap maximizes retention where it matters most (frontend is muscle memory); agent-authored-on-strengths spends the learner's time where there's something to learn.
