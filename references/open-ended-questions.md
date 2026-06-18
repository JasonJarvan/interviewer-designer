# Open-Ended Concept and Curiosity Questions

Use these in the final 5-10 minutes. The goal is not strict correctness. Use them to test whether the candidate understands current concepts, has thought about common industry debates, and shows technical interest.

## How to Use

- Ask whether the candidate is willing to discuss a few recent technical topics.
- Pick 2-4 questions relevant to the role.
- Listen for tradeoff reasoning, practical experience, curiosity, and ability to say "I do not know, but my intuition is...".
- Do not over-penalize unfamiliarity unless the concept is central to the role.

## Agent and Platform Questions

- MCP is becoming a common way to connect models with tools and data sources. In an enterprise Agent platform, would you expose internal tools directly as MCP servers, or put an internal tool gateway in front? Why?
- Many Agent products support multi-Agent handoff. In production systems, when do you think multi-Agent is necessary, and when is a single Agent plus tool workflow enough?
- How would you separate frontend tools, backend tools, Skills, MCP tools, and workflow nodes in an enterprise Agent platform?
- What risks matter most when an Agent can trigger real business actions: prompt injection, over-permission, tool misuse, auditability, cost, or user trust?

## AI Coding Questions

- If coding agents can create branches, run tests, and open PRs, what becomes the core value of a senior backend engineer?
- Which parts of backend development are most suitable for AI Coding today, and which parts still need strong human ownership?
- How would you introduce AI Coding into a legacy codebase without causing hidden regressions?

## Applied AI Questions

- Prompt platforms often evolve into workflow or Agent platforms. Which capabilities should stay in code, and which should become configurable products?
- How would you build a quality evaluation system for AI translation, customer support, or code generation?
- What does a useful data flywheel look like for an LLM application? What data should be captured, and what should not be captured?

## Backend and Architecture Questions

- Do you prefer orchestration-based workflows or choreography/event-driven workflows for long-running AI tasks?
- How would you design audit replay for systems where some steps call non-deterministic models?
- Where should business rules live when both humans and AI agents operate the same workflow?

## Reading Signals

Strong signals:

- The candidate connects new concepts to production constraints.
- The candidate distinguishes hype from real engineering value.
- The candidate gives examples, tradeoffs, and failure cases.
- The candidate is comfortable with uncertainty and updates their view.

Risk signals:

- The candidate only repeats buzzwords.
- The candidate treats new frameworks as magic.
- The candidate cannot name risks or operational constraints.
- The candidate shows no curiosity about recent changes in the field.
