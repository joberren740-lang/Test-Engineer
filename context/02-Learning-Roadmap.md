# Learning Roadmap

> Last Updated: 2026-09-22
> Purpose: 记录测试开发学习路线、阶段目标、优先级和重要决策。

## 1. Current Strategy

- 接口测试基础、Pytest 工程化和 Git 阶段 1 已完成；求职前能力链目标为 `requests + Selenium + Appium + Pytest`。
- Pytest 高级工程化子阶段已完成生命周期、Hook、核心对象和项目内部 Plugin 实践；当前只保留 CI 所需的执行、参数、结果采集和报告能力，Plugin 深入开发暂缓。
- 后续 Jenkins CI/CD 工程实践以 IndianTest 作为真实自动化测试框架；独立 Demo 仅用于 Jenkins/Groovy 语法实验。
- IndianTest 1.0.0 已完成，CI/CD 学习恢复，并以该真实项目继续 Pipeline 工程化实践。
- Appium 基础学习继续推进；当前教程练习统一在独立的 AppiumDemo 项目中完成。
- Appium 采用分阶段递进学习：每个小阶段完成讲解、练习与验收，并经用户确认掌握后再进入下一阶段。
- 当前 Appium专项聊天只学习 Appium本身的功能、命令与运行机制；UI自动化框架构建、Pytest集成和工程分层由独立侧边聊天承担。
- Groovy 只学习理解 Jenkins Pipeline DSL 所需内容，不发展为长期技术方向。
- Git 阶段 2 暂不抢占 CI/CD 主线；FastAPI 服务级 Mock 保持独立扩展分支。

## 2. Learning Stages

### Stage 1 — Foundation

- RESTful → Swagger/OpenAPI → ApiFox Mock：`阶段完成`。

### Stage 2 — Test Development Core

- Pytest 基础工程化：`阶段完成`，包括框架分层、数据驱动、Fixture、Schema 校验、Demo 与报告。
- Pytest 高级工程化：`阶段完成`，包括生命周期、Fixture 资源设计、Hook、Recorder 失败采集与内部 Plugin 化。
- Plugin 能力边界：项目内部 Plugin 为 `基础完成`；pytest11 第三方插件发布仍需实践。
- Allure 测试报告体系：`学习中`，已建立报告业务化、测试证据、失败分类、执行环境和趋势展示的基础认知，尚需接入当前接口自动化框架。

### Stage 3 — Engineering

- Git 阶段 1：`阶段完成`。
- Jenkins 基础 Pipeline 与 pytest 初次接入：`阶段完成`。
- CI/CD 总体：`学习中`，基于 IndianTest 1.0.0 恢复真实项目 Pipeline 工程化优化。
- Docker 在基础流水线形成后推进。

### Stage 4 — Project Practice

- 推进 IndianTest 1.0，并在其上线后承接 CI/CD 工程实践。
- AppiumDemo 定位为当前 Appium 专项学习项目，集中承载教程练习、配置和运行验证。
- BobTest 计划在 Appium 学习完成后演进为传统 UI 自动化框架：保留底层能力、Pages、插件和测试代码，移除 API 部分并接入 Appium。
- ApiClient 插件化重构作为独立项目实践分支，不打断 Pytest 知识主线。
- 使用 FastAPI 构建可控 Mock 服务并接入测试框架。

### Stage 5 — Interview Preparation

- 根据目标岗位补齐测试理论、项目表达、常见面试题与适量数据结构算法。
- 具体启动时间待确认。

## 3. Current Priorities

### P0 — Highest Priority

1. 将 IndianTest 1.0.0 接入 Jenkins，并完成 Python 解释器检测与版本约束。
2. 让 Jenkins 通过统一 `run.py` 入口稳定执行真实测试框架。
3. 完成自动触发、报告发布与结果反馈闭环。

### P1 — Important

1. 完成 IndianTest 1.0 上线。
2. 在 AppiumDemo 中完成 Appium 配套练习并保留可运行证据。
3. IndianTest 1.0 上线后恢复 CI/CD 学习与工程化实践。

### P2 — Later

1. Docker 基础与测试环境容器化。
2. Git 阶段 2 与数据结构算法求职向复习。
3. pytest11 发布、动态插件系统和测试平台能力按岗位需求补充。

## 4. Technology Map

### Git

- 阶段 1 已完成：本地版本管理、feature 分支、merge/conflict、remote 及远程协作。
- 阶段 2 候选范围包括 rebase、高级提交管理和团队协作规范。

### Python / Pytest

- 已完成框架分层、数据驱动、Fixture、Schema 校验、生命周期、Hook 和内部 Plugin 基础实践。
- 已通过 `pytest_runtest_makereport`、`item.funcargs` 与 Recorder 实现失败测试信息及请求记录采集。
- 已理解 Config、Request、Item、Call、Report 等核心对象的职责边界。
- 后续结合真实需求补充 Fixture Plugin 化、插件解耦、pytest11 发布与复杂多插件执行顺序。
- 当前 Pytest 学习服务于 CI 流水线建设，重点保留执行模型、Fixture 生命周期、Hook、结果采集、报告生成及 CI 运行方式；Plugin 深入开发不阻塞当前主线。

