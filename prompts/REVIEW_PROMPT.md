# Review Prompt

Use this template to review AI, code, or documentation changes.

```text
Review the proposed changes.

Check:
- Scope: Does the change stay within the requested scope?
- Correctness: Does it solve the stated problem?
- Architecture concerns: Does it fit existing architecture and IAOS direction?
- Security: Does it expose secrets, weaken access control, or mishandle sensitive data?
- Duplication: Does it create duplicate logic or duplicate source of truth?
- Documentation: Are necessary docs, workflows, standards, or ADRs updated?
- Validation: Were appropriate tests, checks, builds, or manual reviews run?
- Recommended decision: merge, request changes, or reject.

Prioritize concrete issues with file references where possible.
Mark assumptions and remaining risks.
Do not invent facts.
```
