# Learning Progress

> Last Updated: 2026-09-23
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

IndianTest 1.0.0 已完成，Jenkins CI/CD 学习已恢复；当前 Appium 专项先完成剩余功能学习与验收，之后再进入 ECMobile 项目实践。

## 2. Progress Overview

| Topic | Status | Current Level / Evidence | Next Action |
| ----- | ------ | ------------------------ | ----------- |
| RESTful / Swagger / ApiFox Mock | 阶段完成 | 已完成接口基础、文档与 Mock 实践 | 按需复习和应用 |
| Postman | 待学习 | 已确认按 Apifox 经验迁移基础使用 → 进阶学习 → 后续答疑推进；暂无 Postman 实践或验收证据 | 从基础使用及与 Apifox 的对应关系开始 |
| Pytest 基础工程化 | 阶段完成 | 完成分层、数据驱动、Fixture、Demo 与报告 | 作为 CI 接入基础 |
| Pytest 生命周期与 Hook | 阶段完成 | 实践 configure、collection、setup/call/teardown、makereport 并验证顺序 | 按需验证复杂多插件场景 |
| Fixture 资源设计 | 阶段完成 | 实践 session 认证和 function Recorder，明确 Fixture/Hook 职责 | 验证 Fixture Plugin 化 |
| Recorder 失败采集 | 阶段完成 | 成功采集 TestID、异常与请求记录 | 降低对固定 Fixture 名称的依赖 |
| pytest 核心对象 | 基础完成 | 能说明 Config、Request、Item、Call、Report 职责并在 Hook 中使用 | 避免无需求深入内部 API |
| 项目内部 Plugin | 基础完成 | Recorder Hook 已从 conftest 拆分并通过 pytest_plugins 加载 | 优化目录与通用接口 |
| pytest11 第三方插件 | 需要实践 | 仅理解 entry point，未打包、安装或发布 | 后续按价值决定是否实践 |
| Allure 报告体系 | 学习中 | 已理解业务化报告、测试证据、失败分类、执行环境、历史趋势及 Jenkins 展示链路 | 接入当前接口自动化框架 |
| Allure 框架接入 | 基础完成 | 重构后的 API 链路已实际生成 Allure 报告；失败用例能够展示 Request、Response、Test Exception 与日志附件 | 后续补充执行环境信息并接入 Jenkins 发布 |
| Allure attach | 基础完成 | 已在重构后的框架中再次验证，请求、响应、异常和日志附件均正常展示 | 后续补充敏感信息脱敏与边缘失败场景 |
| Git 阶段 1 | 阶段完成 | 完成本地版本、分支、冲突与远程协作 | 为 CI/CD 提供基础 |
| Git 高级使用 | 待学习 | rebase 尚无独立实践 | 后续确认阶段 2 |
| Jenkins 基础 Pipeline | 阶段完成 | 完成 Pipeline、参数化和 Credential 基础实践 | 转入工程化优化 |
| pytest 接入 Jenkins | 阶段完成 | 完成 checkout、依赖安装、pytest 与报告发布 | 稳定入口和环境 |
| Python CI 环境控制 | 基础完成 | IndianTest-CI 已验证 Python 3.14.5 的版本、解释器和 pip 来源；正向校验继续构建，反向校验以 exit code 1 主动失败并跳过后续阶段 | 保持校验并转入统一入口集成 |
| Python 依赖管理 | 学习中 | IndianTest-CI 已在清空 workspace 后新建 `.venv`，并从 `requirements.lock.txt` 成功安装全部精确版本；场景分层尚未落地 | 保持锁文件基线并按实际场景评估分层 |
| requirements 场景分层 | 需要实践 | IndianTest API 1.0 已清理直接依赖、生成精确锁文件，并通过全新虚拟环境安装与运行验证；API/UI/CI 多文件拆分尚未实施 | 1.0完成后按执行场景拆分 |
| pytest CI 稳定执行 | 基础完成 | `INTERNALERROR` 已消失，失败可按普通 assertion failure 和 exit code 1 表达并生成报告 | 继续验证完整失败生命周期 |
| 测试失败生命周期处理 | 学习中 | 已消除当前内部错误，但用户确认完整机制仍在修复 | 完成专项验证 |
| 多层运行入口 | 基础完成 | Jenkins 已通过构建参数将 run-config、type 传入统一 `run.py` 入口；`api` 与 `all` 构建均已验证 | 保持入口契约并完善报告发布 |
| 测试框架结构重构 | 阶段完成 | IndianTest 1.0.0 已形成统一入口、API Plugin、数据参数化、统一断言、日志、附件、异常退出码、锁定依赖及项目文档 | 作为 Jenkins CI 真实工程基线 |
| Jenkins 动态入口调度 | 基础完成 | `RUN_CONFIG`、`TEST_TYPE` 使用受限 choice 参数并映射到 `run.py`；`TEST_TYPE=all` 已成功完成动态构建 | 后续随真实配置和测试类型扩展 |
| Groovy Pipeline DSL | 基础完成 | 理解方法、闭包与 Pipeline 嵌套 | 按需复习 |
| CI/CD 总体 | 学习中 | IndianTest-CI 已完成环境稳定性、锁定依赖、UTF-8 日志和参数化统一入口；尚无完整自动闭环 | 完善报告发布生命周期 |
| FastAPI / 服务级 Mock | 待学习 | 已建立独立学习分支 | 后续构建 Mock Server |
| Docker | 待学习 | 暂无实践证据 | CI 稳定后学习 |
| JMeter | 需要实践 | 有参数关联和 Groovy 数据处理实践 | 补充完整性能测试 |
| Fiddler Classic | 基础完成 | 已实际完成 HTTP/HTTPS 抓包解密、Composer、断点、AutoResponder、延迟与断连模拟、重定向、缓存、CORS、Replay 和 Timeline；ECMobile 代理链路已有前置验证 | 在 ECMobile 真实业务流程中继续练习请求关联、Android HTTPS 与证据交付 |
| Appium 测试框架 | 学习中 | 已完成Intent action、URI、extras与flags基础实践；ECMobile APK、API 28模拟器、本地后端及Fiddler代理通信链路已验证 | 盘点并完成剩余Appium功能，再进入ECMobile项目实践 |
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
- 完成 Jenkins workspace 内 `.venv` 创建、CI 固定依赖安装及虚拟环境内 pytest 执行的基础实践。
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

