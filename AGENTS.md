# AGENTS.md
## Boundaries
- Do not edit files outside `plan/`, `src/`, `public/`, `docs/` without explicit ask.
- No secrets committed; use `.env.local` and `.gitignore`.
- All lesson content changes need a PR referencing the relevant TODO item.

## Workflow
- Branch per feature: `feat/<slug>`.
- Commit message format: `<type>(<scope>): <subject>`.
- Run `npm run lint` + `npm run test` before pushing.
