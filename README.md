# renovate-config

Shared Renovate preset and the single self-hosted Renovate runner of `thomas-lg`.

- `default.json`: the preset. A repository uses it with `"extends": ["github>thomas-lg/renovate-config"]` and adds
  only what is its own (managers, groups, ignores, auto-merge policy, base branch).
- `.github/workflows/renovate.yml`: runs Renovate daily at 01:00 UTC as the `thomas-lg-renovate` GitHub App, with
  autodiscover. **Installing the App on a repository enrols it**; a repository without a `renovate.json` gets an
  onboarding PR extending this preset. Run it by hand from the Actions tab (dry run, log level, or a list of
  repositories).
- Secrets of this repository: `RENOVATE_APP_ID`, `RENOVATE_APP_PRIVATE_KEY`.

New update PRs open on Monday mornings (Europe/Paris); the daily run picks up Dependency Dashboard checkboxes and
rebases. Documented in the homelab repository (`roadmap.md`, "Hermes handles the pending PRs").
