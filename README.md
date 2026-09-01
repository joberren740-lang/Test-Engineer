# Test Engineer

## Project Purpose

本仓库服务于测试开发学习、工程实践和求职准备，是 Testing Engineer 项目的项目级事实源。GitHub 中的仓库内容是 Codex 与 ChatGPT 共享项目 Context 的统一来源。

## Repository Responsibilities

本仓库负责维护：

- 长期目标与约束
- 学习路线与优先级
- 学习进度与完成证据
- 当前任务状态
- 项目级工程决策
- 独立工程项目索引

## Repository Boundaries

本仓库不保存：

- 完整聊天记录
- 临时 Debug 过程和一次性错误
- Jenkins 临时日志
- 课程全文转写
- 通用技术教程
- Obsidian 最终知识笔记
- BobTest 等独立工程仓库的真实代码

## Structure

```text
Test-Engineer/
├─ AGENTS.md
├─ README.md
├─ context/
│  ├─ 01-Profile-and-Goals.md
│  ├─ 02-Learning-Roadmap.md
│  ├─ 03-Learning-Progress.md
│  └─ 04-Current-Task.md
├─ docs/
│  └─ decisions/
│     └─ README.md
└─ projects/
   └─ README.md
```

## Context Model

- `01-Profile-and-Goals.md`：长期背景、职业目标与稳定约束。
- `02-Learning-Roadmap.md`：学习路线、优先级与已确认决策。
- `03-Learning-Progress.md`：当前学习进度、完成证据与待实践项。
- `04-Current-Task.md`：当前短期任务、待办事项与下一步行动。

## AI Workflow

- Codex 直接读取和维护 Git 仓库中的 Context。
- ChatGPT 通过 GitHub 插件按需读取最新 Context。
- Git 仓库是项目 Context 的唯一事实源。
- 不维护 ChatGPT Project Sources 的重复副本。

## Knowledge Boundary

项目状态与项目级决策保存在 Git；经过整理的最终知识笔记保存在 Obsidian。
