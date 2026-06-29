# IAOS Boot

Status: Draft
Owner: Konstantin / Izumi IT
Purpose: Define what every human or AI session must read before doing IAOS work.

## Read first

Before making changes, read:
- `README.md`
- `IAOS_SPECIFICATION.md`
- `IAOS_BLUEPRINT.md`
- `foundation/CURRENT_STATE.md`
- `foundation/NORTH_STAR.md`
- `foundation/TRANSFORMATION_STRATEGY.md`

Then read only the workflow, standard, decision, or prompt files relevant to the task.

## Current operating mode

IAOS is in Foundation v0.1 Draft mode.

The goal is to create practical working structure for Izumi IT now, not a complete enterprise framework.

## Current business priority

The current priority is LINE Business OS for the Japanese B2B market.

IAOS work should support product execution, AI-assisted development, review, documentation, and decision-making for that priority.

## Continuing work without losing context

When starting a new AI or human session:
1. Read this file first.
2. Read the source files listed above.
3. Check `git status`.
4. Identify the exact task, files, constraints, non-goals, and validation method.
5. Make small, reviewable changes.
6. Update IAOS when the work changes a repeated process or decision.

## Source of truth rule

The GitHub repository is the source of truth.

Chat memory, project memory, IDE context, and AI conversation history are helpful context only. They are not official source of truth unless captured in repository files.
