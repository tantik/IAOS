# Product Development Workflow

Status: Draft
Owner: Konstantin / Izumi IT
Purpose: Define a practical workflow from product idea to merged change for LINE Business OS.

## Scope

Use this workflow for meaningful product, engineering, documentation, or operational changes related to LINE Business OS.

For tiny typo fixes or emergency maintenance, use judgment, but still preserve source-of-truth updates when needed.

## 1. Idea

Capture the user or customer problem, expected outcome, affected product area, and why it matters now.

Do not start implementation from a vague idea.

## 2. Clarification

Clarify who the change is for, current behavior, desired behavior, constraints, known risks, and source files or systems involved.

If market, legal, pricing, compliance, or customer claims are involved, use current verified sources before documenting them.

## 3. Scope

Define what is in scope, what is out of scope, the smallest useful version, acceptance criteria, and validation method.

Prefer small changes that can be reviewed and merged safely.

## 4. Architecture check

Before implementation, check whether the change fits the current LINE Business OS architecture, creates duplicate logic or duplicate source of truth, affects security or deployment, or requires an IAOS standard or decision update.

If the decision is significant, create or update an ADR.

## 5. Cursor/Codex implementation prompt

Use `prompts/CURSOR_TASK_PROMPT.md`.

The prompt must include goal, context, files to inspect, scope, non-goals, constraints, validation steps, and expected output.

## 6. Local validation

Run the smallest useful validation available:
- tests;
- lint or typecheck;
- build;
- local manual check;
- documentation review.

Record what was run and what passed or failed.

## 7. Git branch

Use a feature branch for meaningful changes.

Branch names should be clear and practical, for example:
- `feature/line-reservation-flow`
- `fix/customer-sync-error`
- `docs/iaos-workflow-update`

## 8. Pull Request

For significant changes, open a pull request with summary, scope, screenshots or examples where useful, validation results, risks or assumptions, and follow-up tasks if needed.

## 9. Review

Review for correctness, product fit, architecture concerns, security, duplication, missing validation, and documentation updates.

AI output must be reviewed before merge.

## 10. Merge

Merge only when scope is understood, validation is acceptable, review concerns are resolved or deliberately accepted, and source-of-truth documents are updated where needed.

`main` should remain stable.

## 11. Cleanup

After merge, remove temporary notes or debug code, close related tasks, check whether follow-up issues are needed, and archive outdated material if it should not remain active.

## 12. IAOS update

Update IAOS when the work changes a repeated workflow, engineering or documentation standard, important decision, reusable AI prompt, current state, or strategic direction.

If IAOS does not need an update, note that in the PR or review summary.
