# Learning Progress

> Last Updated: 2026-09-01
> Purpose: 记录当前学习状态、阶段成果、待实践内容和下一步行动。

## Status Definitions

- `待学习`
- `学习中`
- `基础完成`
- `需要实践`
- `需要复习`
- `阶段完成`
- `暂缓`

## 1. Current Focus

CI/CD 总体保持 `学习中`。Python 环境隔离与 CI 依赖安装已完成基础实践；当前先独立推进测试框架目录与多层运行入口重构，验收后再返回 Jenkins 动态调度和完整 CI 闭环。

## 2. Progress Overview

| Topic | Status | Current Level / Evidence | Next Action |
| ----- | ------ | ------------------------ | ----------- |
| RESTful / Swagger / ApiFox Mock | 阶段完成 | 已完成接口基础、文档与 Mock 实践 | 按需复习和应用 |
| Pytest 基础工程化 | 阶段完成 | 完成分层、数据驱动、Fixture、Demo 与报告 | 作为 CI 接入基础 |
| Pytest 生命周期与 Hook | 阶段完成 | 实践 configure、collection、setup/call/teardown、makereport 并验证顺序 | 按需验证复杂多插件场景 |
| Fixture 资源设计 | 阶段完成 | 实践 session 认证和 function Recorder，明确 Fixture/Hook 职责 | 验证 Fixture Plugin 化 |
| Recorder 失败采集 | 阶段完成 | 成功采集 TestID、异常与请求记录 | 降低对固定 Fixture 名称的依赖 |
| pytest 核心对象 | 基础完成 | 能说明 Config、Request、Item、Call、Report 职责并在 Hook 中使用 | 避免无需求深入内部 API |
| 项目内部 Plugin | 基础完成 | Recorder Hook 已从 conftest 拆分并通过 pytest_plugins 加载 | 优化目录与通用接口 |
| pytest11 第三方插件 | 需要实践 | 仅理解 entry point，未打包、安装或发布 | 后续按价值决定是否实践 |
| Allure 报告体系 | 学习中 | 已理解业务化报告、测试证据、失败分类、执行环境、历史趋势及 Jenkins 展示链路 | 接入当前接口自动化框架 |
| Allure 框架接入 | 需要实践 | 尚未将 Listener 数据、环境信息和失败上下文形成完整报告诊断链 | 完成一次真实框架接入 |
| Allure attach | 基础完成 | 用户已确认在真实运行中正常输出 | 在框架重构后验证能力未失效 |
| Git 阶段 1 | 阶段完成 | 完成本地版本、分支、冲突与远程协作 | 为 CI/CD 提供基础 |
| Git 高级使用 | 待学习 | rebase 尚无独立实践 | 后续确认阶段 2 |
| Jenkins 基础 Pipeline | 阶段完成 | 完成 Pipeline、参数化和 Credential 基础实践 | 转入工程化优化 |
| pytest 接入 Jenkins | 阶段完成 | 完成 checkout、依赖安装、pytest 与报告发布 | 稳定入口和环境 |
| Python CI 环境控制 | 基础完成 | Jenkins 已校验 Python 3.14.5、创建 `.venv`、安装 CI 依赖并从虚拟环境运行 pytest | 保持可复现并积累稳定运行证据 |
| Python 依赖管理 | 学习中 | 已有 CI 依赖清单并理解直接/传递依赖职责，场景分层尚未落地 | 基于运行入口实施分层 |
| requirements 场景分层 | 需要实践 | 已完成 API/UI/CI 等方向的设计讨论，无文件与运行验证 | 重构后落地并重建环境验证 |
| pytest CI 稳定执行 | 基础完成 | `INTERNALERROR` 已消失，失败可按普通 assertion failure 和 exit code 1 表达并生成报告 | 继续验证完整失败生命周期 |
| 测试失败生命周期处理 | 学习中 | 已消除当前内部错误，但用户确认完整机制仍在修复 | 完成专项验证 |
| 多层运行入口 | 学习中 | 目标方向已经用户确认，尚无代码和运行证据 | 在框架重构专项实现并验收 |
| 测试框架结构重构 | 学习中 | 已决定转入独立专项，尚无迁移验收证据 | 完成目录迁移与回归验证 |
| Jenkins 动态入口调度 | 待学习 | 等待框架运行接口稳定 | 返回 CI 主线后实施 |
| Groovy Pipeline DSL | 基础完成 | 理解方法、闭包与 Pipeline 嵌套 | 按需复习 |
| CI/CD 总体 | 学习中 | 已有手动 Pipeline 初版，尚无完整自动闭环 | 完成优化、触发和反馈 |
| FastAPI / 服务级 Mock | 待学习 | 已建立独立学习分支 | 后续构建 Mock Server |
| Docker | 待学习 | 暂无实践证据 | CI 稳定后学习 |
| JMeter | 需要实践 | 有参数关联和 Groovy 数据处理实践 | 补充完整性能测试 |
| 数据结构与算法 | 待确认 | 缺少完成度证据 | 确认后设置状态 |

## 3. Completed

