# 观心：觉察与松开执念

一个中文、纯指令的 Agent Skill。通过一次一个问题的温和对话，帮助你看清情绪、区分事实与解释、探索“非如此不可”的要求，并选择一个具体行动。

**调用名：`loosen-attachment`**

## 它如何工作

1. **觉察**：从一件具体事件和当下感受开始。
2. **退一步**：分清可观察的事实、脑中的解释和真实感受。
3. **照见**：了解你在乎什么，不强行把所有情绪归结为执念。
4. **松开**：保留合理愿望与边界，尝试松动僵硬的绝对要求。
5. **行动**：选择沟通、核实、争取、设边界、休息等一个小行动。

每轮通常两至五句话，只问一个问题；可以跳步、暂停或结束。成功不是“情绪归零”，而是更清楚、多一点选择。

## 文件

- [SKILL.md](SKILL.md)：完整行为、触发条件、对话流程和安全边界。
- [README.md](README.md)：安装与使用说明。

没有脚本、外部服务、API 密钥或运行依赖。

## 在本地 Codex 使用

先确认已安装支持 Agent Skills 的 Codex。下面的命令适用于 macOS / Linux，仅下载 skill 文件，不运行安装脚本：

```bash
mkdir -p "$HOME/.agents/skills"
git clone https://github.com/d-wwei/loosen-attachment.git "$HOME/.agents/skills/loosen-attachment"
```

如果目标目录已经存在，请先检查内容，不要盲目覆盖。也可以手动下载本仓库，将 `SKILL.md` 放到 `~/.agents/skills/loosen-attachment/SKILL.md`。

在 Codex CLI / IDE 扩展中用 `/skills` 查看，或在提示词中明确调用：

> 用 $loosen-attachment 帮我看一件放不下的事，一次问一个问题。

只用于某个项目时，可改放到该项目的 `.agents/skills/loosen-attachment/SKILL.md`。

以上发现路径与调用方式依据 [OpenAI 官方 Build skills 文档](https://learn.chatgpt.com/docs/build-skills)，核对日期：2026-10-29；具体可用性以你的客户端和工作区设置为准。

## 在 ChatGPT 使用

支持独立 skills 的 ChatGPT 桌面应用可在 Skills 界面查看可用项，并通过 `@` 选择。**发布到 GitHub 或下载文件，不等于已安装进你的 ChatGPT 账号或本地客户端。** 若当前应用中没有此 skill，可将 `SKILL.md` 作为当前对话的指令材料并明确请求使用；这不代表永久安装。

本仓库是独立 skill 源文件，不是已发布到插件目录的插件。跨 Chat / Work 等产品面的安装与分发方式请查阅 [官方说明](https://learn.chatgpt.com/docs/build-skills)。

## 示例

以下为通用示例，不是真实对话记录：

- “用 loosen-attachment 帮我梳理一件反复纠结的事，一次问一个问题。”
- “我想复盘今天的情绪，但不要替我下结论。”
- “今天先不分析了，帮我整理已知信息，选一个小行动。”

普通抱怨或现实问题求助，不应自动触发内观。

## 边界与隐私

- 不是心理治疗、诊断或危机干预服务，不承诺根除执念或让情绪消失。
- 不要求放弃合理诉求、宽恕伤害或忍受危险；现实安全优先。
- 不主动挖掘创伤，不把不同意见解释为抗拒。
- 仅在用户要求时整理或保存记录；不承诺跨会话记忆，也不自动设置提醒。
- 仓库不含私人经历、聊天记录或凭证。Skill 本身没有保存、上传数据的代码，但对话仍由所用平台按其设置和政策处理；不要把敏感复盘提交到公开仓库或 issue。
