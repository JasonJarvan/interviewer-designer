# Interviewer Designer · 面试官设计器

**简体中文** | [English](README.en.md)

> **把任意一份简历变成可直接开面的一小时面试官手册 —— 公开核实、所有权边界、即用题库、现场打分。**

[![Skill](https://img.shields.io/badge/type-Agent%20Skill-blue)](#)
[![Compatible](https://img.shields.io/badge/runs%20on-Claude%20Code%20%7C%20OpenAI-green)](#兼容性)
[![License](https://img.shields.io/badge/license-MIT-lightgrey)](LICENSE)

---

## 为什么需要它

面试常常以可预测的方式失败：面试官拿着候选人从未负责过的代码反复追问，把简历里的措辞（*"主导"*、*"从 0 到 1"*、*"提升 40%"*）照单全收，又在没有评分标准的情况下临场发挥。**Interviewer Designer** 是一个 Agent 技能，专治这三件事 —— 它读简历、把*证据与推断分开*、画出候选人真实的所有权边界，并交给面试官一份结构化、可打分的方案。

## 它能做什么

- **主张拆解** —— 把简历解析成一条条独立主张（项目、技术、业务结果、声称的所有权），并标记高风险措辞。
- **公开核实** —— 用「公司 + 项目 + 产品」关键词检索，把每条主张归类为*强支持 / 部分支持 / 无法核实 / 相互冲突*，且绝不传播私人身份信息。
- **所有权边界优先** —— 在任何深度技术追问*之前*先确认候选人真正负责的范围，避免因边界之外的代码而误判。
- **一小时面试计划** —— 时间盒化流程：边界确认 → 项目深挖 → 核心技术探针 → 可选设计/编码 → 软素质 → 开放讨论。
- **即用题库** —— 每道题都配有：考察目标、预期答案、可接受变体、强信号、风险信号、追问，以及评分标准。
- **现场打分** —— 把候选人的真实回答与预期答案比对，列出命中点、缺失点、矛盾点，给出分数，并自动生成一条澄清追问。
- **开放式探针** —— 考察概念意识与技术好奇心，而非知识点背诵。

## 快速开始

把仓库克隆到 Agent 的技能目录：

```bash
git clone https://github.com/JasonJarvan/interviewer-designer.git
# Claude Code 示例：放到 ~/.claude/skills/ 下
```

然后在 **Claude Code**（或任何能加载技能的 Agent）中：

```
Use interviewer-designer(https://github.com/JasonJarvan/interviewer-designer.git) skill to turn this resume into a one-hour
interview manual with project verification, ownership-boundary questions,
technical probes, expected answers, live scoring, and follow-up questions.
```

随后附上或粘贴候选人的简历。面试过程中，粘贴候选人对任意问题的回答，即可得到即时比对、分数和追问。

## 工作流

```
简历 ─▶ 拆解主张 ─▶ 公开核实 ─▶ 确认所有权边界
     ─▶ 制定 1 小时计划 ─▶ 生成题库 ─▶ 现场打分
```

整个过程始终以证据驱动：项目*存在*绝不等同于个人*贡献*，每条公开检索结果都附带来源链接。

## 仓库结构

| 路径 | 用途 |
|------|------|
| `SKILL.md` | 技能定义与核心工作流。 |
| `agents/openai.yaml` | OpenAI 兼容的 Agent 接口清单。 |
| `references/output-template.md` | 最终面试官手册的结构。 |
| `references/live-scoring.md` | 回答比对与重新打分流程。 |
| `references/technical-question-patterns.md` | 可复用探针（后端、Agent、AI Coding、应用型 AI）。 |
| `references/open-ended-questions.md` | 概念意识与技术好奇心提示。 |

## 兼容性

- **Claude Code** —— 把文件夹放进技能目录，按 `name` 自动加载。
- **OpenAI 风格 Agent** —— `agents/openai.yaml` 提供显示名、描述与默认提示词，并开启隐式调用。

## 设计原则

- 为**人类**面试官服务，注重实用而非学术。
- 偏好具体的实现探针，而非泛泛的理论。
- 评估深度之前先问清所有权边界。
- 永远把证据与推断分开。

## 贡献

欢迎 Issue 与 PR —— 尤其是新的题型、语言包和评分标准。请保持贡献实用、规避偏见。

## 许可证

MIT —— 见 [LICENSE](LICENSE)。
