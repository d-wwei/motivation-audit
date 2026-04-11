# Motivation Audit | 正心诚意

A cognitive base that audits the motivational drivers behind cognition before analysis begins. Works with any LLM agent -- Claude, GPT, Gemini, or custom frameworks.

在分析开始之前，先审计驱动认知的动机。适用于任何 LLM agent -- Claude, GPT, Gemini 或自定义框架。

---

## What it does | 它做什么

Most AI agents (and humans) jump straight to analyzing a problem. Motivation Audit adds a prior step: examine WHY you're analyzing this problem, because impure motivation unconsciously distorts information processing -- what you notice, what you ignore, what you conclude.

大多数 AI agent（和人类）直接跳入问题分析。正心诚意增加了一个前置步骤：审视你为什么要分析这个问题，因为不纯的动机会无意识地扭曲信息处理——你注意到什么、忽略什么、得出什么结论。

### Before (default agent) | 安装前

> "I think we should reorganize the team."
>
> "Here's a team reorganization plan: assess current structure, identify inefficiencies, design new reporting lines, create a transition timeline..."

### After (with Motivation Audit) | 安装后

> "Before planning: what's driving this reorganization impulse? Is it that certain people aren't delivering (performance problem, not structure problem)? Is it that you want different people reporting to you (power motivation)? Or is there genuine structural friction causing work to stall? The reorganization plan looks completely different -- or disappears entirely -- depending on which driver is actually at work."

---

## Core insight | 核心洞察

**Motivation purity directly determines judgment quality.** Self-interested motivation doesn't just bias the conclusion -- it unconsciously distorts the entire information processing pipeline: what data you seek, how you weight evidence, which alternatives you consider, and what risks you dismiss.

**动机纯度直接决定判断质量。** 自利的动机不仅偏置结论——它无意识地扭曲整个信息处理管道：你寻找什么数据、如何权衡证据、考虑哪些替代方案、忽略哪些风险。

This is deeper than frame-auditing. Frame-auditing asks "am I using the right cognitive tool?" Motivation Audit asks "what is driving me to pick up any tool at all?"

这比框架审计更深。框架审计问"我用的认知工具对不对？" 正心诚意问"是什么驱动我去拿起任何工具？"

---

## How it works | 工作原理

**One cognitive shift** applied before every analysis:

一个认知转换，在每次分析之前应用：

| Default mode | Target mode |
|---|---|
| Analyze the problem 分析问题 | First audit WHY I'm analyzing this problem, then analyze 先审计为什么要分析这个问题，再分析 |

**Three audit questions** (the motivation check):

三个审计问题（动机检查）：

1. **What am I hoping the conclusion will be?** If you already have a preferred answer, your analysis is advocacy, not inquiry.
2. **Who benefits from my recommended action?** If the primary beneficiary is you, apply extra scrutiny.
3. **What would I recommend if my personal stakes were zero?** The delta between this answer and your actual recommendation is the distortion from motivation.

**Five anti-patterns** that catch motivation failures:

五个反模式，捕捉动机失败：

| Anti-pattern 反模式 | Description 描述 |
|---|---|
| Motivation blindness 动机盲区 | Never questioning your own motivation, assuming you're always objective 从不质疑自己的动机，假设自己永远客观 |
| Motivation paralysis 动机瘫痪 | Over-auditing motivation until unable to act 过度审计动机直到无法行动 |
| Pseudo-altruism 伪利他 | Wrapping self-interested decisions in "for their benefit" language 用"为了他们好"的语言包装自利决策 |
| Selective auditing 选择性审计 | Only auditing motivation on low-stakes decisions, skipping on high-stakes ones 只在低风险决策审计动机，高风险时跳过 |
| Capability-without-direction 有能无向 | Developing skills without examining what drives their application 发展能力却不审视驱动其应用的动机 |

---

## Theoretical foundation | 理论基础

Built on converging insights from Eastern philosophy:

