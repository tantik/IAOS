# IAOS Boot

Status: Active  
Owner: Konstantin / IAC  
Last updated: 2026-08-01  
Purpose: Define the minimum context every human or AI session must read before performing IAOS or IAC-level work.

## 1. Read first

Before making IAOS or IAC-level changes, read:

1. [README.md](README.md)
2. [IAC_CONTEXT.md](IAC_CONTEXT.md)
3. [docs/IAC_CURRENT_STATUS.md](docs/IAC_CURRENT_STATUS.md)

Then read only the documents relevant to the current task:

- [docs/IAC_MASTER_PLAN.md](docs/IAC_MASTER_PLAN.md) for strategy, roadmap, priorities, and stage definitions;
- [docs/IAC_DECISIONS_INDEX.md](docs/IAC_DECISIONS_INDEX.md) for accepted decisions;
- `decisions/` for full IAOS decision records;
- `workflows/` for repeatable operating workflows;
- `standards/` for IAOS standards;
- `prompts/` for reusable AI task templates.

Do not load the entire repository when the task only requires a small subset of context.

## 2. IAC repository roles

The IAC ecosystem currently uses three separate repositories.

### IAOS

Repository:

`tantik/IAOS`

Local path:

`D:\Dev\IAOS`

Authority:

- IAC strategy;
- Active Stage;
- product portfolio priorities;
- major company decisions;
- stage definitions;
- current high-level status.

IAOS defines what IAC is doing and why.

### OAES

Repository:

`tantik/oaes`

Local path:

`D:\Dev\oaes`

Authority:

- AI-assisted engineering standards;
- engineering rules;
- Definition of Done;
- review practices;
- workflow checklists;
- AI-provider adapters.

OAES defines how engineering work should be performed.

OAES is not an AI-agent platform and is not the IAC AI Workforce.

### ORUWA Business OS

Repository:

`tantik/line-business-os`

Local path:

`D:\Dev\line-business-os`

Authority:

- application code;
- product implementation;
- database and migrations;
- RLS and tenant isolation;
- product architecture;
- tests;
- CI;
- preview evidence;
- technical ADRs;
- product completion evidence.

ORUWA Business OS defines what is technically implemented and verified.

## 3. Source-of-truth precedence

Use the following precedence rules.

### Strategy and Active Stage

IAOS is authoritative.

### General engineering workflow

OAES is authoritative.

### Product implementation and technical evidence

The relevant product repository is authoritative.

For the current product, this is:

`tantik/line-business-os`

### Conflict rule

If two sources conflict:

1. Do not guess.
2. Do not silently choose one.
3. Identify the exact conflicting statements.
4. Report the conflict.
5. Wait for a human decision when the conflict affects architecture, security, billing, production, permissions, or product scope.

Chat memory, AI memory, IDE context, and conversation history are supporting context only. They are not official evidence unless the relevant information is recorded in a source-of-truth repository.

## 4. Current operating mode

IAOS Foundation and IAC Master Plan v1.0 are established.

IAOS is now in maintenance mode.

This means IAOS should be updated only when:

- a major stage is completed;
- the Active Stage changes;
- a strategic decision is accepted;
- a real workflow repeatedly fails or needs improvement;
- repository evidence contradicts the current IAOS status;
- business direction materially changes.

Do not expand IAOS for documentation completeness.

Do not create documents that do not improve decisions, reduce mistakes, accelerate execution, or support recurring revenue.

## 5. Current business priority

The current Active Stage is:

**Finish Cafe Package v2.0**

The immediate objective is to:

1. review the actual implementation evidence in `tantik/line-business-os`;
2. perform a complete acceptance audit;
3. fix verified defects;
4. confirm functional, security, tenant-isolation, permission, UX, localization, and performance requirements;
5. record founder acceptance;
6. update `docs/IAC_CURRENT_STATUS.md`.

Do not start Platform Standardization, Platform Foundation, a second product, a third product, or broad active sales until the current stage is accepted, unless the founder explicitly changes the Active Stage.

## 6. Starting a work session

Before work:

1. Open the repository that is allowed to be modified.
2. Read its local instructions.
3. Check the current branch.
4. Check `git status`.
5. Identify the exact task.
6. Define scope and non-goals.
7. Identify required source documents.
8. Define validation before implementation.
9. Work in small, reviewable changes.
10. Review all AI-generated changes.
11. Report evidence, not assumptions.

For ORUWA implementation work, begin in:

`D:\Dev\line-business-os`

Read:

- `AGENTS.md`;
- relevant `.cursor/rules/`;
- relevant architecture, security, ADR, plan, and acceptance documents;
- `docs/IAC_REFERENCE.md`.

Read IAOS and OAES only when they are relevant to the task.

## 7. Approval boundaries

Human approval is required before:

- production deployment;
- Cloud database migration;
- destructive SQL;
- deletion of production data;
- billing changes;
- payment operations;
- LINE broadcast or mass communication;
- secrets or credential changes;
- permission or RLS policy changes;
- legal commitments;
- autonomous AI execution of critical actions.

Do not interpret a documentation plan as approval to perform any of these actions.

## 8. Completion rule

A major stage is not complete because:

- code was written;
- tests passed;
- CI is green;
- a preview deployed.

A stage is complete only when:

- scope is fulfilled;
- acceptance criteria are met;
- required verification is complete;
- known risks are reviewed;
- founder approval is recorded;
- relevant documentation is updated;
- `docs/IAC_CURRENT_STATUS.md` is updated.

Only then may the next major stage become Active.