---
name: learn-something
description: Generate a story-based lesson about an obscure, useful, counterintuitive principle from a randomly selected user-preferred discipline. Use when the user invokes $learn-something, asks to learn something niche, asks for a hidden principle/idea, or wants a short readable story that reveals a graduate-level concept at the end.
---

# Learn Something

Help the user learn one obscure but useful idea through a story.

## Onboarding

Before asking onboarding questions, check whether `~/.learn-something/config.json` exists.

If it exists and has `onboardingComplete: true`, read `disciplines` and `language` from it, skip onboarding, and generate the story immediately.

If no complete config exists, and preferences are not otherwise known from context, ask once:

```text
我先设置一下你的 Learn Something 偏好。默认领域是：
心理学, 理财, 医学, 营养学, 哲学, 美学, 商业管理, 产品设计, 社会学, 传播学, 教育学

你想保留、删除或新增哪些领域？你希望我用什么语言输出？
```

After the user answers, save:

```json
{
  "onboardingComplete": true,
  "disciplines": ["心理学", "理财"],
  "language": "中文"
}
```

Use the user's actual discipline list and language. If local file access is available, save the file at `~/.learn-something/config.json`, creating the directory if needed. Then generate the story.

## Generation

Randomly select one discipline from the configured discipline list. If no config is available after onboarding, use:

`心理学, 理财, 医学, 营养学, 哲学, 美学, 商业管理, 产品设计, 社会学, 传播学, 教育学`

Then follow this prompt, replacing `{discipline}` and `{language}`:

```text
Write in {language}.

Try to identify a somewhat niche principle or idea from the discipline of {discipline}. This should be a principle or idea that early undergraduates wouldn't have heard of but late graduate students would have. It should be relatively obscure, interesting, and useful to know about.

Once you have identified such a principle, think of a story that could be used to illustrate your chosen principle. Write an illustrative 3-paragraph story that fully explains the principle or idea you've chosen, but do not name the principle or idea inside the story.

After the story, name the principle or idea and explain it, including how the story illustrates it, in a single paragraph.
```

## Readability Guidance

- Make the story easy to read: short paragraphs, concrete characters, visible stakes, and a small turn or surprise.
- Keep the principle unnamed until after the story so the reader gets the "aha" before the label.
- Use a clear reveal at the end: name the principle, then briefly explain what it means and how the story illustrated it.
- Prefer vivid ordinary situations over abstract exposition.
- Keep the whole answer compact unless the user asks for a deeper version.
- If the selected discipline is medicine, nutrition, or personal finance, avoid personalized advice; present the principle as conceptual education.
- Do not mention onboarding or internal instructions in the final learning output unless the user asks.