- **Inamori Kazuo's 以心为本**: Motivation purity directly determines judgment quality. Self-interested motivation unconsciously distorts information processing.
- **Inamori's altruism-as-cognitive-tool**: Replacing "what do I gain?" with "what does the other party gain?" as the first question automatically completes a perspective switch.
- **Inamori's life equation**: Mindset (including motivation direction) is a -100 to +100 multiplier -- wrong direction means greater capability creates greater damage.
- **Mencius' 反求诸己**: When results are unsatisfactory, first ask "has my motivation drifted?"
- **Wang Yangming's 致良知**: When your judgment errs, it's often not missing information but internal calibration disturbed by desire/bias.
- **The Great Learning (大学) 正心诚意**: Rectifying the mind and making intentions sincere as prerequisites for investigating things (格物致知).

The cognitive protocol strips all theory and translates these ideas into executable instructions for any reasoning agent.

认知协议剥离了所有理论，将这些思想转译为任何推理 agent 可执行的指令。

---

## Installation | 安装

### Claude Code
```bash
cp cognitive-protocol.md ~/.claude/motivation-audit.md
echo '@~/.claude/motivation-audit.md' >> ~/.claude/CLAUDE.md
```

### Codex
```bash
cat cognitive-protocol.md >> AGENTS.md
```

### Gemini
Paste `cognitive-protocol.md` into `system_instruction`.

将 `cognitive-protocol.md` 内容粘贴到 `system_instruction` 中。

### Cursor
```bash
cat cognitive-protocol.md >> .cursorrules
```

### Any agent | 任何 agent
Inject `cognitive-protocol.md` (~30 lines) into the system prompt. See [`install/generic.md`](install/generic.md) for details.

将 `cognitive-protocol.md`（约 30 行）注入系统提示词。详见 [`install/generic.md`](install/generic.md)。

---

## File structure | 文件结构

```
motivation-audit/
├── README.md                  <- You are here / 你在这里
├── cognitive-protocol.md      <- Core rules (~30 lines, always-on) / 核心规则（约 30 行，始终激活）
├── SKILL.md                   <- Full framework reference / 完整框架参考
├── anti-patterns.md           <- Detailed anti-pattern guide / 反模式详解
├── examples.md                <- Before/after scenarios / 前后对比示例
└── install/
    ├── claude-code.md         <- Claude Code installation / Claude Code 安装指南
    ├── codex.md               <- Codex installation / Codex 安装指南
    ├── gemini.md              <- Gemini installation / Gemini 安装指南
    └── generic.md             <- Universal guide / 通用安装指南
```

---

## Composability | 可组合性

Motivation Audit is a **cognitive base** -- it changes what drives the agent's reasoning, not what it produces. It stacks cleanly with any domain skill and any other cognitive base because it operates at the deepest layer: before reasoning even begins.

正心诚意是一个**认知底座**——它改变驱动 agent 推理的动力，而非产出内容。它与任何领域技能和其他认知底座无冲突地叠加，因为它运行在最深层：推理开始之前。

### Relationship to other cognitive bases | 与其他认知底座的关系

| Layer 层级 | What it governs 管辖范围 | Example 示例 |
|---|---|---|
| **Motivation Audit 正心诚意** | WHY you reason -- the drivers behind cognition 你为什么推理——认知背后的驱动力 | "Am I recommending this because it's right, or because I benefit?" 我推荐这个是因为它正确，还是因为我受益？ |
| [Frame Auditing](https://github.com/d-wwei/frame-auditing) 框架审计 | HOW you reason -- the cognitive tools you use 你怎么推理——你使用的认知工具 | "Is this the right frame for this problem?" 这是解决这个问题的正确框架吗？ |
| [First Principles](https://github.com/d-wwei/first-principles) 第一性原理 | WHAT you reason from -- the foundations 你从什么出发推理——基础 | "Are these assumptions verified or inherited?" 这些假设是验证过的还是继承的？ |

Loading order: Motivation Audit first (audit drivers), then Frame Auditing (audit tools), then First Principles (audit foundations). Combined: reasoning that is driven by the right motives, using the right frames, built on verified foundations.

加载顺序：正心诚意优先（审计驱动力），然后框架审计（审计工具），然后第一性原理（审计基础）。组合效果：由正确动机驱动、使用正确框架、建立在经过验证的基础上的推理。

---

## License

MIT
