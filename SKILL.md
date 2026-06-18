---
name: interviewer-designer
description: Generate an interviewer manual from a candidate resume or profile. Use when the user asks how to interview a candidate, verify resume project authenticity, choose assessment directions, design a one-hour interview flow, create technical or soft-skill question pools, generate expected answers, compare candidate answers, score responses, or produce follow-up probes.
---

# Interviewer Designer

## Core Workflow

Use this skill to turn a resume into a practical interviewer manual and, when needed, support live interview evaluation.

1. Confirm the interviewer's assessment direction before designing the interview unless the user already specified it.
   - Hard skills: traditional backend, system design, Agent development, AI Coding, applied AI/algorithm work such as evaluation systems and data flywheels, reliability, observability, architecture governance.
   - Soft skills: collaboration, ownership, communication, personality, technical curiosity, project-driving ability, mentoring or technical influence.
   - Ask for weight and duration only when missing. Default to one hour.

2. Parse the resume into claims.
   - Extract projects, technologies, business outcomes, claimed ownership, role level, team context, and quantified results.
   - Mark high-risk wording: "led", "owned", "from 0 to 1", "improved by X%", "10+ systems", "core architecture", "technical owner".

3. Verify public project evidence when requested or useful.
   - Search company + project + product + technology keywords.
   - Search candidate name + company + technical keywords only when necessary; do not spread phone numbers, email addresses, or other private identifiers.
   - Classify each claim as strong support, partial support, unverifiable, or conflicting.
   - Separate project existence from personal contribution. Never infer personal ownership from a company article.

4. Establish boundaries before technical grilling.
   - First ask for project architecture, candidate-owned modules, non-owned modules, team structure, reporting line, collaboration model,上线/运维 involvement, and decision authority.
   - Ask deep technical questions only within the candidate's claimed ownership boundary.
   - If a module is outside the candidate's boundary, use it only for light collaboration/context checks.

5. Build the one-hour interview plan.
   - Allocate time according to the confirmed directions.
   - Include boundary confirmation, project deep dive, core technical probes, optional design/coding probe, soft-skill probes, and open-ended discussion.

6. Generate a question pool.
   - Include candidate-selected baseline questions and interviewer-selected depth questions.
   - Candidate-selected question answered well is expected. Interviewer-selected question answered well is a positive signal.
   - For each question, include: assessment target, applicable boundary, expected answer, acceptable variants, strong signals, risk signals, follow-ups, and scoring rubric.

7. Support live answer evaluation.
   - When the interviewer provides the candidate's answer, compare it against the expected answer.
   - List matched points, missing points, contradictions, and likely causes.
   - Assign an initial score.
   - Generate a clarifying follow-up based on mismatches.
   - If the candidate gives a coherent tradeoff-based explanation, revise the score upward; if not, keep or lower the score.

8. Use open-ended questions to test concept awareness and technical curiosity.
   - Do not treat open-ended answers as strict correctness checks.
   - Use them to see whether the candidate understands current industry concepts, has thought about common engineering debates, and shows technical interest or pursuit.
   - Good open questions create resonance, disagreement, and tradeoff discussion rather than trivia recall.

## Reference Files

Load only the reference needed for the current task:

- `references/output-template.md`: structure for the final interviewer manual.
- `references/live-scoring.md`: response comparison and rescore workflow.
- `references/technical-question-patterns.md`: reusable probes for backend, Agent, AI Coding, and applied AI.
- `references/open-ended-questions.md`: concept-awareness and technical-curiosity prompts.

## Output Rules

- Be practical for a human interviewer.
- Prefer concrete implementation probes over broad theory.
- Ask for ownership boundaries before assessing implementation depth.
- Do not punish the candidate for implementation details outside their claimed boundary.
- Separate evidence from inference.
- Include expected answers and red flags for critical questions.
- For public research, include links to used sources.
