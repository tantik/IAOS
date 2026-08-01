# IAOS Boot

Status: Draft
Owner: Konstantin / Izumi IT
Purpose: Define what every human or AI session must read before doing IAOS or IAC work.

## Read first

Before making changes, read:
- [README.md](README.md)
- [IAC_CONTEXT.md](IAC_CONTEXT.md)
- [docs/IAC_CURRENT_STATUS.md](docs/IAC_CURRENT_STATUS.md)

Then read only the workflow, standard, decision, or prompt files relevant to the task.

## Current operating mode

IAOS is in Foundation v0.1 Draft mode, and the IAC documentation package is being established as a practical operating layer for the wider ecosystem.

The goal is to create a practical working structure for IAC now, not a complete enterprise framework.

## Current business priority

The current documented priority is to complete Cafe Package v2.0 and verify it before expanding into the next major stage.

IAOS and IAC work should support product execution, AI-assisted development, review, documentation, and decision-making for that priority.

## Continuing work without losing context

When starting a new AI or human session:
1. Read this file first.
2. Read the source files listed above.
3. Check `git status`.
4. Inspect the current branch.
5. Confirm the exact task, constraints, non-goals, and validation method.
6. Work in small, reviewable changes.
7. Verify before reporting completion.
8. Do not trust chat memory over repository evidence.

## Source of truth rule

The GitHub repository is the source of truth.

Chat memory, project memory, IDE context, and AI conversation history are helpful context only. They are not official source of truth unless captured in repository files.
