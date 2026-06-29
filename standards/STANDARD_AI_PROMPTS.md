# AI Prompt Standard

Status: Draft
Owner: Konstantin / Izumi IT
Purpose: Make AI-assisted work clearer, safer, and easier to review.

## Required sections

Prompts for meaningful work should include goal, context, constraints, files to inspect, scope, non-goals, validation, and expected output.

## Accuracy rule

AI should not invent facts.

If current facts are required, AI should inspect current sources or ask for them.

## Assumptions and risks

AI should mark assumptions, risks, missing context, and validation gaps.

## Implementation prompt rule

Implementation prompts must ask for changed files, diff/stat summary, validation commands and results, and remaining risks or follow-up items.

## Secrets rule

Prompts must not include secrets, credentials, private customer data, or unredacted security-sensitive logs.
