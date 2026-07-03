<!--
  EXAMPLE — global ~/.claude/CLAUDE.md for a SINGLE-model plan.
  No delegate-down / escalate-up switching (there's only one model), but you keep the full
  safe-shipping flow, Definition of Done, and Merge-Safety gate. That's most of the value.
-->

# Verify Before Recommending (applies to EVERY session)

Before offering next steps, re-check the LIVE repo/PR/prod state (git fetch, gh pr view, actual
files) — do not rely on memory or previous messages. Show evidence before any merge/deploy/migration.

# Model Routing (applies to EVERY session)

Only one model available (**Sonnet 5**), so there is no tier switching. Instead:
- Still **delegate to subagents** for bulk reading and mechanical work to keep the main thread
  focused — same model, fresh context, scoped (no deploy/merge/live-API).
- The "escalate up = ask first" gate collapses, but the **PRODUCTION-ACTION gate stays**: merging to
  the live branch, deploying, prod DB/migrations, or prod env/secrets ALWAYS ask first.

# Model Fallback

Single tier: **Sonnet 5**. If it's unavailable, STOP and tell the human — there's no lower tier to
fall back to. Don't silently proceed.

# Two Lanes, Definition of Done, Independent Verify, Merge-Safety Agent, Auto Mode Hard Line
# → identical to templates/CLAUDE.global.md; copy those sections in verbatim.
#   (The Independent-Verify step still works: it's a FRESH subagent, not a different model —
#    independence comes from clean context, which you have even on one model.)
