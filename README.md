# AI-SOPs

AI-SOPs is a collection of operational playbooks that help a human and an AI agent complete repeatable workflows from a single document.

The goal is simple:

> A person reads the SOP, prepares the required inputs, gives the document to an AI agent, and the AI agent can complete the workflow, verify the result, and tell the person what remains.

## What This Repository Is For

This repo is for workflows where the final result depends on both human preparation and AI execution.

Each SOP should clearly answer:

- What is the workflow trying to achieve?
- What should the human prepare before starting?
- What should the AI agent do step by step?
- What should the AI verify before saying it is done?
- What should the human do after the AI finishes?
- What common failure modes should both sides watch for?

## Repository Structure

```text
AI-SOPs/
  README.md
  docs/
    obsidian-karpathy-llm-wiki-sop.md
  templates/
    ai-sop-template.md
  checklists/
    sop-quality-checklist.md
  examples/
    obsidian-llm-wiki-file-tree.md
```

## Available SOPs

- [Build an Obsidian LLM-Wiki Based on Karpathy's LLM Wiki Idea](docs/obsidian-karpathy-llm-wiki-sop.md)

## SOP Design Principles

1. The document must be executable by an AI agent.
2. Human responsibilities and AI responsibilities must be separated.
3. Every workflow must include verification.
4. The final state must be explicit.
5. The SOP should avoid relying on hidden context.
6. The SOP should include examples, file paths, and expected outputs where possible.

## How To Use

1. Pick the SOP that matches your task.
2. Complete the "Human Preparation" section.
3. Give the SOP to an AI agent.
4. Ask the AI to execute the "AI Execution Plan".
5. Review the "Verification Checklist".
6. Complete the "Human Follow-Up" section.

## How To Add A New SOP

1. Copy [templates/ai-sop-template.md](templates/ai-sop-template.md).
2. Save it under `docs/`.
3. Fill in every section.
4. Run the quality checklist in [checklists/sop-quality-checklist.md](checklists/sop-quality-checklist.md).
5. Add the SOP to this README.

