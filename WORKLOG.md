# Worklog

## 2026-05-22 — Published PM interview prep system to GitHub

**Did:**
- Read `WHAT-WE-BUILT.md` to confirm scope of the system (8 categories, 9 frameworks, plugin architecture, 35 files).
- Initialized git at the repo root, added `.gitignore` covering OS/Python/Node noise plus `/RESUME.md` and `/resume/` per the Developer-folder convention.
- Single initial commit with all files: `_core/`, `plugins/` (8 categories), `questions/` (DAY-05-22 generated set), `config.yaml`, docs.
- Created GitHub repo via `gh` and pushed: https://github.com/devsandip/pm-interview-prep
- Flipped repo visibility from private to public.

**State now:**
- Repo is live and public at `devsandip/pm-interview-prep`, tracking `main`.
- Working tree clean.
- Generated practice questions for 2026-05-22 are checked in (under `questions/<category>/DAY-05-22.md`). These will accumulate daily as Cowork runs the scheduled task.

**Next:**
- Decide whether daily generated `questions/**/DAY-MM-DD.md` files should stay in the repo or be gitignored. If staying, no action. If not, add `questions/**/DAY-*.md` to `.gitignore` and `git rm --cached` the existing eight.
- Add a LICENSE (likely MIT given public visibility) — none exists yet.
- The `README.md` is the original system README; consider whether it needs a GitHub-facing rewrite that leads with what the project is and how to use it.

**Decisions:**
- Repo name: `pm-interview-prep` (matches the GitHub structure suggested in `WHAT-WE-BUILT.md`).
- Initial visibility was private; flipped to public on request. The `questions/` folder contains today's generated questions but no personal answers yet, so nothing sensitive.
- Kept the existing `_core/`, `plugins/`, `questions/` layout as-is rather than migrating to the `core/` + `examples/questions/` structure suggested in `WHAT-WE-BUILT.md`. That migration is a separate decision.
