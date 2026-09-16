<!--
  Aligned Simplified Chinese copy. 2026-09-08 product decision: do not create
  a separate github.com/arkapp/ark. The currently public git README is already
  used for SEO.

  The three language files carry the same claims, sections, and links; when one
  changes, change all three. Every claim must stay consistent with
  documents/GTM/website/WEBSITE_CONTENT_RATIONALE.md section 5: no unverified
  numbers, no competitor comparisons without a source and a date.
-->

[English](README.md) · **简体中文** · [日本語](README.ja.md)

# Ark — AI 原生的终端与 SSH 客户端

Ark 是一个面向远程服务器的 SSH 客户端和终端，内置的 AI 智能体直接在你已经连上的
那台机器上工作。终端、SFTP 文件传输和服务器状态共用同一条真实连接，因此智能体
从实时事实出发，而不是先让你描述自己的环境。

**macOS 12+（Apple Silicon 与 Intel）· Windows x64 · 提供免费版**

[**下载 Ark**](https://arkapp.ai/#download) ·
[Mac App Store](https://apps.apple.com/app/ark-ssh/id6803574965?mt=12) ·
[智能体能做什么](https://arkapp.ai/ai-ssh-client) ·
[macOS](https://arkapp.ai/ssh-client-mac) ·
[Windows](https://arkapp.ai/ssh-client-windows) ·
[更新日志](https://arkapp.ai/changelog)

> 本仓库只存放文档和公开的问题追踪。Ark 本身是闭源的，因此这里不发布任何应用代码。
> 欢迎在 [Issues](https://github.com/RonkyTang/napoleon/issues) 中提交缺陷报告和功能建议。

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

- 交互式 Agent 的受控改动需要你逐次明确确认；本机定时任务只按你预先保存并授权的范围执行。
- 在改动之前，Ark 会展示服务器、身份、目标对象、完整命令、预期影响，以及结果将如何验证。
- SSH 私钥、密码和你的自定义模型 API 密钥都保留在你的设备上，智能体不会读取它们。局域网配对只在你的设备之间传送，不经过 Ark 云。
- 你可以随时中止一次运行，改在 CLI 里把工作做完。
- 执行成功、技术验证和业务健康状况会分开报告，所以"命令跑通了"绝不会被说成"问题解决了"。

## 安装

从 [arkapp.ai](https://arkapp.ai/#download) 下载对应系统的安装包。中国大陆以外也可从
[Mac App Store](https://apps.apple.com/app/ark-ssh/id6803574965?mt=12) 安装。

| 平台 | 系统要求 | 安装包 |
| --- | --- | --- |
| macOS | 12（Monterey）或更高，Apple Silicon 或 Intel | 官网已签名磁盘映像，或中国大陆以外的 [Mac App Store](https://apps.apple.com/app/ark-ssh/id6803574965?mt=12) |
| Windows | 10 或更高，x64 | NSIS 安装程序（`.exe`） |

官网直装包会检查新版本并支持在应用内完成更新。Mac App Store 版走商店更新。

## 价格

| 套餐 | 价格 | 包含 |
| --- | --- | --- |
| 免费版 | $0 | 登录、SSH / CLI 会话、SFTP 文件传输、主机数量不限、本地历史记录、多设备登录（不含同步） |
| Basic | $1.99 / 月 | 免费版全部功能，智能体与单机驾驶舱，使用自有 API 密钥的自定义模型，本机经验卡片（加密存本机，按主机注入） |
| Pro | $4.99 / 月 | Basic 全部功能，加上本机定时任务，以及经局域网与桌面配对的 iOS / Android 配套客户端（浏览、上传、传输、预览远端图片和视频、确认后删除）。iOS 尚未在 App Store 列出。Android 不上 Google Play，官网 APK 尚未发布。多端设备数据同步、跨服务器作业、MCP 与 Skills 仍为规划。 |

2026 年 11 月 30 日前注册的账号可获得活动 Basic 权益。活动不会自动续费或扣款；活动结束时没有付费订阅的账号会回到 Free。

付费套餐按月计费，默认自动续费，可随时取消；取消后当期仍有效，到期回到 Free。官网和直装版付款由 Stripe 处理；Mac App Store 版按 Apple 商店规则办理，价格以商店显示为准。模型费用由你与模型服务商结算，不计入 Ark 套餐。

## 常见问题

**Ark 是 SSH 客户端还是 AI 助手？**
都是。它是一个可以独立使用的完整 SSH 客户端和终端，同时附带一个在你已连接的服务器上
工作的智能体。

**可以不使用 AI 功能吗？**
可以。免费版涵盖 SSH 和 CLI 会话、SFTP 文件传输、不限数量的主机连接、本地历史记录，以及不含同步的多设备登录。

**我的 SSH 密钥存在哪里？**
存在你自己的设备上。私钥、密码和自定义模型 API 密钥都不会被上传。局域网配对只在你的设备之间传送，不经过 Ark 云。

**Ark 使用哪些模型？**
你使用自己的 API 密钥，因此供应商和密钥始终属于你。

**支持 Linux 吗？**
目前没有 Linux 桌面客户端；你可以在 macOS 或 Windows 上使用 Ark，通过 SSH 连接 Linux 服务器。macOS 也可在中国大陆以外的 Mac App Store 获取。Pro 含 iOS / Android 配套客户端，经局域网与桌面配对；iOS 商店尚未列出；Android 不上 Google Play，官网 APK 尚未发布。

**如何订阅和取消？**
付费套餐按月计费，默认自动续费。可随时取消；取消后当期仍有效，到期回到 Free。官网和直装版付款由 Stripe 处理；Mac App Store 版按 Apple 商店规则办理。模型费用由你与模型服务商结算。

## 反馈与联系

- 缺陷与功能建议：[Issues](https://github.com/RonkyTang/napoleon/issues)
- 邮箱：<official@arkapp.ai>
- [服务条款](https://arkapp.ai/#legal-tos) ·
  [隐私政策](https://arkapp.ai/#legal-privacy)

---

Ark 面向全球用户，默认英语，并提供简体中文和日语。不在中国大陆的应用商店推广或上架；官网访问和使用不受限制。
