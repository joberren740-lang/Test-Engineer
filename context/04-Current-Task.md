# Current Task

Last Updated: 2026-09-24

> Purpose: 本文件仅保存恢复当前工作所需的短期状态，不承担长期路线、长期背景或知识笔记职责。

## Active Task

Appium专项收尾：完成尚未验收的Appium功能学习，再进入ECMobile项目实践。

## Goal

- 盘点并完成Appium专项中尚未完成的功能实践与理解验收。
- 保持Appium功能学习与UI自动化框架工程化分离。
- Appium专项完成后，使用ECMobile及其本地后端进入真实业务项目实践。

## Confirmed State

- IndianTest 1.0.0 已完成，`main` 当前基线提交为 `8e65159`。
- 已具备统一 `run.py` 入口与 `requirements.lock.txt`。
- CI/CD 已从 `暂缓` 恢复为 `学习中`。
- 旧项目已有 Jenkins 基础 Pipeline、虚拟环境、pytest 和报告发布实践，不重复基础教学。
- Pipeline 中解释器来源检测与 Python 版本校验均已完成验收。
- Appium 阶段 1 已通过理解验收，当前恢复 Appium 学习。
- 当前 Appium 教程练习集中在新建的独立 AppiumDemo 项目。
- AppiumDemo 已本地安装 UiAutomator2 Driver 8.6.1。
- Node 24.19.0、npm 12.0.2、Temurin JDK 21.0.12 和 `JAVA_HOME` 已通过命令验证。
- UiAutomator2 Doctor 已验证 Java 正常，并报告 2 个必修修复项：Android SDK/`ANDROID_HOME` 未配置，导致 adb 与 emulator 不可用。
- Android Studio Quail 3（2026.1.3）已安装并正常进入欢迎页。
- Android Studio 已重新安装至 `D:\dev\Android\Android Studio`，SDK 与 `ANDROID_HOME` 统一为 `D:\dev\Android\Sdk`；ADB、Emulator 与 sdkmanager 已可用，尚未创建 AVD。
- AVD `Pixel_7_API_37` 已创建并启动，ADB显示 `emulator-5554 device`。
- 模拟器为 Android 17/API 37普通 4 KB页镜像；UiAutomator2 Doctor的所有必需项均通过，可选依赖暂不处理。
- Appium 3.7.0 已启动，UiAutomator2 8.6.1 加载成功并监听 4723；当前仅误将根路径 `/` 作为状态接口，返回 404。
- `GET /status` 已返回 `ready: true`，Server端响应 HTTP 200，阶段 2.3通过。
- Appium Python Client 6.0.2与 Selenium 4.48.0 已安装于 AppiumDemo `.venv`，当前 Python为 3.14.5，阶段 2.4通过。
- 首个 UiAutomator2 Session已成功创建、返回 sessionId并正常关闭，进程退出码0；实际前台应用为 Nexus Launcher而非系统设置。
- 已确认序列化结果包含正确的 `appium:appPackage` 与 `appium:appActivity`；同时有重复的未前缀 `automationName`，并需验证 `noReset` 与 `forceAppLaunch` 的启动语义。
- ADB已通过 `.Settings` 成功启动系统设置，Android 17实际落地 Activity为 `.homepage.SettingsHomepageActivity`。
- AppiumDemo `Scripts/first_session.py` 已成功创建 Session，将系统设置置于前台，读取到 `com.android.settings/.Settings`，并正常关闭 Session；阶段 2.5运行目标已达成。
- 脚本中的 `device_name=Pixel_7_API_7` 是显示名称笔误；本次实际设备由 `udid=emulator-5554` 唯一指定，因此不影响运行结果。
- 阶段 2.5已通过理解验收；能够说明 Client、Server、UiAutomator2与模拟器的基本调用关系，并理解 Session资源需要在异常路径中可靠释放。
- 阶段 3.1已通过运行与理解验收；设置页成功定位20个 `TextView`并读取其核心属性，已理解单元素/多元素查询及类名定位的非唯一性。
- 阶段 3.2已通过运行与理解验收；唯一搜索标题 ID定位成功并验证可见，通用标题 ID实际返回10个元素，已理解非唯一定位的误操作风险。
- 阶段 3.3已通过运行与理解验收；已点击 `Network & internet`进入 `.SubSettings`、验证子页面元素，并返回后重新验证设置首页。
- 阶段 3.4已通过运行与理解验收；已用 `WebDriverWait`替换固定等待，完成首页、子页面和返回后的动态状态验证，并理解条件轮询与超时异常。
- Appium Inspector已安装并连接 `127.0.0.1:4723/`，成功创建 Android Session，设备截图、Native控件树及定位搜索均可用。
- 阶段 3.5已通过实践与理解验收；能够对应截图、Native控件树和定位结果，理解 Inspector用于辅助开发而非替代自动化测试代码。
- 阶段 3.6已通过运行与理解验收；成功输入 `Bluetooth`、处理软键盘并返回设置首页，已区分键盘关闭与页面返回操作。
- 阶段 3.7已通过运行与理解验收；三次向下滚动后到达边界并成功定位当前镜像实际存在的底部元素 `Tips & support`，已区分手势结果与错误目标数据。
- 阶段 4.1已通过运行与理解验收；系统设置状态已实际验证为 `4 → 1 → 4`，并确认应用终止不等于 Appium Session关闭。
- 阶段 4.2已通过运行与理解验收；设置应用进入后台状态 `3`时 Launcher成为前台，重新激活后恢复状态 `4`，Session全程有效。
- AppiumDemo当前采用 `run.py → runner.run_session → scripts.<name>.run(driver)`结构，已集中创建和释放 Session；项目虚拟环境尚未安装 pytest。
- 用户确认本聊天仅学习 Appium本身功能；Pytest集成和UI自动化框架构建由独立侧边聊天负责，本聊天不继续 Fixture工程练习。
- 阶段 5.1的 HOME子项已通过运行验证：Launcher成为前台、设置保持后台状态 `3`，随后在同一 Session中重新激活成功。
- 阶段 5.1已通过运行与理解验收；Android KeyCode BACK与标准 `driver.back()`均完成同一返回导航，已理解两者的抽象层级与平台范围。
- 阶段 5.2已通过运行与理解验收；已查询系统设置的 requested、granted和denied权限，并理解查询命令与 Session初始化自动授权的边界。
- 已只读确认模拟器存在 `com.android.camera2`，其 `ACCESS_FINE_LOCATION`当前未授权，适合作为可恢复的权限变更练习对象。
- `mobile: changePermissions`已成功对相机临时授予两级位置权限并恢复原状态；当前需确认命令中的 `appPackage`可独立指定，不受 Session初始 `appPackage`限制。
- 阶段 5.3已通过运行与理解验收；已确认权限命令可显式指定其他应用包，省略时才默认使用 Session目标包。
- 阶段 5.4已通过运行与理解验收；Camera权限弹窗的触发、文本读取、拒绝以及原始权限和前台应用恢复均成功。
- 阶段 5.5已通过运行与理解验收；截图文件、PNG字节、Base64文本和Native Page Source均已实际获取并验证。
- 阶段 5.6已通过运行与理解验收；当前 Session成功返回三种日志类型及10000条 Logcat，已理解 Server日志与设备日志的层级区别。
- 阶段 5.7已通过运行与理解验收；`threadtime`格式和Tag级别过滤已在新 Session生效，Logcat由10000条降至225条，且不再出现目标Tag阈值以下日志。
- 阶段 5.8已通过运行与理解验收；录屏返回内容成功解码为1274798字节MP4且可正常播放，已理解录制启动、停止取回结果与异常清理。
- 阶段 5已完成，覆盖Android系统按键、应用状态、权限、截图与Page Source、日志和屏幕录制。
- 阶段 6.1已通过运行与理解验收；0.08比例下已分别用3次scroll和3次swipe完成往返，已理解轨迹比例、Android手势识别、方向与返回值差异。
- 阶段 6.2已通过运行与理解验收；以5000像素/秒两次fling至底部目标可见，并正确使用边界返回值；已理解速度控制、内容方向和动作后边界语义。
- 阶段 6.3已通过运行与理解验收；媒体音量进度条已按 `dragGesture`参数实际移动，已理解 `elementId`、元素内部相对起点、屏幕绝对终点和 `rect`。
- 阶段 6.4已通过运行与理解验收；W3C Pointer Actions已成功执行，能够说明触摸序列、viewport与元素原点，以及Selenium和Appium在协议、客户端与执行后端上的异同。阶段 6完成。
- 阶段 7.1已通过运行与理解验收；已成功创建Android Chrome Mobile Web Session，可用Context为 `NATIVE_APP` 与 `CHROMIUM`，当前Context为 `CHROMIUM`，并成功完成页面导航和标题读取。
- 阶段 7.2已通过运行与理解验收；已在真实百度页面完成 `CHROMIUM → NATIVE_APP → CHROMIUM`，分别读取Web DOM与Android XML控件树，并验证切回后HTML元素定位正常。
- 阶段 7.3已通过运行与理解验收；已动态等待并选择Web Context，在错误Native Context中验证HTML定位异常，切回后恢复正常。阶段 7完成。
- 阶段 8.1已通过运行与理解验收；`mobile: startActivity`返回 `Status: ok`和HOT启动结果，前台包恢复为系统设置且Session ID不变。此次从Web Session发出的Android移动扩展仍由UiAutomator2成功执行，但原生页面元素操作需要 `NATIVE_APP`。
- Intent action、URI、extras与flags已完成基础实践和概念验证，能够区分组件、隐式Intent匹配、参数契约与任务栈标志。
- ECMobile 3.2 APK已在Android 9/API 28模拟器成功启动；模拟器访问宿主机Apache及ECMobile PHP接口的链路已验证。
- ECMobile通过模拟器Wi-Fi代理接入Fiddler后，`shop.ecmobile.cn/ecmobile/`请求已进入本地Apache；Fiddler与access日志中的`/config`、`/cart/list`时间、状态和响应长度相互对应。
- 用户确认当前顺序为：先完成Appium剩余学习内容，再开始ECMobile项目实践；当前网络验证只作为项目实践前置环境证据。
- Appium 学习完成后再重构 BobTest：移除 API 部分、加入 Appium，并保留底层能力、Pages、插件和测试代码分层；当前不提前实施。
- Jenkins 已完成 Environment Check、版本校验、干净 `.venv`、锁定依赖安装和统一入口集成验收；`mock` 环境可达，UTF-8 中文日志与 `bat` 参数结构均已验收，4 条 API 用例通过并返回 SUCCESS；日志中尚无报告发布阶段。

## Open Items

- Postman 独立专项已建立：本专项聊天用于基于 Apifox 的基础使用学习、进阶学习及完成后的答疑；下一步开始基础使用，尚无实践验收证据。Appium 与 Jenkins 原有任务继续保留。
- Postman 大纲已保存至用户确认的位置：[Postman学习大纲](<D:/DB/obsidian/Software Engineering/1-Test Engineering/4-Testing Technology/4-Postman/Postman学习大纲.md>)；细化内容仍为建议稿，保存不代表完成学习。学习内容完成后仅删除大纲并清理引用，保留主题文件夹、笔记和附件。

- 修正并验证ECMobile Native Session中的终止/激活逻辑：使用固定目标包名，避免终止后再次读取动态`current_package`。
- 盘点Appium专项尚未完成或尚无运行证据的内容，逐项完成实践与验收。
- Appium专项结束后再进入ECMobile业务流程和UI自动化项目实践。
- Jenkins 参数化统一入口已通过验收；并线任务下一步处理 JUnit、HTML、Allure 报告发布生命周期。

## Next Action

先完成ECMobile Native Session终止与激活的修正验证，再盘点并继续下一个尚未完成的Appium功能阶段。
