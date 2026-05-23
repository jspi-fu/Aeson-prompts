---
title: Reliable Coding Agent
slug: reliable-coding-agent
summary: 增强 AI 编程代理稳定性的扩展提示词系统
description: Reliable Coding Agent 是一套增强 AI 编程代理原有能力的扩展提示词，通过融入优秀人类工程师的思维方式和工作流程，实现更稳定、可靠的编码水平，目前支持 Claude Code、Codex CLI 和 Gemini CLI。
---

> **注意**：在 Gemini CLI + Gemini 3 Pro 上，这套提示词的指令遵循效果有问题，待优化改进。

本项目是一套增强 AI 编程代理原有能力的扩展提示词，目前主要针对 `Claude Code` 和 `Codex CLI` 进行了优化和测试。

在不影响 AI 编程代理原有能力的前提下，为其融入优秀人类工程师的思维方式和工作流程，以实现**更稳定、更可靠**的编码水平。

## 使用方法

> 由于可能与其他原有设定冲突，建议直接替换文件。

### Claude Code

将 [ClaudeCode.md](ClaudeCode.md) 的内容复制到 Claude Code 的全局 `CLAUDE.md` 中即可。

**典型路径**：

| 系统 | 路径 |
|------|------|
| Mac | `~/.claude/CLAUDE.md` |
| Windows | `C:\users\你的用户名\.claude\CLAUDE.md` |

### Codex

将 [Codex.md](Codex.md) 的内容复制到 Codex 的全局 `AGENTS.md` 中即可。

**典型路径**：

| 系统 | 路径 |
|------|------|
| Mac | `~/.codex/AGENTS.md` |
| Windows | `C:\users\你的用户名\.codex\AGENTS.md` |

### Gemini CLI

将 [GeminiCli.md](GeminiCli.md) 的内容复制到 Gemini CLI 的全局 `GEMINI.md` 中即可。

**典型路径**：

| 系统 | 路径 |
|------|------|
| Mac | `~/.gemini/GEMINI.md` |
| Windows | `C:\users\你的用户名\.gemini\GEMINI.md` |

### Cursor

由于 Cursor 已经支持识别项目目录中的 `AGENTS.md` 或 `CLAUDE.md`，因此可以参照 Claude Code 或 Codex 的方法直接使用。

## 核心优势

### 非侵入式的增强

不影响系统提示词的原有逻辑，仅进行补充增强，最大程度发挥模型和代理本身的能力。

### 复杂项目的提效

通过自动维护必要的文档和记忆，来节省重复分析代码架构、反复修改的时间和 Token，让 Coding Agent 基于对文档的理解去更有效、更有针对性的进行编码工作。

### 可靠的编程结果

通过三段式增强来达成更可靠的编程结果：

1. **基础的代码质量要求**
2. **优化对于复杂任务的处理思路和阶段拆分**
3. 基于**测试**、**记忆**、**文档**（TMD）的编码稳定性闭环
