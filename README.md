# 长篇小说写作助手 V4.4.4

<div align="center">

**Long-form Novel Writing Assistant**

[![Version](https://img.shields.io/badge/version-4.4.4-b8860b)](./novel-writer-V4.4.4.html)
[![Single File](https://img.shields.io/badge/app-single--file_HTML-2f855a)](./index.html)
[![Local First](https://img.shields.io/badge/data-local--first-2563eb)](#数据与隐私)
[![GitHub Pages](https://img.shields.io/badge/demo-GitHub_Pages-181717)](https://nanbo0ne.github.io/novel-writer/)

[在线使用](https://nanbo0ne.github.io/novel-writer/) · [下载独立版](./novel-writer-V4.4.4.html) · [English](#english)

</div>

![长篇小说写作助手界面](docs/screenshot.png)

## 简介

长篇小说写作助手是一款本地优先的单文件 HTML 创作工具。它把项目设定、大纲、分章正文、长期记忆、审稿修改、全文编辑 Agent 和多格式导出集中在一个浏览器页面中，适合持续创作中长篇与超长篇小说。

V4.4.4 是干净的单模式公开版：只保留原始普通写作模式和默认视觉主题，不包含加密载荷，也没有隐藏的替代模式或主题。源码与应用都在同一个 HTML 文件里，可直接阅读、下载和离线运行。

## 核心能力

- **完整创作流程**：项目设定、大纲生成与续写、分章写作、续写、结尾、审稿和导出。
- **任务模型分工**：为全局思维、编辑润色、正文创作、注意事项记忆和 JSON 修复分别选择模型。
- **DeepSeek 思考控制**：支持全局与任务级思考开关，以及 `high` / `max` 思考强度。
- **DeepSeek 生成增强**：可选的全局增强开关会按任务实际路由模型判断，只对 DeepSeek 生成请求生效。
- **虚拟首轮注入**：大纲生成和分章写作可分别配置虚拟用户消息、模型思考与模型回复，默认关闭。
- **长篇连贯性**：章节摘要、长期记忆、章节桥接、剧情关键点和前文上下文协同工作。
- **全文编辑 Agent**：可连续调用读取、搜索和编辑工具直到任务完成；选中的重点片段会持续高亮并显示在侧栏，但不会限制 Agent 按指令处理其他位置。
- **可审阅改稿**：完整诊断显示在对话中，计划按修改位置归并；应用前可直接编辑最终成稿，再逐项确认、跳过、定位和撤销。
- **增强工具兼容**：支持标准 `tool_calls`、旧式 `function_call` 及常见 JSON 工具格式，原始工具代码不会显示在对话中。
- **审稿与修改**：一致性检查、专家意见、去 AI 味、修改前后对比和章节历史快照。
- **本地数据**：项目数据保存在浏览器 IndexedDB，可导入导出 JSON 备份。
- **单文件运行**：无需安装、构建或后端服务，下载 HTML 后即可打开。

## 快速开始

1. 打开[在线版本](https://nanbo0ne.github.io/novel-writer/)，或下载 `novel-writer-V4.4.4.html` 后用浏览器打开。
2. 在“设置”中填写 OpenAI 兼容 API 地址、API Key 和模型名称。
3. 填写书名、类型、世界观、人物设定、章节数和每章目标字数。
4. 生成或导入大纲，然后进入“写作”逐章创作。
5. 使用“编辑”中的 Agent 做选区润色、计划修改和可撤销的全文修订。
6. 定期从“导出”下载项目 JSON 备份和正文文件。

## 模型与接口

应用使用 OpenAI 兼容的 Chat Completions 接口。不同任务可以使用不同 API 配置与模型；未单独指定时会回退到当前基础模型。DeepSeek 模型可额外配置思考模式与思考强度。

API 服务商对模型名称、参数、上下文长度和数据保留政策的支持可能不同，请以服务商文档为准。

## 数据与隐私

- 项目、章节、对话、记忆和设置默认保存在当前浏览器的 IndexedDB 中。
- API Key 保存在浏览器本地，不会被上传到本仓库。
- 只有执行 AI 功能时，对应上下文才会发送到你配置的 API 服务商。
- 更换浏览器、清理网站数据或使用无痕模式可能导致本地项目不可用，请定期导出 JSON 备份。
- V4.4.4 会忽略旧版不兼容的模式数据，不显示或执行它们，也不会主动删除原有本地记录。

## 文件

| 文件 | 用途 |
| --- | --- |
| `index.html` | GitHub Pages 入口 |
| `novel-writer-V4.4.4.html` | 可下载、可离线打开的独立版本 |
| `docs/screenshot.png` | README 界面预览 |

## 作者

伯劳

---

# English

## Overview

Long-form Novel Writing Assistant is a local-first, single-file HTML workspace for planning, drafting, revising, and exporting long-form fiction. Project settings, outlines, chapter drafts, continuity memory, review tools, a full-manuscript editing agent, and exports all live in one browser application.

V4.4.4 is the clean public single-mode edition. It contains only the original writing mode and the default visual theme. There is no encrypted payload and no hidden alternative mode or theme. The readable source and the application are delivered together as one HTML file.

## Highlights

- **End-to-end writing workflow** for projects, outlines, chapters, continuation, endings, reviews, and exports.
- **Task-specific model routing** for global reasoning, editing, chapter writing, memory, and JSON repair.
- **DeepSeek thinking controls** with global and per-task settings plus `high` / `max` effort.
- **DeepSeek generation boost** with an optional global switch that follows the actual routed model and affects only DeepSeek generation requests.
- **Virtual first-turn injection** for outline and chapter generation, with separate virtual user, reasoning, and assistant fields that are disabled by default.
- **Long-form continuity tools** including summaries, persistent memory, chapter bridges, and plot points.
- **Full-manuscript editing agent** that keeps reading, searching, and editing until the task is complete; pinned excerpts remain highlighted in the manuscript and visible in the sidebar without restricting edits elsewhere when the instruction requires them.
- **Reviewable revisions** with full diagnostics in chat, location-based plan cards, editable final replacement text, step skipping, confirmation, history, and undo.
- **Broader tool-call compatibility** for standard `tool_calls`, legacy `function_call`, and common JSON tool envelopes without exposing raw tool code in the conversation.
- **Revision safety** through consistency checks, expert feedback, before/after comparison, and chapter snapshots.
- **Local-first storage** in IndexedDB with JSON project backup and restore.
- **No installation or build step**: download the HTML file and open it in a modern browser.

## Quick Start

1. Open the [live application](https://nanbo0ne.github.io/novel-writer/) or download `novel-writer-V4.4.4.html`.
2. Open Settings and enter an OpenAI-compatible Base URL, API key, and model name.
3. Define the title, genre, world, cast, chapter count, and target chapter length.
4. Generate or import an outline, then draft chapters in the Writing view.
5. Use the Editing Agent for focused rewrites, reviewable plans, and reversible manuscript changes.
6. Export project backups regularly from the Export view.

## Models and APIs

The application uses an OpenAI-compatible Chat Completions endpoint. Each task category can use its own API configuration and model, with the current base model as fallback. DeepSeek models can also use configurable thinking mode and reasoning effort.

Model names, supported parameters, context limits, and data-retention policies depend on your API provider.

## Data and Privacy

- Projects, chapters, chats, memory, and settings are stored locally in browser IndexedDB.
- API keys remain in local browser storage and are not committed to this repository.
- Context is sent only when you invoke an AI-powered action, and only to the API endpoint you configured.
- Clearing site data, switching browsers, or using private browsing can make local projects unavailable. Export JSON backups regularly.
- V4.4.4 ignores incompatible legacy mode data without displaying, executing, or actively deleting the original local records.

## Author

伯劳 (Bolao)