### API Testing

- 采用 `TestCase → Service → ApiClient → requests.Session → Backend` 分层。
- ApiClient 负责 HTTP 通信；Service 负责业务封装；断言由 TestCase 负责。
- Postman 作为面试需求驱动的工具学习专项：以已有 Apifox 经验切入基础使用，再进入进阶学习；学习完成后保留专项聊天用于后续答疑。

### Mock / Backend

- ApiFox Mock 基础阶段已完成。
- 服务级 Mock 路线：FastAPI 基础 → Mock Server → 接入测试框架。

### Jenkins / CI/CD

- 已完成基础 Pipeline、参数化构建、Credential 注入、Gitee checkout、pytest 执行及 JUnit/HTML 报告发布。
- 当前状态为 `学习中`；IndianTest 1.0.0 已完成，恢复真实项目 CI 实践。
- 当前路线：IndianTest 真实框架 CI 接入 → Pipeline 工程化优化 → 自动触发与结果反馈 → 完整 CI 流程。
- Groovy 定位为 Pipeline DSL 辅助能力。
- Python package 隔离与 CI 固定依赖安装已达 `基础完成`；Pipeline 中解释器来源检测和 Python 版本校验仍需实践。
- 后续目标采用多层运行入口 + Jenkins 动态调度；具体目录、接口和参数仍待框架重构专项验证。

### UI / Mobile Testing

- 求职前目标技术链为 `requests + Selenium + Appium + Pytest`。
- Selenium 已有学习或使用基础；Appium 当前为 `学习中`，至少完成基础部分后再开始求职。
- 当前 Appium 教程练习在独立的 AppiumDemo 项目中完成，并以实际运行结果作为状态提升依据。
- Appium 基础学习完成后，再将能力接入 BobTest 并实施其 UI 专项框架重构。

### Allure

- 已理解 pytest 结果 → Allure 报告 → Jenkins 展示的数据流，以及业务化报告、测试证据、失败分类、执行环境和趋势的作用。
- 当前路线：参数与环境控制 → 框架内 Allure 接入 → Jenkins 发布与趋势展示。
- 具体装饰器和 Attachment 实现细节属于知识与实践内容，不进入路线文件。

### Docker

- 在基础 CI 流水线稳定后学习，用于测试环境隔离与一致性。

### Data Structures & Algorithms

- 求职导向掌握常用结构、复杂度、排序与查找；高级算法按岗位需求补充。

## 5. Deferred Topics

- Java 技术栈。
- 深入后端开发、微服务和复杂部署运维。
- Mock.js、Easy Mock、WireMock 和大型服务虚拟化平台。
- Git 内部原理、源码分析和复杂企业分支模型。
- Jenkins 插件开发、Agent 分布式执行、Kubernetes CI/CD 和 Groovy 高级开发。
- 动态 Plugin Manager、动态服务/断言包、测试数据 DSL、Event Bus 和完整测试平台化设计。
- Pytest Plugin 深入开发；现有内部 Plugin 基础继续保留，后续仅按真实工程需要扩展。

## 6. Major Decisions