1. 明确 IndianTest 的 JUnit、HTML、Allure 三类报告产物及 Jenkins 职责。
2. 增加 Jenkins 报告发布逻辑。
3. 验证测试失败时报告仍可被发布和保留。

### After Current Stage

1. IndianTest 1.0 上线后恢复 Jenkins Environment Check、版本校验及后续 CI 工程化工作。
2. 继续 workspace、Webhook、Allure 报告发布和结果反馈闭环。
3. 按价值决定 Fixture Plugin 化、pytest11 和 Recorder 解耦实践。
4. 再确认 Docker、Git 阶段 2 与 FastAPI Mock 的启动时间。

## 9. Recent Updates

- **2026-09-23：** Fiddler Classic 基础学习形成实际操作证据：完成代理与 HTTPS 解密、报文分析和多种请求体构造，并验证断点、AutoResponder、延迟、连接中断、重定向、ETag/304、CORS、Replay 与 Timeline；工具基础达到 `基础完成`，后续结合 ECMobile 真实业务流程继续实践。
- **2026-09-21：** 用户确认先完成 Appium 专项中尚未完成的功能学习与验收，再进入 ECMobile 项目实践；ECMobile APK 已在 API 28 模拟器启动，并经 Wi-Fi 代理、Fiddler 和本地 Apache 实际验证 `/config`、`/cart/list` 请求及响应链路，当前只作为后续项目实践的环境前置证据。
- **2026-09-14：** Appium阶段 8.1 通过：从桌面调用 `mobile: startActivity`启动系统设置，Activity Manager返回 `Status: ok`和 `LaunchState: HOT`，前台包恢复为 `com.android.settings`且Session ID保持不变；理解 `wait`不替代页面显式等待、`stop=true`会先终止目标进程。此次命令从Chrome Web Session发出仍成功，说明该Android移动扩展由UiAutomator2层执行，但后续原生元素操作仍需切到 `NATIVE_APP`。
- **2026-09-14：** IndianTest-CI 参数化统一入口通过验收：`RUN_CONFIG` 与 `TEST_TYPE` 使用受限 choice 参数并映射到 `run.py`，`TEST_TYPE=all` 动态构建成功；Jenkins 动态入口调度达到 `基础完成`。
- **2026-09-14：** Appium阶段 7.3 通过：使用 `WebDriverWait`动态选择非 `NATIVE_APP` Context；在Native Context按HTML标签定位得到 `InvalidSelectorException`，切回 `CHROMIUM`后body可见且标题正常。理解Context名称不应硬编码及错误Context定位失败不代表屏幕内容不存在。阶段 7完成。
- **2026-09-14：** Appium阶段 7.2 通过：访问百度后在同一Session中完成 `CHROMIUM → NATIVE_APP → CHROMIUM`，分别读取236个Web DOM节点与32个Native控件，切回后成功定位HTML body并读取页面标题；理解Context切换不改变屏幕页面，而是改变命令的目标驱动和元素树。
- **2026-09-14：** Appium阶段 7.1 通过：模拟器Chrome与WebView均为145.0.7632.218，Appium自动匹配ChromeDriver后成功创建Mobile Web Session；可用Context为 `NATIVE_APP` 与 `CHROMIUM`，当前Context为 `CHROMIUM`，并成功访问百度、读取URL和页面标题。理解 `browserName`、ChromeDriver DOM控制及浏览器/驱动版本兼容关系。
- **2026-09-14：** IndianTest-CI UTF-8 修复通过验收：`bat` 的 Groovy 参数结构已修正，不再执行无效的 `encoding:`/`script:` 命令；中文日志正常，Run Config/Test Type 正常显示，4 条用例通过并返回 SUCCESS。
- **2026-09-14：** IndianTest-CI 中文业务日志已通过 `chcp 65001` 和 Python UTF-8 环境变量恢复正常，但 `encoding:`、`script:` 被误放入批处理文本并作为 Windows 命令执行；因末尾测试返回 0，Pipeline 仍显示 SUCCESS。需修正 `bat` Groovy 参数结构后再验收。
- **2026-09-13：** IndianTest-CI 完整正向流水线通过：checkout `main@8e65159`，校验 Python 3.14.5，清空 workspace 后创建 `.venv`，安装 `requirements.lock.txt`，通过统一 `run.py test --run-config product_create_product --type api` 执行 4 条用例并返回 SUCCESS；同时发现中文日志乱码、旧参数输出 `Current module: null`，且尚未看到 Jenkins 报告发布步骤。
- **2026-09-13：** Appium阶段 6.4 通过：使用W3C Pointer Actions成功执行 `pointerMove → pointerDown → pause → pointerMove → pointerUp`触摸序列；理解按下前定位起点、按下后形成移动、viewport与元素坐标原点，以及Selenium/Appium共享协议和客户端动作模型但执行后端不同。确认Selenium 4.48.0对 `origin`的类型标注会提示str不匹配，省略时按W3C默认使用viewport。阶段 6完成。

