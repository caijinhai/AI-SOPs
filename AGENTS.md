# AI-SOPs Maintenance Rules

This repository stores SOPs for workflows executed by humans and AI agents together.

## Writing Rules

1. Every SOP must separate human preparation from AI execution.
2. Every SOP must include verification steps.
3. Every SOP must include human follow-up work.
4. Every SOP must be reusable without hidden chat history.
5. Prefer concrete paths, commands, file trees, and expected outputs.
6. Avoid vague instructions such as "set things up properly" without defining the final state.

## Repository Conventions

- Put full SOPs in `docs/`.
- Put reusable formats in `templates/`.
- Put checklists in `checklists/`.
- Put concrete examples in `examples/`.

## Before Finishing Changes

Check:

- The README links to new SOPs.
- The SOP quality checklist still applies.
- File names are lowercase with hyphens when possible.
- The SOP can be handed to another AI agent as-is.

