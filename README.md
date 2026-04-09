# nbot tracker OpenClaw

基于 OpenClaw 的信息推送 Skill，用于读取指定 `nbot tracker` 的更新内容，并按预设格式定时推送至 iMessage。当前已完成从 tracker 到 iMessage 的端到端流程验证。

## 项目概述

这个项目源于一个很具体的使用场景：希望把 `nbot tracker` 中持续更新的信息自动整理后，定时发送到消息端，而不是手动反复查看。为此，我基于 OpenClaw 整理并打包了一个可复用的 Skill，用于实现信息读取、内容整理与消息推送的自动化流程。

## 核心流程

该 Skill 的核心流程如下：

1. 接收指定的 `nbot tracker` 链接
2. 读取 tracker 中的更新内容
3. 按预设格式整理输出
4. 通过 OpenClaw 定时推送至 iMessage

## 我在项目中的工作

在这个项目中，我主要完成了以下工作：

- 明确信息推送场景与使用需求，确定从 tracker 到消息端的自动化流程
- 基于 OpenClaw 整理并打包可导入的 Skill 文件
- 设计内容输出格式，使推送结果更适合消息场景阅读
- 完成从 `nbot tracker` 到 iMessage 的实际跑通与验证
- 对项目结构与使用方式进行文档化整理，并撰写配套说明内容

## 当前验证状态

当前已验证通过的场景包括：

- **输入来源：** `nbot tracker`
- **调度与执行：** OpenClaw
- **消息目标：** iMessage
- **当前状态：** 已完成完整推送链路验证

## 仓库内容

本仓库当前主要包含：

- `nbot-tracker.skill`：可导入 OpenClaw 的 Skill 文件
- `docs/package-overview.md`：补充说明文档
- `README.md`：项目说明文档

## 使用方式

1. 将 `nbot-tracker.skill` 导入 OpenClaw
2. 提供需要跟踪的 `nbot tracker` 链接
3. 配置消息通道并确认 iMessage 可用
4. 运行流程或设置定时任务
5. 等待更新内容按预设方式推送到指定消息端

## 当前限制

- 当前验证通过的主要场景为 iMessage 推送
- 运行依赖 OpenClaw 环境及消息通道配置
- 仓库中不包含运行时凭证或个人配置
- 若扩展到其他消息通道，仍需在 OpenClaw 侧完成相应配置

## License

MIT License
