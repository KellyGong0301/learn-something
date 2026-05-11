# Learn Something

A tiny Codex skill that teaches one obscure, useful, counterintuitive idea through a short story.

The skill randomly picks from your preferred disciplines, tells a story without naming the principle first, then reveals the principle and explains why the story illustrates it.

## Who This Is For

Use this if you want your AI agent to occasionally teach you a useful idea that feels slightly off the beaten path: not trivia, not a textbook intro, but the kind of principle a late graduate student or thoughtful practitioner might know.

Keywords: Codex skill, AI skill, prompt skill, learning prompt, story-based learning, counterintuitive ideas, obscure principles.

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
