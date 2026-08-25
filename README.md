# 引导式个人解梦 Skill

一个通过针对性追问帮助用户理解个人梦境的 Codex Skill。它结合梦中的情绪、个人联想，以及梦与现实经验之间的相似、反差或缺席，形成一份有依据、深入且贴近个人经验的解梦报告。

它不套用固定的梦境符号词典，也不把梦境解释成人格诊断或医学结论。

## 整体流程

1. 完整听取并保留用户的梦境原话。
2. 从最有力量的画面、情绪、关系或反常之处开始追问。
3. 结合个人联想与现实经验形成可修正的主要理解。
4. 在材料足够并完成核对后，生成约 800–1200 字的完整解梦报告。
5. 询问用户是否希望把梦境整理成可保存的「梦境手记」。
6. 用户同意后，直接交付独立梦境图 PNG 和完整梦境手记 PNG。

## 安装

### 使用 Skill Installer

在 Codex 中调用 `$skill-installer`，并提供本仓库地址：

```text
https://github.com/yangqiandun/guided-dream-interpretation-skill
```

### 手动安装

克隆或下载仓库后，将整个目录放入：

```text
~/.codex/skills/guided-dream-interpretation
```

完成后重新打开 Codex，使 Skill 被重新加载。

## 使用

可以直接分享梦境并要求解读，或显式调用：

```text
$guided-dream-interpretation
```

例如：

- “我昨晚做了一个梦，想和你一起理解它。”
- “帮我分析这个梦，但不要直接套梦境符号词典。”
- “这个梦让我醒来后仍然很难受，我想知道它可能和什么有关。”

## 目录

```text
guided-dream-interpretation/
├── SKILL.md
├── README.md
├── LICENSE
├── assets/
│   └── dream-note-template.html
└── references/
    ├── questioning-method.md
    ├── report-method.md
    ├── dream-note-method.md
    └── golden-cases.md
```

## 文件职责

- `SKILL.md`：定义触发范围、工作流与硬边界。
- `references/questioning-method.md`：定义追问节奏、选项使用、推断方式与解读边界。
- `references/report-method.md`：定义报告依据、分析深度、文字结构与完成格式。
- `references/dream-note-method.md`：定义梦境图提示词、模板填充、图片生成与交付。
- `references/golden-cases.md`：提供一个匿名化案例，用于校准追问节奏、心理推演和报告深度。
- `assets/dream-note-template.html`：内部渲染模板，用于把梦境图、梦境原文和完整报告生成一张竖向长图。

## 边界

- 不使用脱离个人经验的固定意象释义。
- 不做心理、人格或医学诊断。
- 用户否定某个方向或要求停止时，不强行继续。
- 用户没有请求时，不擅自提供行动建议。
- 梦境手记只在用户明确同意后生成。

## License

MIT
