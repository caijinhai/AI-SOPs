# AI-SOPs

![SOPs](https://img.shields.io/badge/SOPs-agent--ready-2ea44f)
![Docs](https://img.shields.io/badge/docs-human%20%2B%20AI-blue)
![Languages](https://img.shields.io/badge/readme-English%20%7C%20中文-orange)
![Markdown](https://img.shields.io/badge/format-Markdown-black)
![License](https://img.shields.io/badge/license-MIT-5865f2)

> **Reusable operating procedures for humans and AI agents.**

**1 production SOP | 1 reusable template | 1 quality checklist | agent-executable Markdown**

Language: **English** | [中文](README.zh-CN.md)

---

**AI-SOPs is a practical SOP system for turning successful AI-assisted workflows into reusable, executable documents.**

Not just prompts. A complete SOP tells the human what to prepare, tells the AI agent what to do, defines how the result should be verified, and explains what the human should do after the AI finishes.

This repository is designed for workflows that should be repeated reliably: setting up knowledge systems, configuring tools, building project environments, publishing repositories, onboarding agents, and documenting operational processes.

## Why AI-SOPs

Most AI conversations disappear after the task is done. AI-SOPs turns the best parts of those conversations into durable procedures.

Each SOP is written so another AI agent can pick it up later and execute it with clear boundaries:

- Human preparation
- Required inputs
- AI execution plan
- Files and directories to create
- Verification checklist
- Human follow-up
- Common failure modes

## Available SOPs

| SOP | What It Builds | Status |
| --- | --- | --- |
| [Obsidian Karpathy LLM-Wiki SOP](docs/obsidian-karpathy-llm-wiki-sop.md) | An Obsidian vault structured as an LLM-maintained personal wiki | Ready |

## Quick Start

1. Open an SOP in `docs/`.
2. Complete the "Human Preparation" section.
3. Give the SOP and your project-specific inputs to an AI agent.
4. Ask the agent to execute the "AI Execution Plan".
5. Review the verification checklist before accepting the result.
6. Complete the human follow-up section.

## Repository Map

```text
AI-SOPs/
  README.md
  README.zh-CN.md
  AGENTS.md
  docs/
    obsidian-karpathy-llm-wiki-sop.md
  templates/
    ai-sop-template.md
  checklists/
    sop-quality-checklist.md
  examples/
    obsidian-llm-wiki-file-tree.md
```

## Write A New SOP

Start from the reusable template:

- [SOP template](templates/ai-sop-template.md)
- [SOP quality checklist](checklists/sop-quality-checklist.md)

A good SOP should be executable without hidden chat history. If another person can hand it to another AI agent and get the same result, it is doing its job.
