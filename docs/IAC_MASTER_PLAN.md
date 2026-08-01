# IAC Master Plan

Status: Accepted v1.0
Owner: Konstantin / Izumi IT
Last updated: 2026-08-01
Purpose: The main operating document of IAC. It exists to help humans and AI make faster, better decisions about what to build, review, sell, and prioritize. It is not a handbook, not a vision document, and not theory.

## Executive Summary

IAC is the company and product ecosystem building SaaS products for Japanese B2B businesses, on top of ORUWA Business OS. IAOS exists because IAC is founder-led and AI-assisted: without a shared operating system, decisions repeat, mistakes repeat, and AI-assisted work loses context between sessions. The current company priority is a single Active Stage — finish Cafe Package v2.0 and get it accepted — with everything else Planned or Backlog.

Use this document to check three things before starting significant work: what the current Active Stage is, whether the task belongs to it, and whether it should proceed, wait for a later stage, or go to backlog.

## 1. Why IAC Exists

IAC exists to build SaaS products that Japanese small and medium businesses will pay for and keep paying for. A single founder cannot run every business process by hand at scale, so IAC depends on software and AI-assisted workflows to build, review, and ship reliably. Documentation and architecture are not the goal — revenue from real, retained customers is. IAOS exists to make that repeatable: it keeps decisions, standards, and workflows in one place so they survive tool changes, AI provider changes, and session resets. When IAOS work stops helping IAC build, sell, or avoid repeated mistakes, it should stop.

## 2. Purpose of This Document

This document answers three questions for any IAC task:
- What is the current Active Stage, and does this task belong to it?
- What is the next Stage after that, and should this task wait for it?
- Does this task increase customer value, revenue, or reduce future work?

If a task does not help answer these questions better, it does not belong in this document.

## 3. Current State

Active Stage: **Finish Cafe Package v2.0** (see [docs/IAC_CURRENT_STATUS.md](IAC_CURRENT_STATUS.md) for the live operational detail).

Verified in this repository:
- IAOS foundation, accepted ADRs ([decisions/](../decisions/)), workflows, standards, and prompts exist and are in active use.
- The IAC documentation package (this file, [IAC_CONTEXT.md](../IAC_CONTEXT.md), [IAC_CURRENT_STATUS.md](IAC_CURRENT_STATUS.md), [IAC_DECISIONS_INDEX.md](IAC_DECISIONS_INDEX.md)) exists and is accepted.

Not yet verified in this repository:
- Cafe Package v2.0 founder acceptance.
- A completed market-intelligence cycle.
- Cafe Product Review outputs.

Status facts belong in [docs/IAC_CURRENT_STATUS.md](IAC_CURRENT_STATUS.md), which is the single source of truth for what is currently true. This Master Plan does not duplicate that detail — it defines the stages, principles, and decisions that status is measured against.

## 4. Vision

IAC becomes a product company that builds, sells, and scales multiple SaaS products for the Japanese B2B market, run on a shared platform (ORUWA Business OS) and a shared engineering standard (OAES), with durable knowledge that survives individual tools, AI providers, and sessions (IAOS).

The full long-term framing lives in [foundation/NORTH_STAR.md](../foundation/NORTH_STAR.md). The vision matters here only to the extent it disciplines near-term choices: build for reuse, don't build for a future that isn't funded yet.

## 5. Success Targets

Success is a sequence of stage outcomes, not a calendar date:

```
Cafe Package accepted
   ↓
Platform Foundation ready
   ↓
Three sellable products
   ↓
Sales Ready
   ↓
First Paying Customer
   ↓
Scale
```

