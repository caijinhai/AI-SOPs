# AI-SOPs

**English** | [中文](#中文)

AI-SOPs is a practical playbook repository for turning repeatable work into clear, executable SOPs for humans and AI agents.

The core idea:

> A human prepares the context and makes key decisions.
> An AI agent follows the SOP, builds the workflow, verifies the result, and reports what remains.

This repository is for workflows that should be done reliably more than once, especially workflows where the handoff between a person and an AI agent needs to be precise.

## Why This Exists

Most AI prompts describe what the user wants right now. A good SOP describes how the work should be done every time.

AI-SOPs helps convert one successful workflow into a reusable document that another AI agent can execute later with less ambiguity.

Each SOP answers:

- What is the final outcome?
- What should the human prepare first?
- What inputs should be given to the AI agent?
- What steps should the AI execute?
- How should the AI verify the result?
- What should the human do after the AI finishes?
- What can go wrong, and how should it be fixed?

## Repository Structure

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

## Available SOPs

- [Build an Obsidian LLM-Wiki Based on Karpathy's LLM Wiki Idea](docs/obsidian-karpathy-llm-wiki-sop.md)

## How To Use

1. Choose an SOP from `docs/`.
2. Complete the "Human Preparation" section.
3. Give the SOP and your inputs to an AI agent.
4. Ask the AI agent to execute the "AI Execution Plan".
5. Review the verification checklist.
6. Complete the human follow-up work.

## How To Write A New SOP

1. Copy [templates/ai-sop-template.md](templates/ai-sop-template.md).
2. Save the new SOP under `docs/`.
3. Fill in every section.
4. Check it with [checklists/sop-quality-checklist.md](checklists/sop-quality-checklist.md).
5. Add it to the "Available SOPs" section.

## SOP Principles

- Make the final state explicit.
- Separate human responsibilities from AI responsibilities.
- Include concrete file paths, commands, examples, and expected outputs.
- Include verification before completion.
- Avoid hidden chat history or unstated assumptions.
- Make the document reusable by another person and another AI agent.

---

## 中文

AI-SOPs 是一个面向人与 AI agent 协作的 SOP 文档仓库。

它的目标不是保存一次性的 prompt，而是把一套已经跑通的流程沉淀成可复用、可执行、可验证的操作文档。

核心思路：

> 人负责准备上下文、做关键决策、验收结果。
> AI agent 按照 SOP 执行流程、构建环境、完成验证、说明剩余工作。

如果一个任务未来还会重复做，或者你希望另一个 AI agent 也能按同样标准完成它，就适合把它写成这里的 SOP。

## 这个仓库解决什么问题

普通 prompt 往往只描述“我现在想要什么”。
好的 SOP 会描述“这类事情每次应该怎么做”。

每份 SOP 都应该说清楚：

- 最终要得到什么？
- 人在开始前要准备什么？
- 需要给 AI agent 哪些输入？
- AI agent 应该按什么步骤执行？
- AI agent 做完后如何验证？
- 人在 AI 完成后还要继续做什么？
- 常见错误是什么，怎么发现和修复？

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

## 当前 SOP

- [基于 Karpathy LLM Wiki 思路搭建 Obsidian LLM-Wiki](docs/obsidian-karpathy-llm-wiki-sop.md)

## 如何使用

1. 从 `docs/` 里选择一份 SOP。
2. 先完成其中的“Human Preparation / 人的准备工作”。
3. 把 SOP 和你的具体输入交给 AI agent。
4. 要求 AI agent 执行 “AI Execution Plan”。
5. 根据验证清单检查结果。
6. 完成 SOP 里列出的后续人工工作。

## 如何新增一份 SOP

1. 复制 [templates/ai-sop-template.md](templates/ai-sop-template.md)。
2. 把新文件放到 `docs/`。
3. 填完整所有章节。
4. 用 [checklists/sop-quality-checklist.md](checklists/sop-quality-checklist.md) 检查质量。
5. 在 README 的“当前 SOP”里添加链接。

## 好 SOP 的标准

- 最终状态清楚。
- 人做什么、AI 做什么分得清楚。
- 有路径、命令、示例和预期输出。
- 有验证步骤，而不是“做完就算”。
- 不依赖隐藏聊天上下文。
- 另一个人和另一个 AI agent 也能复用。
