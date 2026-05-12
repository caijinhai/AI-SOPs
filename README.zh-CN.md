# AI-SOPs

![SOPs](https://img.shields.io/badge/SOPs-agent--ready-2ea44f)
![Docs](https://img.shields.io/badge/docs-human%20%2B%20AI-blue)
![Languages](https://img.shields.io/badge/readme-English%20%7C%20中文-orange)
![Markdown](https://img.shields.io/badge/format-Markdown-black)
![License](https://img.shields.io/badge/license-MIT-5865f2)

> **给人和 AI agent 共同执行的可复用操作流程。**

**1 份可用 SOP | 1 个复用模板 | 1 份质量检查表 | 可交给 agent 执行的 Markdown**

语言：[English](README.md) | **中文**

---

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

## 新增 SOP

从模板开始：

- [SOP 模板](templates/ai-sop-template.md)
- [SOP 质量检查表](checklists/sop-quality-checklist.md)

一份好的 SOP 不应该依赖隐藏聊天上下文。另一个人把它交给另一个 AI agent，也应该能得到稳定结果。
