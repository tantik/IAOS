# AI-Assisted Development Workflow

Status: Draft
Owner: Konstantin / Izumi IT
Purpose: Define how Izumi IT uses AI tools for development without losing review control or source-of-truth discipline.

## Tool roles

### ChatGPT

Use ChatGPT for strategy, architecture discussion, planning, product clarification, review prompts, documentation drafting, and risk analysis.

### Cursor/Codex

Use Cursor/Codex for inspecting repositories, implementing code and documentation changes, running validation, summarizing diffs, and preparing review notes.

### GitHub

Use GitHub for repository source of truth, branches, pull requests, review history, issues or tasks where applicable, and accepted documentation and decision records.

## Development loop

1. Read `BOOT.md` and relevant repository files.
2. Clarify goal, scope, constraints, non-goals, and validation.
3. Ask AI to inspect the relevant files before proposing or editing.
4. Make small, reviewable changes.
5. Run appropriate validation.
6. Review AI output before merge.
7. Update IAOS if the work changes a repeated workflow, standard, prompt, or decision.

## AI review rule

AI output must be reviewed before merge.

The reviewer is responsible for correctness, security, customer promises, source-of-truth accuracy, and final product quality.

## Secrets rule

Never paste secrets into AI chats.

Do not paste API keys, database passwords, access tokens, private customer data, production credentials, or unredacted security-sensitive logs.

Use environment variables, secret managers, and redacted examples instead.

## Assumptions rule

AI must mark assumptions and risks.

If current facts are required, AI should ask for or inspect current sources rather than inventing facts.
