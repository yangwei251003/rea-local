---
name: rea-local
description: 使用 REA 逆向分析已发布应用、二进制、反编译、Electron ASAR、JavaScript 应用包、.NET 程序集，理解无源码软件的功能实现、比较发布版本和重建行为。Reverse Engineer Anything MCP 本机接入。
---

# REA 本机入口

适用于用户提供的发布程序、应用包或明确要求的运行行为取证。普通源码仓库阅读用原生文件工具。

先完整读取官方技能 已安装的 `reverse-engineer-anything/SKILL.md`，再按该技能读取当前目标所需参考资料。此入口不替代官方约束或工具 schema。

Codex 注册的服务器名为 `rea`。有实际暴露的 REA MCP 工具时直接使用真实工具及其 schema；配置存在不证明当前会话已连接。无工具时按官方 connection-and-recovery 指南诊断，CLI 可完成其支持的已授权工作。

CLI通过当前环境的`rea`入口调用。诊断仅在连接或能力受阻时按官方指南执行，无需每次任务重新安装或setup。

JavaScript/Electron 静态分析优先 `analyze_javascript_application`；.NET 静态分析使用 `inspect_managed_artifact`。原生反编译需要可用 Ghidra/IDA 等引擎，不能把工具已列出当作引擎可用。未经请求不运行目标程序或扩大取证范围。

不要把安装验收中的样例路径当成用户的分析目标。
