# Learn Something

A tiny Codex skill for learning something while you wait.

When your agent is busy, or when you are just a little bored, invoke this skill and get one short story that quietly teaches an obscure, useful, counterintuitive idea. It is meant for the small idle moments between bigger tasks: a lightweight way to pick up a principle you probably would not meet in an intro class.

## Who This Is For

Use this when you are waiting for an agent response, watching a long command run, taking a tiny break, or want your AI workspace to occasionally hand you a worthwhile idea instead of more noise.

The skill randomly picks from your preferred disciplines, tells a story without naming the principle first, then reveals the principle and explains why the story illustrates it.

Keywords: Codex skill, AI skill, prompt skill, learning while waiting, idle learning, story-based learning, counterintuitive ideas, obscure principles.

## Install

Copy the skill folder into your Codex skills directory:

```bash
cp -R learn-something ~/.codex/skills/learn-something
```

Then start a new Codex session and invoke:

```text
$learn-something
```

## First Run

On first use, the skill checks for:

```text
~/.learn-something/config.json
```

If the file does not exist, it asks which disciplines you care about and what language to use. It then saves preferences like:

```json
{
  "onboardingComplete": true,
  "disciplines": ["心理学", "理财"],
  "language": "中文"
}
```

## Default Disciplines

```text
心理学, 理财, 医学, 营养学, 哲学, 美学, 商业管理, 产品设计, 社会学, 传播学, 教育学
```

## License

MIT