- 完成 RESTful → Swagger/OpenAPI → ApiFox Mock、Pytest 基础工程化和 Git 阶段 1。
- 完成 Jenkins 基础 Pipeline、pytest 执行及 JUnit/HTML 报告发布初版链路。
- 通过运行日志验证 Pytest collection、setup、call、teardown 和 report 生命周期。
- 实现并验证 `pytest_configure`、`pytest_collection_modifyitems`、`pytest_runtest_*` 与 `pytest_runtest_makereport`。
- 实践 `hookwrapper`、`tryfirst` 和多 Hook 执行顺序。
- 完成 session 认证 Fixture 与 function Recorder Fixture 设计。
- 通过 `item.funcargs` 获取 Recorder，并在失败时输出 TestID、异常和请求记录。
- 将 Recorder Hook 从 `conftest.py` 拆分为项目内部 Plugin。
- Pytest 高级工程化子阶段通过验收，整体为 `阶段完成`。
- 完成 Allure 基础概念体系学习，建立 pytest 执行 → 测试结果 → Allure 报告 → Jenkins 展示的整体认知。
- 完成 Jenkins 指定 Python 版本校验、workspace 内 `.venv` 创建、CI 依赖安装及虚拟环境内 pytest 执行的基础实践。
- CI 中 pytest 已从框架内部错误恢复为正常测试结果表达，并保持 JUnit/HTML 报告输出。
- Allure attach 已获得实际运行确认。

## 4. In Progress

- 测试框架失败处理生命周期继续修复。
- 测试框架目录与多层运行入口重构。
- Python 依赖管理从单一 requirements 向场景化依赖体系演进。

## 5. Need Practice / Review

### 需要实践

- Fixture 从 `conftest.py` 迁移到 Plugin 并完成加载验证。
- pytest11 第三方插件的打包、安装和发布验证。
- Recorder 与固定 `record_client` Fixture 名称解耦。
- 多 Plugin 目录、通用接口和复杂执行顺序设计。
- Jenkins workspace 完整生命周期和 Webhook 自动触发。
- requirements 场景化分层、重新安装与运行验证。
- Jenkins 对多层运行入口的动态参数调度。
- Credential 私有资源场景、Allure Jenkins 集成与结果反馈。
- 将 Listener 记录的请求、日志和异常作为 Allure 测试证据，并接入执行环境信息。
- 将当前 `TestCase → Service → ApiClient → Listener` 结构映射到业务化报告结构，形成完整失败诊断链。
- Git rebase、真实多人协作和企业分支策略。

### 需要复习

- Hook 的 `tryfirst`、`trylast`、wrapper 和复杂多插件顺序。
- Plugin 目录与多模块组织方式。
- Jenkins Pipeline DSL、生命周期与 Credential 作用域。
- Git 历史模型及 merge/rebase 边界。

## 6. Pending / Deferred

- FastAPI 服务级 Mock、Docker、Git 高级使用：`待学习`。
- pytest11 发布实践：`需要实践`，不作为当前主线阻塞项。
- Pytest Plugin 深入学习：`暂缓`；已有内部 Plugin 基础完成状态不变。
- 动态 Plugin Manager、服务/断言包动态加载、测试数据 DSL、Event Bus 和完整测试平台：`暂缓`。
- Jenkins Agent、插件开发、Kubernetes CI/CD 和 Groovy 高级开发：`暂缓`。

## 7. Current Problems

- 已确定采用多层运行入口并由 Jenkins 动态调度；具体目录、接口和实现仍待框架重构专项验证。
- Recorder Hook 仍依赖固定 Fixture 名称，后续可按实际价值解耦。
- Jenkins 尚无长期稳定运行、自动触发和完整 CI/CD 闭环证据。
- Allure 基础 attach 已验证正常输出；Listener/Recorder 数据、环境信息和失败上下文如何组成完整诊断链仍待实践确认。
- 测试框架失败处理机制仍在完善，尚无完整生命周期验收证据。
- Pytest 高级子阶段无必须解决的阻塞问题。

## 8. Next Actions

### Immediate

1. 在独立专项完成框架目录与多层运行入口重构。
2. 验证重构后的 import、API 测试启动、Plugin、Fixture 和 Allure attach。
3. 根据实际入口完成 requirements 场景化分层，并重新创建环境验证。
4. 返回 CI 主线，让 Jenkins 调用稳定入口并实现动态参数调度。

### After Current Stage

1. 继续 workspace、Webhook、Allure 报告发布和结果反馈闭环。
2. 按价值决定 Fixture Plugin 化、pytest11 和 Recorder 解耦实践。
3. 再确认 Docker、Git 阶段 2 与 FastAPI Mock 的启动时间。

## 9. Recent Updates

- **2026-08-15：** RESTful → Swagger/OpenAPI → Mock 与 Pytest 基础工程化通过验收。
- **2026-08-17：** Git 专项阶段 1 通过验收。
- **2026-08-19：** Jenkins 基础接入子阶段通过验收，CI/CD 总体调整为 `学习中`。
- **2026-08-21：** Pytest 高级工程化子阶段通过验收，完成生命周期、Hook、Recorder 失败采集和内部 Plugin 实践。
- **2026-08-21：** 保留 Jenkins CI/CD 为当前工程主线；材料中的“尚未进入 CI/CD”被判定为过期路线信息，未写入。
- **2026-08-25：** Allure 基础概念体系完成学习，报告体系调整为 `学习中`，并进入真实框架接入实践。
- **2026-08-25：** 当前入口调整为 Pytest 参数管理与 CI 环境控制；Pytest Plugin 深入学习调整为 `暂缓`，不改变内部 Plugin 已有完成状态。
- **2026-09-01：** Python CI 环境控制达到 `基础完成`，真实框架已在 Jenkins 创建的 `.venv` 中执行并正常表达测试结果。
- **2026-09-01：** 运行入口方向明确为多层入口 + Jenkins 动态调度；当前先进入框架目录与入口重构专项，完成后返回 CI 主线。