| Date | Type | Decision | Reason |
| ---- | ---- | -------- | ------ |
| 2026-08-14 | 用户已确认 | 当前主线使用 Python + Pytest，短期不学习 Java | 集中形成测试开发求职能力链 |
| 2026-08-15 | 用户已确认 | RESTful → Swagger/OpenAPI → Mock 阶段完成 | 已有文档、接口管理和 Mock 实践证据 |
| 2026-08-15 | 用户已确认 | 服务级 Mock 作为独立学习分支 | 避免与接口基础阶段混杂 |
| 2026-08-14 | 用户已确认 | 请求模型校验为可选能力；测试数据按接口组织 | 支持异常测试并保持职责清晰 |
| 2026-08-15 | 用户已确认 | Pytest 基础工程化阶段完成 | 已完成分层、数据驱动、Fixture、Demo 与报告 |
| 2026-08-17 | 用户已确认 | Git 建立独立专项，并完成阶段 1 | 已完成版本管理和协作实践 |
| 2026-08-19 | 用户已确认 | CI/CD 先于 Git 阶段 2 启动 | 已实际开始 Jenkins Pipeline 接入 |
| 2026-08-19 | 用户已确认 | Jenkins 回归真实框架；Groovy 仅作辅助 | 学习目标是测试框架 CI/CD，而非单独掌握 Jenkins/Groovy |
| 2026-08-19 | 用户已确认 | PracticeDemo-CI 用于语法实验，真实框架用于工程实践 | 分离实验与项目成果 |
| 2026-08-21 | 用户已确认 | Pytest 高级应用继续作为独立知识主线，ApiClient 插件化重构另开分支 | 保持 Hook/Fixture/Plugin 学习不被代码重构细节打断 |
| 2026-08-21 | 用户已确认 | 认证保持 session 生命周期；Recorder 聚焦 Hook 学习并采用简单挂载 | 控制当前框架复杂度，服务阶段目标 |
| 2026-08-25 | 用户已确认 | 当前工程主线形成 Pytest → Allure → Jenkins 能力链 | Allure 基础体系已学习，并已理解其在 CI 报告链路中的定位 |
| 2026-08-25 | 用户已确认 | Pytest Plugin 深入学习暂缓，转入参数管理与 CI 环境控制 | Plugin 深化不阻塞当前 CI 能力建设 |
| 2026-09-01 | 用户已确认 | CI 目标采用多层运行入口，并由 Jenkins 按测试类型和环境动态调度 | 分离框架执行职责与 CI 编排职责 |
| 2026-09-01 | 用户已确认 | 在继续 Jenkins 多入口改造前，先独立完成测试框架目录与运行入口重构 | 避免 Pipeline 依赖尚不稳定的框架接口 |
| 2026-09-01 | 用户已确认 | requirements 分层应基于实际运行入口和测试场景推进 | 避免脱离执行场景进行形式化拆分 |
| 2026-09-02 | 用户已确认 | 后续 Jenkins 学习基于 IndianTest 项目 | 使用正在重构的真实统一测试框架承接 CI 工程化实践 |
| 2026-09-02 | 用户已确认 | 开启 Appium 测试框架学习专项，练习部分在 BobTest 项目中完成 | 将知识学习与真实工程实践结合，并保持工程仓库独立维护 |
| 2026-09-02 | 用户已确认 | BobTest 定位为专用于练习的 Demo 项目，不作为求职主项目 | 区分学习练习载体与真实工程项目 |
| 2026-09-02 | 用户已确认 | Appium 学习与 IndianTest 1.0 建设并线推进，求职前至少掌握 Appium 基础 | 补齐 requests、Selenium、Appium、Pytest 技术链 |
| 2026-09-02 | 用户已确认 | CI/CD 学习等待 IndianTest 1.0 上线后恢复 | 使用已上线的真实项目承接 CI 工程化实践 |
| 2026-09-02 | 用户已确认 | Appium 教程按小阶段递进，确认掌握后再进入下一阶段 | 保证学习状态以理解和实践证据为依据 |
| 2026-09-07 | 用户已确认 | IndianTest 1.0.0 完成，恢复 Jenkins 学习 | CI/CD 恢复条件已满足，开始真实框架集成 |
| 2026-09-08 | 用户已确认 | 当前 Appium 练习集中在独立的 AppiumDemo 项目 | 将教程实验与后续框架实践分离 |
| 2026-09-08 | 用户已确认 | Appium 学习完成后，将 BobTest 重构为底层能力、Pages、插件与测试代码组成的 UI 自动化框架，移除 API 部分并加入 Appium | 明确 BobTest 的后续项目定位与实施时机 |
| 2026-09-10 | 用户已确认 | 当前聊天聚焦 Appium本身功能学习，UI自动化框架构建转交独立侧边聊天 | 分离工具能力学习与框架工程实践，避免两条内容混杂 |
| 2026-09-21 | 用户已确认 | 先完成 Appium 专项中尚未完成的功能学习与验收，再开始 ECMobile 项目实践 | 先补齐工具能力闭环，再用真实电商项目承接综合实践 |

## 7. Next Milestone

- 完成 IndianTest Jenkins Environment Check 与 Python 版本校验。
- 让 Jenkins 使用锁定依赖并通过统一 `run.py` 入口执行测试。
- 随后推进报告发布、自动触发与结果反馈。

## 8. AI Suggestions Not Yet Adopted

- 建议后续实践 pytest11 第三方插件打包、安装和发布；用户尚未确认。
- 建议使用独立 Jenkins Job 分离 Demo 与真实项目；是否实施尚未确认。
- 框架目录、requirements 文件和 run 层的具体组织方案仍为 AI 建议，尚未由工程实践确认。

## 9. Pending Decisions

- 多层运行入口的最终目录、接口形式和命令规范。
- requirements 的最终拆分粒度，以及环境准备与依赖安装在 Jenkins 和 run 层之间的职责边界。
- Jenkins 动态参数包含测试类型、环境、marker 等哪些维度。
- Webhook 自动触发和私有仓库 Credential 场景的实施方式。
- Allure Attachment 的最终工程实现方式。
- Allure 在 Jenkins 中作为主报告，还是与 pytest-html 并存。
- 是否安排 Fixture Plugin 化、pytest11 和 Recorder 解耦实践。
- Git 阶段 2 的启动时间、范围和实验仓库。