- **2026-09-13：** IndianTest-CI Environment Check 通过真实 Console Output 验收：基础解释器为 Python 3.14.5，路径为 `D:\dev\python\3.14.5\python.exe`，`python -m pip` 对应同一 Python 3.14 环境；下一步进入版本校验。
- **2026-09-13：** IndianTest-CI Python 版本校验通过正反向构建验收：3.14.x 正向构建成功；临时要求 3.13.x 时命令返回 exit code 1，Install 与 Test 阶段均被跳过。Python CI 环境控制达到 `基础完成`。
- **2026-09-13：** Appium阶段 6.3 通过：在系统声音页面定位媒体音量控件，使用 `elementId`、元素内部相对起点及屏幕绝对终点执行 `dragGesture`，实际观察到音量进度条按脚本移动；理解 `rect`、元素引用及两类坐标体系。真实测试仍应补充原音量恢复。
- **2026-09-12：** Appium阶段 6.2 通过：修正可见性方法调用和参数边界后，使用 `flingGesture`以5000像素/秒两次甩动至 `Tips & support`可见，并以返回值控制边界；理解fling速度影响惯性而非直接指定最终距离、direction表示内容滚动方向以及false表示动作后到达边界。
- **2026-09-12：** Appium阶段 6.1 通过：在同一区域对比 `scrollGesture`与`swipeGesture`，将比例降至0.08后分别用3次完成向下与返回顶部操作；理解 `percent`约束手势轨迹而非最终内容位移、短轨迹可能被Android控件按点击识别，以及两者都通过触摸手势执行但目标语义和返回值不同。
- **2026-09-12：** Appium阶段 5.8 通过：成功启动和停止设备端屏幕录制，获得Base64字符串并解码保存为1274798字节的MP4，视频可正常播放；理解启动录制、停止并返回结果、客户端解码以及异常路径清理的职责边界。阶段 5完成。
- **2026-09-12：** Appium阶段 5.7 通过：使用 `threadtime`格式及 `ActivityTaskManager:I`、`AndroidRuntime:E`、`*:S`过滤规则重新创建 Session，Logcat由10000条降至225条；输出中不再出现目标 Tag阈值以下日志。定位并修正了规则末尾空格导致优先级回退到 Verbose的问题。
- **2026-09-10：** Appium阶段 5.6 通过：当前 Session支持 `logcat`、`bugreport`和`server`，成功获取10000条 Logcat并控制为最后10条样本输出；能够区分 Server层日志与 Android设备层日志，并理解 `skipLogcatCapture`会禁用采集。
- **2026-09-10：** Appium阶段 5.5 通过：截图成功保存，PNG返回209742字节、Base64返回277256字符，Page Source返回51536字符并保存为XML；能够区分屏幕像素证据与当前控件树快照，以及字节与文本编码形式。
- **2026-09-10：** Appium阶段 5.4 通过：临时撤销 Camera权限后成功触发系统授权弹窗，读取文本、执行拒绝，并在 `finally`中恢复 Camera权限为已授权及前台应用为 Settings；理解自动授权、Alert代理与环境恢复职责。

