# AI-SOPs

![SOPs](https://img.shields.io/badge/SOPs-agent--ready-2ea44f)
![Docs](https://img.shields.io/badge/docs-human%20%2B%20AI-blue)
![Bilingual](https://img.shields.io/badge/language-English%20%7C%20中文-orange)
![Markdown](https://img.shields.io/badge/format-Markdown-black)
![License](https://img.shields.io/badge/license-MIT-5865f2)

> **Reusable operating procedures for humans and AI agents.**

**1 production SOP | 1 reusable template | 1 quality checklist | bilingual project guide | agent-executable Markdown**

---

## Language / 语言

[English](#english) | [中文](#中文)

---

## English

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

---

## 中文

**AI-SOPs 是一个把 AI 协作流程沉淀成可复用 SOP 的文档系统。**

它不是单纯保存 prompt，而是把一次跑通的流程整理成完整操作文档：人需要提前准备什么，AI agent 应该怎么执行，做完以后怎么验证，人还需要继续做哪些收尾工作。

这个仓库适合沉淀那些未来还会重复执行的流程：知识库搭建、工具配置、项目环境初始化、GitHub 仓库发布、agent 上手流程、团队操作规范等。

## 为什么需要 AI-SOPs

很多 AI 对话在任务完成后就消失了。AI-SOPs 的目标是把这些成功经验变成长期可复用的操作流程。

每份 SOP 都应该让另一个 AI agent 也能按文档执行，并且边界清楚：

- 人的准备工作
- 必要输入
- AI 执行步骤
- 需要创建的文件和目录
- 验证清单
- 人的后续工作
- 常见失败模式

## 当前 SOP

| SOP | 构建内容 | 状态 |
| --- | --- | --- |
| [Obsidian Karpathy LLM-Wiki SOP](docs/obsidian-karpathy-llm-wiki-sop.md) | 一个由 LLM 维护的 Obsidian 个人 Wiki 知识库 | Ready |

## 快速开始

1. 打开 `docs/` 中的一份 SOP。
2. 先完成 “Human Preparation / 人的准备工作”。
3. 把 SOP 和你的具体输入交给 AI agent。
4. 要求 agent 执行 “AI Execution Plan”。
5. 按验证清单检查结果。
6. 完成人需要继续做的后续工作。

## 仓库结构

```text
AI-SOPs/
  README.md
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

## 新增 SOP

从模板开始：

- [SOP 模板](templates/ai-sop-template.md)
- [SOP 质量检查表](checklists/sop-quality-checklist.md)

一份好的 SOP 不应该依赖隐藏聊天上下文。另一个人把它交给另一个 AI agent，也应该能得到稳定结果。