Each arrow is a gate: the next outcome is not pursued until the current one is real and verified, per [Section 17](#17-definition-of-success).

## 6. IAC Ecosystem

- **IAC** — the full company and product ecosystem: strategy, products, sales, marketing, market intelligence, onboarding, and the future AI Workforce.
- **IAOS** — the internal operating system: how IAC decides, builds, reviews, and documents. Not a product, not a product repository.
- **ORUWA Business OS** — the reusable multi-tenant SaaS platform for Japanese SMBs. The foundation every vertical product is built on.
- **OAES** — the vendor-independent engineering standard and workflow system. Separate from the AI Workforce.
- **AI Workforce** — a future, controlled capability for selected support roles (research, QA, review, sales prep). Not a completed system; not to be designed ahead of product and sales evidence.

Full context: [IAC_CONTEXT.md](../IAC_CONTEXT.md).

## 7. Core Principles

- **Money drives progress.** Work that does not lead toward revenue, directly or by removing a blocker to revenue, is lower priority than work that does.
- **Build → Verify → Sell → Improve.** Nothing is "done" until it is verified; nothing is verified until it is sold and used.
- **Practical now, scalable later.** Solve the problem in front of us with the simplest working design; keep the door open for scale, don't build the scaled version first.
- **Customer value before engineering elegance.** A less elegant solution that ships and helps a customer beats an elegant one that doesn't.
- **No theory for theory's sake.** If a document, framework, or process doesn't change a decision, it shouldn't exist.
- **Single source of truth.** Every concept lives in exactly one place; everything else links to it.
- **Small reviewable iterations.** Prefer many small changes over one large one.
- **Review before merge.** No exceptions for AI-generated work — a human reviews before it ships.
- **Architecture for future. Implementation for present.** Design so today's shortcut doesn't block tomorrow's scale, but implement only what today's stage needs.
- **Ideas are never deleted. Only reprioritized.** See [Section 13](#13-backlog-philosophy).
- **Never redesign working architecture without measurable business value.** A working system is not a bug to be fixed by curiosity.
- **Documents exist to help decisions.** If a document does not help make a better decision, reduce a mistake, accelerate development, or increase future revenue, it should not exist.
- **80/20 rule.** Prefer the small amount of work that produces the greatest customer or business value. Before starting significant work, ask: will this meaningfully help us launch, sell, or reduce future work? If not, consider postponing it.
- **Validate before optimizing.** Never optimize before validation. Prove customer value first with real usage; optimize only after that proof exists.

## 8. Decision Matrix

Before starting any significant task, answer:

1. Does this increase customer value?
2. Does this help revenue?
3. Does this reduce future work?
4. Can it be reused (across products, tenants, or teams)?
5. Can it wait?
6. Is this today's bottleneck?

A task that scores well on 1–4 but fails 5/6 (it can wait, and isn't the bottleneck) belongs in the backlog, not the Active Stage. See [Section 13](#13-backlog-philosophy).

## 9. Product Portfolio

- **ORUWA Business OS** — the shared multi-tenant platform. One shared SaaS architecture, not tenant-specific forks. Platform Billing (tenant → IAC) is kept strictly separate from Merchant Payments (business → its own customers).
- **Cafe Package** — the first vertical product, currently in v2.0 completion. Proves the platform before anything is generalized from it.
- **Future verticals** — selected only through the product-selection process in [Section 12](#12-current-priorities) / Stage 6, based on current Japanese-market research, not assumption.

### UI foundation decision (adopted)

The official UI foundation for IAC products is **shadcn/ui + shadcn Blocks**, extended into ORUWA UI. TailAdmin and similar admin-template projects are inspiration only — they are not to be adopted wholesale or used to justify replacing ORUWA UI.

## 10. Current Roadmap

There is exactly one **Active** Stage at any time. Everything else is **Planned** or **Backlog**.

```
ACTIVE
Finish Cafe Package v2.0
   ↓
Cafe Product Review
   ↓
Platform Standardization
   ↓
Platform Foundation
   ↓
Second Product
   ↓
Third Product
   ↓
Sales Readiness
   ↓
Active Sales
```

## 11. Stage Definitions

Every stage follows [Section 17](#17-definition-of-success) before it can move from Active to Completed.

**Finish Cafe Package v2.0** (Active) — functional, permission, tenant-isolation, UX, and localization review completed; known bugs reviewed; founder acceptance recorded.

**Cafe Product Review** (mandatory, Planned) — must include:
- internal review of strengths and weaknesses;
- competitor research, including the Japanese market and relevant foreign competitors;
- feature evaluation and cost vs. value for each candidate feature;
- classification of ideas into Cafe 2.1, Cafe 3.0, or future backlog.

**Platform Standardization** (mandatory, Planned) — extracts only what Cafe Package proved works, before Platform Foundation starts:
- shared UI, shared workflows, shared configuration;
- branding, permissions, tenant configuration, localization;
- module contracts.

Changes stay limited to the proven core. This is not a rewrite.

**Platform Foundation** (Planned) — organization, customer portal, platform billing, entitlements, and subscription state, with Platform Billing kept separate from Merchant Payments. Its goal is to reduce onboarding time, maximize reuse across products, support multiple products on one platform, and avoid duplicated implementation. Nothing more.

**Second Product / Third Product** (Planned) — selected via the product-selection process (Stage 6 of the prior roadmap version): 10–15 candidate Japanese-market verticals evaluated on problem severity, willingness to pay, market access, competition, dev time, ORUWA reuse, LINE fit, AI fit, onboarding complexity, support burden, retention, expansion revenue, and path to first 10 customers.

**Sales Readiness** (Planned) — see [Section 15](#15-sales-strategy).

**Active Sales** (Planned) — begins once portfolio, billing, onboarding, website, and basic sales operations can support real customers.

## 12. Current Priorities

**Critical now**
- Complete Cafe Package v2.0 and record founder acceptance.
- Keep Platform Billing separate from Merchant Payments in any related work.
- Preserve tenant isolation and approval gates in any related work.

**Important next**
- Cafe Product Review, once Cafe Package v2.0 is accepted.
- Platform Standardization, limited to what Cafe Package proved.

**Later**
- Platform Foundation, second and third products, sales readiness.

**Explicitly deferred**
- Speculative enterprise architecture.
- Large platform rewrites before reuse is proven.
- AI Workforce design before product and sales evidence exists.

## 13. Backlog Philosophy

Ideas are never deleted. They are reprioritized.

An idea that isn't right for the Active Stage goes to the backlog, not the trash. It stays there, tagged with which future stage it belongs to (Cafe 2.1, Cafe 3.0, Platform Foundation, etc.), until the Decision Matrix says its time has come. This protects good ideas from being lost, and protects the Active Stage from scope creep.

## 14. Market Intelligence Process

Runs approximately every two months. Each cycle reviews:
- Japanese market changes and new vertical opportunities;
- competitors and their features and pricing;
- LINE platform changes and payment-provider changes;
- relevant AI capabilities;
- relevant regulation, subsidies, and support programs;
- customer behavior changes.

Each cycle ends with: findings → implications → roadmap changes or an explicit no-change decision → next action. A cycle that produces no decision is a wasted cycle.

## 15. Sales Strategy

Before Active Sales, Sales Readiness prepares: product website, positioning, product pages, demos, pricing hypotheses backed by research, lead capture, CRM, proposals, demo scripts, onboarding, customer portal, subscription/billing visibility, and customer-support workflow.

### Website decision (adopted)

The marketing website is built from **quality blocks + custom UX + custom Japanese copywriting + ORUWA branding + real screenshots and demos**. It is not built from scratch, and it is not a template published with only cosmetic changes. The blocks provide speed; the UX, copy, branding, and real product evidence provide credibility with Japanese B2B buyers.

## 16. Risks

- Product work outruns validation (documentation or roadmap moves ahead of real evidence).
- Infrastructure, onboarding, or billing complexity grows before reuse is proven.
- Market research becomes performative — cycles run without producing decisions.
- Product expansion starts before product-market fit is proven.
- Ungoverned AI use creates security, compliance, or customer-trust risk.

## 17. Definition of Success

Every Stage must define, before it can be marked Completed:

- **Scope** — what this stage covers.
- **Non-goals** — what it explicitly does not cover.
- **Acceptance criteria** — the conditions that must be true.
- **Verification** — how those conditions were checked.
- **Known risks** — what could still go wrong.
- **Founder approval** — recorded, not assumed.
- **Documentation update** — the relevant IAOS/IAC documents reflect the outcome.
- **Current Status update** — [docs/IAC_CURRENT_STATUS.md](IAC_CURRENT_STATUS.md) reflects the outcome.

Only then: **Completed.**

## 18. Next Action

Complete the Stage 1 acceptance review for Cafe Package v2.0 (functional, permission, tenant-isolation, UX, localization) and record the outcome — accepted or not — in [docs/IAC_CURRENT_STATUS.md](IAC_CURRENT_STATUS.md).

## Revision History

| Version | Status | Date | Summary |
| --- | --- | --- | --- |
| v0.1 | Draft | 2026-08-01 | Initial structured master plan created from IAOS foundation documents. |
| v1.0 | Accepted | 2026-08-01 | Added Executive Summary, Why IAC Exists, Success Targets, 80/20 and validate-before-optimize principles, Platform Foundation goal, Revision History. Renumbered sections to fit; no change to Roadmap, Decision Matrix, Core Principles content, Backlog Philosophy, Stage Definitions, UI Decision, or Website Decision. |
