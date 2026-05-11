# Learn Something

[English](README.md)

一个很小的 agent skill：在等待 agent 回复、命令运行、或者有点无聊的时候，顺手学一点有用的东西。

当你的 AI agent 正在忙，或者你只是想在工作间隙换换脑子，调用这个 skill，它会用一个短故事悄悄讲清楚一个冷门、有用、反直觉的概念。它不是正经上课，也不是冷知识段子，而是给碎片时间准备的小型思想零食。

## 适合谁

适合这些场景：

- 等 agent 回复
- 等长命令跑完
- 工作间隙想休息一下
- 希望 AI 工作区偶尔递给你一个有价值的概念，而不是更多噪音

这个 skill 会从你感兴趣的领域里随机选一个，先讲故事，不提前说出概念名，最后再揭示这个原则，并解释故事如何体现它。

它设计成可移植的 Markdown skill / prompt instruction，适合 Codex、Claude Code、OpenClaw、Hermes，以及其他支持本地 skill、插件或自定义指令的 agent 环境。

关键词：agent skill、AI skill、prompt skill、Codex skill、Claude Code skill、OpenClaw skill、Hermes skill、等待时学习、碎片学习、故事化学习、反直觉概念、冷门原则。

## 安装

任何支持本地 skills、plugins 或可复用 instruction bundles 的 agent 都可以使用这个 skill 文件夹。

Codex 示例：

```bash
cp -R learn-something ~/.codex/skills/learn-something
```

其他 agent 可以按照各自的 skill、plugin 或 custom instruction 机制安装或引用 `learn-something/SKILL.md`。

然后开启新的 agent 会话，调用：

```text
$learn-something
```

## 第一次使用

第一次使用时，skill 会检查：

```text
~/.learn-something/config.json
```

如果文件不存在，它会询问你感兴趣的领域和输出语言，然后保存类似这样的偏好：

```json
{
  "onboardingComplete": true,
  "disciplines": ["心理学", "理财"],
  "language": "中文"
}
```

## 默认领域

心理学、理财、医学、营养学、哲学、美学、商业管理、产品设计、社会学、传播学、教育学。

## License

MIT
