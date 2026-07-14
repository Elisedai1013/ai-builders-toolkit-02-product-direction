# AI Builders 工具箱 02｜验证 AI 产品方向

把一个“能用”的 AI 产品，变成一个**有明确取舍、能被真实用户验证、知道下一步该改什么**的产品。

<p align="center">
  <a href="https://www.youtube.com/watch?v=lr7jom1NHzg">
    <img src="assets/ai-builders-02-cover-landscape.jpg" alt="AI Builders 解读 02：像导演一样做 AI 产品" width="820">
  </a>
</p>

<p align="center">
  <a href="https://www.youtube.com/watch?v=lr7jom1NHzg">观看原演讲</a> ·
  <a href="skills/ai-builder-director/SKILL.md">查看 SKILL.md</a> ·
  <a href="skills/ai-builder-director/references/method-cards.md">打开完整方法卡</a>
</p>

这个仓库不再只是一组供人复制的提示词，而是一个基于[开放 Agent Skills 标准](https://agentskills.io/)的 Skill。它不绑定某个模型或产品：任何支持 Agent Skills 的工具都可以加载；不支持自动发现 Skill 的 Agent，也可以直接读取其中的工作流和方法卡。

你可以把产品想法、页面截图、可点击原型或真实用户测试记录交给它，让 AI 帮你组织判断与证据；最终的产品取舍仍由 Builder 作出。

## 使用它，你可以完成什么

- 在多个都能做的方案之间，写出一条真正能指导取舍的**产品主心骨**；
- 为首页、新功能入口或 Agent 执行前页面设计**五秒第一印象测试**；
- 把可点击版本变成一次可执行的**真实用户试用排练**；
- 整理多位用户的原话与行为，区分证据、推测和未知；
- 根据证据选择下一步：保留、修改呈现方式，或重新检查产品原则；
- 每轮只改变一个最关键变量，让迭代结果可判断。

它不会替你虚构用户反馈，也不会替 Builder 决定产品的主心骨。

## 适合什么，不适合什么

| 适合 | 不适合 |
| --- | --- |
| 在多个合理方案之间明确取舍 | 让 AI 模拟真实用户并把模拟结果当证据 |
| 为页面或工作流准备真实用户测试 | 用五秒测试代替完整的可用性测试 |
| 整理用户原话、行为和重复模式 | 从一次停顿直接推断用户动机 |
| 根据证据选择下一轮只修改的一项 | 把最终产品原则和价值判断交给 AI |

## 在不同 Agent 中使用

Skill 的核心目录是 [`skills/ai-builder-director`](skills/ai-builder-director)。复制整个目录，而不只是单独复制 `SKILL.md`，这样 Agent 才能按需读取完整的方法卡。为避免破坏已安装版本，Skill 内部调用名仍保留为 `ai-builder-director`；仓库名和展示标题则按它的实际用途命名。

| 使用环境 | 放置位置或安装方式 | 调用方式 |
| --- | --- | --- |
| 支持开放 Agent Skills 的工具 | 项目级通常放在 `.agents/skills/ai-builder-director/` | 直接描述任务或点名 Skill |
| Claude Code | 个人级 `~/.claude/skills/ai-builder-director/`；项目级 `.claude/skills/ai-builder-director/` | `/ai-builder-director` 或自然语言触发 |
| OpenAI Codex | 个人级 `~/.codex/skills/ai-builder-director/` | `$ai-builder-director` 或自然语言触发 |
| 其他 AI Agent | 把整个目录加入 Agent 可读取的上下文，并要求它先读取 `SKILL.md` | 使用下面的自然语言示例 |

在 Codex 中也可以直接说：

```text
请使用 $skill-installer 安装这个 Skill：
https://github.com/Elisedai1013/ai-builders-toolkit-02-product-direction/tree/main/skills/ai-builder-director
```

## 怎么使用

安装或加载后，可以直接描述目标，不需要使用 Codex 专属语法。例如：

```text
使用 AI 产品方向验证 Skill，帮我在这两个产品方案之间写出一条真正能指导取舍的主心骨。
```

```text
使用 AI 产品方向验证 Skill，根据这张首页截图帮我准备五秒第一印象测试。不要模拟用户回答。
```

```text
使用 AI 产品方向验证 Skill，把这个可点击原型变成一场 30 分钟的用户试用观察，并给我记录表。
```

```text
使用 AI 产品方向验证 Skill，整理这 5 位真实用户的测试记录。区分行为、原话和观察者推测，并告诉我下一轮只该验证什么。
```

你也可以让它带你走完整闭环：

```text
使用 AI 产品方向验证 Skill，从产品主心骨开始，带我完成第一印象测试、用户试用和下一轮迭代设计。
```

## Skill 的工作闭环

```text
产品主心骨
    ↓ 决定我们坚持什么、放弃什么
五秒第一印象测试
    ↓ 检查意图第一眼是否被接收
用户试用排练
    ↓ 观察真实使用是否成立
证据整理与下一轮单变量迭代
```

AI 的角色是追问取舍、设计测试、整理证据和暴露未知；真实用户负责提供证据；Builder 负责作出最终决定。

## 这个 Skill 来自哪里

它源自「AI Builders 解读」第二期对 Kim Beverett 在 Config 2026 演讲 *Be the Director: How Stage Craft Informs Product Craft* 的转化与实践。

- [YouTube｜观看原演讲：Be the director: how stage craft informs product craft](https://www.youtube.com/watch?v=lr7jom1NHzg)
- [Config 2026｜查看官方演讲页面](https://config.figma.com/san-francisco/session/8f2835f5-9701-4834-9237-0621882953fa/)
- 演讲者：Kim Beverett，Product Manager at OpenAI

Kim 的核心启发是：当 AI 已经能迅速做出一个“能用”的产品，Builder 更需要像导演一样，有意识地决定用户看见什么、感受到什么，并把真实用户带进反复排练的过程。

本 Skill 将这一思路整理为三个可执行工具：

1. 一句话取舍模板；
2. 五秒第一印象测试；
3. 用户试用观察表。

这三个名称和具体模板是「AI Builders 解读 02」为方便实践而整理的编辑性工具，并不是 Kim Beverett 在原演讲中使用的正式名称。

## 关注微信视频号

<p align="center">
  <img src="assets/wechat-channels-elisedai-qr.jpg" alt="微信视频号 Elisedai在创造 二维码" width="320">
</p>

<p align="center">
  <strong>扫码关注微信视频号：Elisedai在创造</strong><br>
  持续分享 AI Builders 的一手内容、实践解读与可复用工具。
</p>

## 仓库结构

```text
assets/                            # README 宣传图
skills/ai-builder-director/
├── SKILL.md                   # Agent 的触发条件、工作流与边界
├── agents/openai.yaml         # 可选：Skill 在 Codex 中的展示信息
└── references/method-cards.md # 三张工具卡的详细模板与提示词
```

详细方法仍保留在 [`method-cards.md`](skills/ai-builder-director/references/method-cards.md) 中，方便阅读、引用和二次修改。
