# Airbyte

Data integration platform for ELT pipelines from APIs, databases, and files to warehouses and lakes.

**Language:** Python

## Structure

- `airbyte-cdk/` — Connector Development Kit
- `airbyte-integrations/` — Connectors and destinations
- `docs/` — Documentation

## Commit Style

- Plain-text capitalized title, no conventional-commit prefix
- Body with labels: `Design:`, `Related:`, `Closes #`
- Keep Markdown lines wrapped at 80 columns and run `nix fmt` before shipping

## Stack

- 1 commit == 1 PR via ghstack
- Amend + `ghstack` to resubmit
- `ghstack land` on head PR to land the entire stack
- Never `gh pr merge` (creates poisoned commits)
- Never force-push ghstack branches
- ghstack only works on HEAD commit chains, not detached HEADs

## Protect `main`

- Require 1 approving review
- Require linear history (no merge commits)
- Require signed commits
- Squash+rebase merge only

*Follow the connector specification. Test all connectors before committing*