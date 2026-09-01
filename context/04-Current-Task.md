# Current Task

Last Updated: 2026-09-01

> Purpose: 本文件仅保存恢复当前工作所需的短期状态，不承担长期路线、长期背景或知识笔记职责。

## Active Task

建立 Testing Engineer 项目的统一 Git Context 仓库，并完成 Codex 与 ChatGPT 的共享上下文工作流。

## Goal

- GitHub 仓库是 Project Context 的唯一事实源。
- Codex 直接读取和维护仓库 Context。
- ChatGPT 通过 GitHub 插件按需读取最新 Context。
- 不再在 Codex 与 ChatGPT Project Sources 之间维护两套同步副本。

## Confirmed Decisions

- `Testing-Engineer` 仓库负责项目 Context、学习/工程决策和独立工程项目索引。
- BobTest 等真实工程代码仓库继续独立维护，不形成 monorepo。
- GitHub 是 Context 的唯一事实源。
- ChatGPT Work 临时工作目录不作为持久 Git workspace。
- GitHub 插件已经验证能读取仓库最新提交。
- `01-Profile-and-Goals.md`、`02-Learning-Roadmap.md`、`03-Learning-Progress.md` 已完成审查和迁移。

## Current Repository Structure

```text
Testing-Engineer/
├── AGENTS.md
├── README.md
├── context/
│   ├── 01-Profile-and-Goals.md
│   ├── 02-Learning-Roadmap.md
│   ├── 03-Learning-Progress.md
│   └── 04-Current-Task.md
├── docs/
│   └── decisions/
└── projects/
```

## Open Items

- 完成正式 `AGENTS.md`。
- 完成根目录 `README.md`。
- 建立 `projects/README.md`。
- 确定 `docs/decisions/` 使用规则。
- 验证正式 Context 文件的 GitHub → ChatGPT 读取。
- 验证完成后删除测试文件 `context-learn.md`。
- 确认旧 ChatGPT Project Sources 的退出方式。

## Next Action

设计并完成正式 `AGENTS.md`。
