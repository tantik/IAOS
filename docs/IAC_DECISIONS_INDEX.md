# IAC Decisions Index

Status: Draft
Owner: Konstantin / Izumi IT
Purpose: Provide a concise index of important IAC and IAOS decisions without duplicating full ADR content.

## Decision index

| Decision | Status | Summary | Source | Date | New ADR needed? |
| --- | --- | --- | --- | --- | --- |
| IAC is the full ecosystem | Adopted in current documentation | IAC includes the company, IAOS, ORUWA Business OS, OAES, products, processes, sales, marketing, onboarding, and the future AI Workforce. | [IAC_CONTEXT.md](../IAC_CONTEXT.md) | Not recorded | ADR required |
| IAOS is the internal operating system of IAC | Accepted | IAOS defines how IAC makes decisions, develops products, uses AI, manages knowledge, reviews work, and improves operations. | [decisions/ADR-0001-iaos-as-company-operating-system.md](../decisions/ADR-0001-iaos-as-company-operating-system.md) | Not recorded | No |
| ORUWA Business OS is the reusable multi-tenant SaaS platform | Adopted in current documentation | ORUWA Business OS is the main reusable platform for Japanese SMBs and the foundation for vertical SaaS products. | [IAC_CONTEXT.md](../IAC_CONTEXT.md) | Not recorded | ADR required |
| OAES is the engineering standard | Adopted in current documentation | OAES is vendor-independent, workflow- and governance-oriented, and separate from the future AI Workforce. | [IAC_CONTEXT.md](../IAC_CONTEXT.md) | Not recorded | ADR required |
| AI Workforce is separate from OAES | Adopted in current documentation | AI Workforce is a future controlled capability for selected support roles, not an engineering standard or application platform. | [IAC_CONTEXT.md](../IAC_CONTEXT.md) | Not recorded | ADR required |
| One shared multi-tenant SaaS | Adopted in current documentation | The platform approach favors one shared multi-tenant SaaS architecture over tenant-specific forks. | [docs/IAC_MASTER_PLAN.md](IAC_MASTER_PLAN.md) | Not recorded | ADR required |
| Tenant-specific forks are prohibited | Adopted in current documentation | Customization should happen through configuration, reusable modules, or controlled experiments rather than forked products. | [docs/IAC_MASTER_PLAN.md](IAC_MASTER_PLAN.md) | Not recorded | ADR required |
| Platform Billing is separate from Merchant Payments | Adopted in current documentation | Platform Billing covers tenant payments to IAC; Merchant Payments cover end-customer payments to the business. | [docs/IAC_MASTER_PLAN.md](IAC_MASTER_PLAN.md) | Not recorded | ADR required |
| Human approval is required for critical AI actions | Adopted in current documentation | Critical actions such as billing, permissions, legal commitments, and destructive data changes must remain human-approved. | [docs/IAC_MASTER_PLAN.md](IAC_MASTER_PLAN.md) | Not recorded | ADR required |
| Three-product target before broad active sales | Adopted in current documentation | The company should aim for a portfolio that can support real sales before broad active outreach. | [docs/IAC_MASTER_PLAN.md](IAC_MASTER_PLAN.md) | Not recorded | ADR required |
| Fast tenant onboarding is a strategic target | Adopted in current documentation | Standard onboarding should be reduced where realistically possible through reusable configuration and clear module boundaries. | [docs/IAC_MASTER_PLAN.md](IAC_MASTER_PLAN.md) | Not recorded | ADR required |
| Stage-gated execution | Accepted | Major stages should only proceed after scope, checks, risks, and founder approval are clear. | [docs/IAC_MASTER_PLAN.md](IAC_MASTER_PLAN.md) | Not recorded | ADR required |
| Recurring market and competitor research | Adopted in current documentation | Research should happen approximately every two months and should drive roadmap decisions. | [docs/IAC_MASTER_PLAN.md](IAC_MASTER_PLAN.md) | Not recorded | ADR required |

## Notes

This index is intentionally concise. Full rationale should remain in the relevant ADRs or in the master plan when no formal ADR exists yet.
