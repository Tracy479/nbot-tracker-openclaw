# Skill 包说明

## 包内文件

当前 `nbot-tracker.skill` 包内可以看到这些主要文件：

- `SKILL.md`
- `scripts/setup-tracker.sh`
- `references/nbot-format.md`
- `references/platform-setup.md`

## 这个包的作用

这个 skill 的目标，是把指定 `nbot tracker` 的内容交给 OpenClaw 处理，并推送到 iMessage。

README 里介绍的是项目层面的用途，这份文档主要补充包内结构，方便快速查看交付内容。

## 当前已验证流程

目前已经跑通的链路是：

1. 提供 `nbot tracker` 链接
2. 由 OpenClaw 读取和处理内容
3. 按预设格式输出
4. 推送到 iMessage

## 交付形式

仓库中的主要交付物就是 `nbot-tracker.skill`。
它适合直接导入、分享和复用，也更符合 OpenClaw 中 skill 的实际使用方式。

## 后续可继续补充的内容

- 示例输入
- 更详细的配置说明
- 其他消息通道的接入说明
- 解包后的文件镜像，用于二次阅读或继续维护
