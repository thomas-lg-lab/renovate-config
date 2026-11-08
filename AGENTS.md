# Working on this repository (humans and agents)

- **`default.json` is the shared Renovate preset** of every repository of the organisation: a change here reaches
  all of them at the next run. Keep repository-specific rules in each repository's `renovate.json`.
- **The runner** (`.github/workflows/renovate.yml`) acts as the organisation's Renovate App; its secrets stay in
  the repository settings, never in a file, a commit message or a log. Test a change with a manual dry run.
- **PR titles** are Conventional Commits (required `conventions / title` check); Renovate's own PRs use
  `fix(deps):` for production dependencies and `chore(deps):` for the rest. Issue forms, the PR template and how
  to fill them come from the organisation's `thomas-lg-lab/.github`.
- Technical files are written in English.
