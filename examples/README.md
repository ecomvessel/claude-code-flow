# Examples — filled-in configs you can copy from

The `templates/` are blank with `<PLACEHOLDER>`s. These are the **same files, filled in** with real
model names and repo settings, so you can see what a finished config actually looks like before you
write your own. They're sanitized (fake repo names/paths) — swap in yours.

| Example | Fits you if… |
|---------|--------------|
| [`multi-model-plan/`](./multi-model-plan) | Your Claude plan has several model tiers and you want full delegate-down / escalate-up routing. |
| [`one-model-plan/`](./one-model-plan) | You have a single model. No switching — but you still get the safe branch → PR → merge flow. |
| [`production-saas-repo/`](./production-saas-repo) | A per-repo `CLAUDE.md` for a real production/customer-data repo (Proper-Flow lane). |
| [`marketing-site-fast-lane/`](./marketing-site-fast-lane) | A low-stakes repo (marketing/staging). Fast lane — usually needs no per-repo file at all; this shows the minimal one. |

Model names below are examples as of 2026 — replace with whatever tiers your plan gives you. The
point is the *roles*, not the names (see [`../MODEL_TIERS.md`](../MODEL_TIERS.md)).