- **2026-09-10：** Appium阶段 5.3 通过：理解权限命令省略 `appPackage`时默认使用 Session目标包，显式提供时可操作其他包；相机两级位置权限的授权、验证与原状态恢复均已成功。
- **2026-09-10：** Appium阶段 5.3运行验证完成：Session目标仍为系统设置，但通过 `mobile: changePermissions`显式指定 `com.android.camera2`，成功临时授予粗略/精确位置权限并在 `finally`中恢复为空；待校正“Session目标包与权限命令目标包”的理解边界后完成验收。
- **2026-09-10：** Appium阶段 5.2 通过：系统设置包查询到 requested 320项、granted 200项、denied 0项，并采用“总数+前10项”控制输出；理解 requested不等于已授权、查询不修改权限，以及 `autoGrantPermissions`由 Server/Driver在 Session初始化阶段处理。

- **2026-09-10：** Appium阶段 5.1 通过：HOME使 Launcher进入前台且设置保持后台，重新激活设置成功；Android KeyCode BACK与标准 `driver.back()`均从 `Network & internet`返回设置首页，已理解两者的平台范围与抽象层级。
- **2026-09-10：** Appium阶段 5.1 HOME子项通过：`press_keycode(AndroidKey.HOME)`后 Launcher成为前台、设置应用状态为后台运行 `3`，随后在原 Session中重新激活设置成功；下一步对比 Android KeyCode BACK与标准 `driver.back()`。
- **2026-09-10：** 用户确认当前聊天只继续 Appium本身的功能学习；Pytest集成、Page Object、Fixture及UI自动化框架构建转交独立侧边聊天，因此撤回本聊天的阶段 5.1 Fixture任务，改为继续 Android平台功能。
- **2026-09-10：** Appium阶段 4.2 通过：`background_app(-1)`后系统设置进入后台运行状态 `3`且 Launcher成为前台，再通过 `activate_app()`恢复设置前台状态 `4`；已理解后台、未运行与 Session关闭的边界。AppiumDemo已形成集中 Session管理的 runner与按名称加载练习脚本的结构，当前 `.venv`尚未安装 pytest。
- **2026-09-10：** Appium阶段 4.1 通过：系统设置初始状态为前台运行 `4`，`terminate_app()`返回 `True`后状态为未运行 `1`，同一 Session中重新激活后恢复前台状态 `4`且包名正确；已区分应用终止与 Session关闭。
- **2026-09-10：** Appium阶段 3.7 通过：设置列表第三次向下滚动后返回 `False`并成功定位 `Tips & support`；确认手势执行、边界判断和滚动后查询均正常，先前失败源于目标文本 `About phone`不属于当前系统镜像。
- **2026-09-09：** Appium阶段 3.6 通过：设置搜索框成功输入 `Bluetooth`，检测并关闭软键盘，随后通过 Android返回操作回到 `Search Settings`首页并正常释放 Session；已区分关闭键盘、返回上一页与返回系统桌面。
- **2026-09-09：** Appium阶段 3.5 通过：能够使用 Inspector查看截图与 Native控件树、理解匹配数量并将属性转换为代码定位器；明确 Inspector是开发辅助客户端，控件树是当前结构快照而非应用布局源码。
- **2026-09-09：** Appium Inspector已完成安装并成功创建本地 Android Session，能够同时显示模拟器截图与 Native控件树；搜索 `com.android.settings:id/search_bar_title`返回1个节点，阶段 3.5进入可视化定位使用验收。
- **2026-09-09：** Appium阶段 3.4 通过：使用显式等待完成设置首页、`.SubSettings`子页面和返回首页的状态验证；能够说明固定等待与条件轮询的区别、可见性条件语义及超时异常。
- **2026-09-09：** Appium阶段 3.3 通过：点击 `Network & internet`后进入 `.SubSettings`并定位到 `Internet`，调用返回操作后重新验证 `Search Settings`；理解交互前后均需验证页面状态，并校正点击命令最终由设备端自动化驱动执行。
- **2026-09-09：** Appium阶段 3.2 通过：唯一 ID成功定位 `Search Settings`并验证可见；`android:id/title`实际匹配10个列表标题，能够说明非唯一条件下 `find_element`返回首个匹配所带来的误操作风险。
- **2026-09-09：** Appium阶段 3.1 通过：修正 `TextView`类名后成功读取设置页20个元素及其属性；能够区分 `find_element`与 `find_elements`，并确认 `resource-id`通常比文本更适合维护，但同一列表模板可复用相同 ID，不能假定其必然唯一。
- **2026-09-09：** Appium阶段 2.5 通过理解验收：能够说明 Session创建时的配置传递和 Server按配置调用 UiAutomator2控制模拟器的链路；已校正 `deviceName`与 `udid`以及 `finally`清理语义的边界，进入 Native元素定位基础。
- **2026-09-09：** Appium阶段 2.5 通过运行验收：`first_session.py` 成功创建 UiAutomator2 Session，系统设置进入前台，读取到 `com.android.settings/.Settings`，随后正常 `quit()`；脚本中的 `device_name=Pixel_7_API_7` 为不影响本次选择设备的显示名称笔误，实际设备由 `udid=emulator-5554` 明确指定。
- **2026-09-09：** `adb shell am start -W -n com.android.settings/.Settings` 返回 `Status: ok`，实际 Activity为 `com.android.settings/.homepage.SettingsHomepageActivity`；确认 Android入口可用。当前 Python输出仍缺少 `appium:forceAppLaunch`，且重复的未前缀 `automationName`尚未清理。
- **2026-09-09：** 首个 Session的实际 Capabilities已确认包含 `appium:appPackage=com.android.settings` 与 `appium:appActivity=.Settings`；同时存在重复的未前缀 `automationName`，目标应用未前台化的当前主要假设为 `noReset=True` 下缺少 `forceAppLaunch`，待运行验证。
- **2026-09-09：** Appium阶段 2.5首次运行已成功创建 Session并正常 `quit()`，Python进程退出码0；读取到前台包名 `com.google.android.apps.nexuslauncher`、Activity `.NexusLauncherActivity`，尚未达到启动系统设置的验收目标。
- **2026-09-09：** Appium阶段 2.4 通过：Appium Python Client 6.0.2与 Selenium 4.48.0 安装于 AppiumDemo `.venv`，Python版本为 3.14.5；进入首个 Session实践。
- **2026-09-09：** Appium阶段 2.3 通过：`GET /status` 返回 `ready: true`，Server端返回 HTTP 200，Appium Server连通性验证完成。
- **2026-09-09：** UiAutomator2 Doctor确认必需问题均已修复；Appium 3.7.0 成功加载 UiAutomator2 8.6.1 并监听 `0.0.0.0:4723`。对根路径的 GET请求返回 404符合路由预期，待验证 `/status`。
- **2026-09-09：** Appium阶段 2.2 通过环境验收：模拟器为 Android 17/API 37，`PAGE_SIZE=4096`；Doctor中 `ANDROID_HOME`、ADB、Emulator、`JAVA_HOME`与 Java均通过，缺失项仅为当前不需要的可选扩展。
- **2026-09-08：** AVD `Pixel_7_API_37` 已创建；`emulator -list-avds` 可识别，启动后 `adb devices -l` 显示 `emulator-5554 device`，Android SDK、Emulator与ADB链路通过实际验证。
- **2026-09-08：** Android Studio 重新安装至 `D:\dev\Android\Android Studio`，SDK 位于 `D:\dev\Android\Sdk`，现已与 `ANDROID_HOME` 统一，原双路径问题解除。
- **2026-09-08：** 新终端已验证 `ANDROID_HOME`、ADB 37.0.1、Emulator 和 sdkmanager 可用，尚无 AVD；终端使用 `D:\dev\Android\Sdk`，与此前 SDK Manager 显示的 `D:\Android\Sdk` 不一致，需先确认并统一。
- **2026-09-08：** SDK Manager 验证：Android SDK 位于 `D:\Android\Sdk`；Android 17/API 37.0 Platform、Command-line Tools、Emulator 37.1.11 与 Platform-Tools 37.0.1 已安装，Build-Tools 有 37.0.0 更新可用。
- **2026-09-08：** Android Studio Quail 3（2026.1.3）已安装并进入欢迎页；尚未验证 Android SDK组件、`ANDROID_HOME`、ADB与模拟器。
- **2026-09-08：** UiAutomator2 Doctor 完成 7 项检查：Java 通过，确认 2 个必修修复项为 Android SDK/`ANDROID_HOME` 与由此缺失的 adb、emulator；bundletool、ffmpeg、gstreamer 为可选项，当前不处理。
- **2026-09-08：** AppiumDemo 环境验证：Node 24.19.0、npm 12.0.2、UiAutomator2 Driver 8.6.1、Temurin JDK 21.0.12 均正常；`JAVA_HOME` 指向 JDK 21，下一步检查 Android SDK、ADB 与模拟器。
- **2026-09-08：** 新建独立 AppiumDemo 项目，当前 Appium 教程练习、配置和运行证据集中于此。
- **2026-09-08：** 确认 Appium 学习完成后再重构 BobTest：移除 API 部分，加入 Appium，并定位为底层能力、Pages、插件和测试代码组成的传统 UI 自动化框架；当前尚未实施。
- **2026-09-08：** Appium 阶段 1.3 通过理解验收；能够区分 Native 控件树与 Web DOM，并说明 Hybrid 流程的 Context 切换，阶段 1 整体完成，进入阶段 2.1。
- **2026-09-07：** IndianTest `docs/MODELS.md` 已与当前模型、注册表、YAML映射、异常退出码和延后项对齐；项目 Markdown 文档已完成上线前集中检查。
- **2026-09-07：** IndianTest 1.0.0 完成，CI/CD 从 `暂缓` 恢复为 `学习中`；当前进入 Jenkins Environment Check。
- **2026-09-07：** IndianTest `docs/ARCHITECTURE.md` 完成，记录框架分层、启动、配置、数据、请求、证据、日志、退出码及 Jenkins 集成边界；下一步校对 `docs/MODELS.md`。
- **2026-09-07：** IndianTest 根目录 `README.md` 完成，覆盖项目定位、目录职责、环境安装、统一入口、配置、测试数据、产物、退出码和当前限制；下一步编写架构文档。
- **2026-09-07：** IndianTest API 1.0 完成直接依赖清理与锁文件生成，并通过全新虚拟环境安装和运行验证；下一步补齐 README 与架构文档，再进入 Jenkins 统一入口集成验收。
- **2026-09-03：** Appium 阶段 1.2 通过理解验收；能够说明 Capabilities 与 Session 的先后关系、sessionId 的作用，以及 Python driver 对象与 UiAutomator2 Driver 的职责区别，进入阶段 1.3。
- **2026-09-03：** Appium 阶段 1.1 通过理解验收；能够说明 Client、Server、Driver、设备及 Pytest 的基本职责和请求链路，进入阶段 1.2。
- **2026-09-02：** 明确 Appium 基础学习与 IndianTest 1.0 建设并线推进；求职前至少掌握 Appium 基础，形成 `requests + Selenium + Appium + Pytest` 技术链。
- **2026-09-02：** BobTest 定位调整为专用于练习的 Demo 项目；CI/CD 总体调整为 `暂缓`，等待 IndianTest 1.0 上线后恢复。
- **2026-09-02：** 开启 Appium 测试框架学习专项；学习过程中的练习统一在独立的 BobTest 项目中完成，当前尚无完成证据。
- **2026-09-02：** 已确认后续 Jenkins 学习切换为基于 IndianTest 项目；当前 Appium 专项和 IndianTest 框架重构安排不变。
- **2026-09-02：** 重构后的 API Plugin、Fixture、ApiCase 参数化与统一断言基础链路完成实际 pytest 运行验证，结果符合预期；框架整体重构状态仍为 `学习中`。
- **2026-09-02：** 重构后的 Allure 失败诊断链完成实际报告验证，4 条用例通过、1 条预期断言失败，Request、Response、Test Exception 与日志附件均正常展示；Allure 框架接入达到 `基础完成`。
- **2026-09-02：** 统一 Runner 已通过 Python 文件调用 `pytest.main()` 完成基础执行验证；报告参数与 run_id/产物路径统一仍待实现。
- **2026-09-02：** Runner 的 run_id 共享、Allure Results 目录和 pytest 退出码传递完成实际验证；4 条通过、1 条预期失败时外部进程正确返回退出码 1。
- **2026-09-02：** Runner 根据 `ReportConfig` 动态注入 Allure 参数完成验证；开启时生成 29 个结果文件，关闭时不注入 Allure 参数，并使用项目绝对产物路径。
- **2026-08-15：** RESTful → Swagger/OpenAPI → Mock 与 Pytest 基础工程化通过验收。
- **2026-08-17：** Git 专项阶段 1 通过验收。
- **2026-08-19：** Jenkins 基础接入子阶段通过验收，CI/CD 总体调整为 `学习中`。
- **2026-08-21：** Pytest 高级工程化子阶段通过验收，完成生命周期、Hook、Recorder 失败采集和内部 Plugin 实践。
- **2026-08-21：** 保留 Jenkins CI/CD 为当前工程主线；材料中的“尚未进入 CI/CD”被判定为过期路线信息，未写入。
- **2026-08-25：** Allure 基础概念体系完成学习，报告体系调整为 `学习中`，并进入真实框架接入实践。
- **2026-08-25：** 当前入口调整为 Pytest 参数管理与 CI 环境控制；Pytest Plugin 深入学习调整为 `暂缓`，不改变内部 Plugin 已有完成状态。
- **2026-09-01：** Python CI 环境控制达到 `基础完成`，真实框架已在 Jenkins 创建的 `.venv` 中执行并正常表达测试结果。
- **2026-09-01：** 运行入口方向明确为多层入口 + Jenkins 动态调度；当前先进入框架目录与入口重构专项，完成后返回 CI 主线。
