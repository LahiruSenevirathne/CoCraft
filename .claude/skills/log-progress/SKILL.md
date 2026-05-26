---
name: log-progress
description: Record or update progress on the CoCraft fullstack learning journey. Use at the end of a working/learning session, after completing a concept or module, or when Lahiru asks "where did I leave off?" / "where am I?". Maintains PROGRESS.md — a dated session journal and a per-module status table.
---

# Log learning progress

Keep [`PROGRESS.md`](../../../PROGRESS.md) an honest, current picture of where Lahiru is on the CoCraft learning journey.

## When invoked

1. **Read** `PROGRESS.md`, `ROADMAP.md`, and `SKILLS.md` for the current state, the plan, and the skills map.
2. **Reconstruct what actually happened this session** from the conversation: which module/concepts were worked on, what Lahiru wrote *himself*, what clicked, where he struggled.
3. **Append a dated entry to the top of the Session log** in `PROGRESS.md`:
   - Today's date.
   - Module / concepts covered.
   - What was learned — concrete takeaways, not "we discussed X".
   - Sticking points or things to revisit.
   - What's next.
4. **Update the Status table** (`PROGRESS.md`) — move items to 🟡 In progress or ✅ Done, and refresh the Notes column.
5. **Update the skills map** (`SKILLS.md`) — tick the competencies Lahiru *actually demonstrated* this session (🟡 Learning / ✅ Can do unaided). Same honesty rule.
6. **Keep the `Currently:` line** at the top of `PROGRESS.md` accurate.

## Rules

- **Be honest.** Mark a concept ✅ Done only if Lahiru actually demonstrated it — he wrote the code, it worked, and he can explain it. "Saw it explained" is *not* done; use 🟡 In progress liberally. An inflated log is worse than none.
- **Table = module level; journal = concept level.** Keep the table skimmable; put the detail in the log entry.
- **Append, don't rewrite.** New entries go above older ones. Don't edit past entries except to fix an outright error.
- **Respect the teaching contract** (`AGENTS.md` / ADR 0002): this skill *records* the journey — it never does the learning for him.
- **If invoked to resume** ("where did I leave off?"), don't write — summarise the latest log entry plus the `Currently:` / Next state, then hand back.
