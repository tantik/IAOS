# Git Workflow Standard

Status: Draft
Owner: Konstantin / Izumi IT
Purpose: Define practical Git rules for Izumi IT repositories.

## Branches

`main` is stable.

`dev` may be used for integration where applicable.

Use feature branches for meaningful changes.

## Pull requests

Use pull requests for significant changes, especially changes that affect product behavior, data model, security, deployment, customer-facing content, or IAOS standards and decisions.

## Risk rule

Do not make direct risky changes without review.

Risky changes include production behavior, security-sensitive code, migrations, billing, customer data, and public claims.

## Commit messages

Commit messages should be clear and practical.

Prefer messages such as:
- `docs: add IAOS foundation workflow`
- `fix: handle LINE webhook retry error`
- `feature: add reservation status filter`

## Review history

GitHub should preserve meaningful review history for product and operating-system changes.
