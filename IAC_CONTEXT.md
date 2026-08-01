# IAC Context

Status: Draft
Owner: Konstantin / Izumi IT
Purpose: Give humans and AI a concise first-read view of IAC, IAOS, ORUWA, OAES, and the current execution focus.

## What IAC is

IAC is the entire company and product ecosystem.

It includes:
- the company and its strategy;
- IAOS as the internal operating system;
- ORUWA Business OS as the main reusable multi-tenant SaaS platform;
- OAES as the engineering standard;
- current and future vertical SaaS products;
- product development processes;
- sales and marketing systems;
- market intelligence;
- customer onboarding;
- the future AI Workforce.

## What IAOS is

IAOS is the internal operating system of IAC.

It defines how IAC:
- makes decisions;
- selects and validates products;
- develops software;
- uses AI tools;
- manages knowledge;
- performs reviews and quality control;
- launches products;
- sells and supports products;
- improves its processes.

IAOS is not a SaaS product and is not a replacement for product repositories.

## How the parts differ

- IAC: the full ecosystem.
- IAOS: the company operating system and governance layer.
- ORUWA Business OS: the reusable multi-tenant SaaS platform for Japanese small and medium businesses.
- OAES: the vendor-independent engineering standard and workflow system.
- AI Workforce: a future controlled capability for selected support roles; not a completed production system.

## Current business objective

The primary objective is to build products that can be sold to real Japanese businesses and generate recurring revenue.

The main success measures are:
- first paying customer;
- 3 paying customers;
- 5 paying customers;
- 10 paying customers;
- MRR;
- retention;
- churn;
- ARPU;
- CAC;
- LTV.

## Current execution priority

The documented priority is Stage 1: finish and accept Cafe Package v2.1 Preview Baseline. The founder has accepted the current Preview UI and product scope as the frozen baseline; functional acceptance and performance acceptance are not yet complete. Only confirmed defect, security, data-protection, performance, reliability, localization, and acceptance-documentation changes are permitted until that acceptance is recorded. See [docs/IAC_CURRENT_STATUS.md](docs/IAC_CURRENT_STATUS.md) for live detail.

## Core principles

- Practicality: every task should help launch, help sell, reduce repeated work, or reduce risk.
- Build → Verify → Sell → Improve.
- Architecture for future, implementation for present.
- Product company, not custom-development agency.
- Revenue-weighted prioritization.
- Stage-gated execution with explicit scope, non-goals, acceptance criteria, checks, risks, and founder approval.

## Source-of-truth rules

- This repository is the practical source of truth for IAOS and IAC documentation.
- Chat memory and AI conversation context are supporting context only.
- Product claims, pricing, regulations, and market data must be verified before they are documented as facts.

## Critical constraints

- Prefer one shared multi-tenant SaaS over tenant-specific forks.
- Keep tenant isolation strict, including tenant and location boundaries.
- Preserve roles, permissions, audit logs, and approval gates for sensitive actions.
- Keep Platform Billing separate from Merchant Payments.
- Do not allow autonomous AI changes to permissions, billing, legal documents, or production data.

## What to read next

1. [README.md](README.md)
2. [docs/IAC_MASTER_PLAN.md](docs/IAC_MASTER_PLAN.md)
3. [docs/IAC_CURRENT_STATUS.md](docs/IAC_CURRENT_STATUS.md)
4. [docs/IAC_DECISIONS_INDEX.md](docs/IAC_DECISIONS_INDEX.md)
5. The relevant foundation, workflow, decision, or standard documents in this repository.
