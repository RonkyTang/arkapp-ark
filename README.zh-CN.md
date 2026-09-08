<!--
  Aligned Simplified Chinese copy. 2026-09-08 product decision: do not create
  a separate github.com/arkapp/ark. The currently public git README is already
  used for SEO.

  The three language files carry the same claims, sections, and links; when one
  changes, change all three. Every claim must stay consistent with
  documents/GTM/website/WEBSITE_CONTENT_RATIONALE.md section 5: no unverified
  numbers, no competitor comparisons without a source and a date.
-->
-->

[English](README.md) · **简体中文** · [日本語](README.ja.md)

# Ark — AI 原生的终端与 SSH 客户端

Ark 是一个面向远程服务器的 SSH 客户端和终端，内置的 AI 智能体直接在你已经连上的
那台机器上工作。终端、SFTP 文件传输和服务器状态共用同一条真实连接，因此智能体
从实时事实出发，而不是先让你描述自己的环境。

**macOS 11+（Apple Silicon 与 Intel）· Windows x64 · 提供免费版**

[**下载 Ark**](https://arkapp.ai/#download) ·
[智能体能做什么](https://arkapp.ai/ai-ssh-client) ·
[macOS](https://arkapp.ai/ssh-client-mac) ·
[Windows](https://arkapp.ai/ssh-client-windows) ·
[更新日志](https://arkapp.ai/changelog)

> 本仓库只存放文档和公开的问题追踪。Ark 本身是闭源的，因此这里不发布任何应用代码。
> 欢迎在 [Issues](../../issues) 中提交缺陷报告和功能建议。

---

## Ark 是什么

大多数 AI 终端工具会打开一个聊天框，然后等你把背景讲清楚。Ark 直接读取它已经掌握的
上下文：你连接的主机、正在使用的身份、当前目录、运行中的服务、监听端口，以及你刚看到的
那段输出。

当一件事不是一条命令能解决的时候，你只需要说明目标。智能体会在服务器上收集证据、
提出下一步方案、在做出任何改动前等待你确认，然后验证结果。

它本身就是一个完整的 SSH 客户端。即使你从不开启智能体，Ark 依然是一个可以每天使用的终端。

## 功能

- **终端** —— 在同一条真实 SSH 连接上提供 shell 会话、分屏、历史记录和补全。
- **SFTP 文件传输** —— 在终端旁边浏览、上传和下载，不必切换到另一个应用。传输队列
  可以暂停、恢复和重试。
- **服务器状态可见** —— 身份、资源、服务、监听端口和关注项，在你决定做什么之前就能看到。
- **导入 SSH 配置** —— 读取已有的主机设置，地址、用户和认证信息都不用重新录入。
- **主机数量不限** —— 连接的主机数量不受套餐限制。
- **AI 智能体** —— 读取实时服务器状态，跨步骤追踪证据，并且把已验证的结论和尚不确定的
  部分分开呈现。
- **使用你自己的模型密钥** —— 可配置自定义模型，供应商和 API 密钥都掌握在你自己手里。
- **本机经验卡片** —— 任务结束后可以把提炼出的经验保存在本机。加密只存在这台设备上，绑定当前账号和当前主机，只作为调查线索使用。
- **界面语言** —— English、简体中文、日本語。

## 控制权与凭据

让智能体去操作一台真实服务器，前提是边界必须明确。以下是产品固有的行为，而不是
需要你记得去打开的选项：

- 没有你的明确确认，不会发生任何实质性改动，且一次确认只授权你眼前的这一个操作。
- 在改动之前，Ark 会展示服务器、身份、目标对象、完整命令、预期影响，以及结果将如何验证。
- SSH 私钥、密码和你的自定义模型 API 密钥都保留在你的设备上，智能体不会读取它们。
- 你可以随时中止一次运行，改在 CLI 里把工作做完。
- 执行成功、技术验证和业务健康状况会分开报告，所以"命令跑通了"绝不会被说成"问题解决了"。

## 安装

从 [arkapp.ai](https://arkapp.ai/#download) 下载对应系统的安装包。下载需要先登录。

| 平台 | 系统要求 | 安装包 |
| --- | --- | --- |
| macOS | 11（Big Sur）或更高，Apple Silicon 或 Intel | 已签名的磁盘映像 |
| Windows | 10 或更高，x64 | NSIS 安装程序（`.exe`） |

Ark 会检查新版本并支持在应用内完成更新，所以首次安装之后不需要再手动下载。

## 价格

| 套餐 | 价格 | 包含 |
| --- | --- | --- |
| 免费版 | $0 | 登录、SSH / CLI 会话、SFTP 文件传输、主机数量不限、本地历史记录、多设备登录（不含同步） |
| Basic | $1.99 / 月 | 免费版全部功能，智能体与单机驾驶舱，使用自有 API 密钥的自定义模型，本机经验卡片（加密存本机，按主机注入） |
| Pro | $4.99 / 月 | Basic 全部功能。多设备云同步、跨服务器作业、定时任务、MCP 与 Skills 为该档规划能力，当前未交付。 |

在 2026 年 11 月 30 日前注册可获得 Basic 免费试用。未订阅时账号会回到免费版。

## 常见问题

**Ark 是 SSH 客户端还是 AI 助手？**
都是。它是一个可以独立使用的完整 SSH 客户端和终端，同时附带一个在你已连接的服务器上
工作的智能体。

**可以不使用 AI 功能吗？**
可以。免费版涵盖 SSH 和 CLI 会话、SFTP 文件传输、不限数量的主机连接、本地历史记录，以及不含同步的多设备登录。

**我的 SSH 密钥存在哪里？**
存在你自己的设备上。私钥、密码和自定义模型 API 密钥都不会被上传。

**Ark 使用哪些模型？**
你使用自己的 API 密钥，因此供应商和密钥始终属于你。

**支持 Linux 吗？**
暂不支持。目前已发布的目标平台是 macOS 和 Windows x64。

## 反馈与联系

- 缺陷与功能建议：[Issues](../../issues)
- 邮箱：<official@arkapp.ai>
- [服务条款](https://arkapp.ai/#legal-tos) ·
  [隐私政策](https://arkapp.ai/#legal-privacy)

---

Ark 面向全球用户，默认英语，并提供简体中文和日语。不在中国大陆的应用商店推广或上架；官网访问和使用不受限制。
