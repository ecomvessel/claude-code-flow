<!--
  EXAMPLE — per-repo CLAUDE.md for a LOW-STAKES repo (marketing site / staging).
  Fast-lane repos usually need NO per-repo file at all — the global rules already default new repos
  to Fast Lane. Add this only if you want to state it explicitly. Kept deliberately tiny.
-->

# Acme Marketing Site — Claude instructions

**Fast Lane** — low-stakes (marketing site, no customer data). Commit straight to `main`.

- Remote: `acme/marketing-site`
- Branch: `main` (auto-deploys on push)

## Workflow
```
git pull            # ALWAYS before editing — never edit stale/live code
# ...edit...
git commit -am "msg" && git push
```
- Pull before editing, every time. One terminal/folder per repo.
- No customer data here, so no Proper-Flow ceremony — but still never deploy from a stale state.
- Auto-merge/auto-push is fine here ONLY if an automated check (CI or local build) actually passed;
  otherwise the agent shows a one-line summary and asks first.
