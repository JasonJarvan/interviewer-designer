# Candidate Interview Designer

> **Turn any resume into a one-hour interviewer manual — with evidence-based verification, ownership boundaries, ready-to-ask probes, and live scoring.**
>
> 把一份简历变成可直接开面的一小时面试官手册 —— 公开核实、边界确认、即用题库、现场打分。

[![Skill](https://img.shields.io/badge/type-Agent%20Skill-blue)](#)
[![Compatible](https://img.shields.io/badge/runs%20on-Claude%20Code%20%7C%20OpenAI-green)](#compatibility)
[![License](https://img.shields.io/badge/license-MIT-lightgrey)](LICENSE)

---

## Why this exists

Most interviews fail in predictable ways: the interviewer grills a candidate on code they never owned, takes resume claims (*"led"*, *"from 0 to 1"*, *"improved by 40%"*) at face value, and improvises questions without a rubric. **Candidate Interview Designer** is an agent skill that fixes all three — it reads the resume, separates *evidence from inference*, draws the candidate's real ownership boundary, and hands the interviewer a structured, scorable plan.

## What it does

- **Claim extraction** — parses the resume into discrete claims (projects, tech, outcomes, claimed ownership) and flags high-risk wording.
- **Public verification** — searches company + project + product keywords to classify each claim as *strong / partial / unverifiable / conflicting*, while never spreading private identifiers.
- **Ownership boundaries first** — confirms what the candidate actually owned *before* any deep technical grilling, so they're never punished for code outside their scope.
- **One-hour interview plan** — time-boxed flow: boundary check → project deep dive → core probes → optional design/coding → soft skills → open discussion.
- **Ready-to-ask question pool** — each question ships with assessment target, expected answer, acceptable variants, strong signals, red flags, follow-ups, and a scoring rubric.
- **Live scoring** — compare a candidate's real answer against the expected one, list matches/gaps/contradictions, assign a score, and auto-generate a clarifying follow-up.
- **Open-ended probes** — gauge concept awareness and technical curiosity, not trivia recall.

## Quick start

In **Claude Code** (or any agent that loads skills):

```
Use candidate-interview-designer to turn this resume into a one-hour
interview manual with project verification, ownership-boundary questions,
technical probes, expected answers, live scoring, and follow-up questions.
```

Then attach or paste the candidate's resume. During the interview, paste the candidate's answer to any question to get an instant comparison, score, and follow-up.

## How it works

```
Resume ─▶ Extract claims ─▶ Verify (public) ─▶ Confirm ownership boundary
       ─▶ Build 1-hour plan ─▶ Generate question pool ─▶ Score answers live
```

The skill stays evidence-driven throughout: project *existence* is never confused with personal *contribution*, and every public research result is returned with source links.

## Repository layout

| Path | Purpose |
|------|---------|
| `SKILL.md` | The skill definition and core workflow. |
| `agents/openai.yaml` | OpenAI-compatible agent interface manifest. |
| `references/output-template.md` | Structure for the final interviewer manual. |
| `references/live-scoring.md` | Answer comparison and re-score workflow. |
| `references/technical-question-patterns.md` | Reusable probes (backend, Agent, AI Coding, applied AI). |
| `references/open-ended-questions.md` | Concept-awareness and curiosity prompts. |

## Compatibility

- **Claude Code** — drop the folder into your skills directory; it auto-loads by `name`.
- **OpenAI-style agents** — `agents/openai.yaml` provides the display name, description, and default prompt with implicit invocation enabled.

## Design principles

- Be practical for a **human** interviewer, not academic.
- Prefer concrete implementation probes over broad theory.
- Ask for ownership boundaries before assessing depth.
- Separate evidence from inference — always.

## Contributing

Issues and PRs welcome — new question patterns, language packs, and scoring rubrics especially. Keep contributions practical and bias-aware.

## License

MIT — see [LICENSE](LICENSE).
