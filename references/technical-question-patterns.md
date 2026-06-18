# Technical Question Patterns

## Traditional Backend

Probe:

- Data model and state machine.
- Transaction boundaries and consistency.
- Idempotency and duplicate prevention.
- MQ retry, dead letters, backpressure, and ordering.
- Cache key design, invalidation, and stale-data risk.
- Observability, incident response, and rollback.

Expected answer should include concrete tables, states, identifiers, failure modes, and operational signals.

## Agent Development

Probe:

- Entry layer, runtime/gateway, Agent orchestration, tool executor, permissions, state store, audit log.
- Tool/Skill/MCP boundaries.
- User-context injection and server-side authorization.
- Stream events to Web and IM.
- Interrupt, human confirmation, and side-effect compensation.
- Trace replay and dry-run replay.

Strong answers distinguish protocol, framework, platform, and business tools.

## AI Coding

Probe:

- How AI is used across requirement breakdown, code generation, tests, review, migration, and debugging.
- How repository context is supplied.
- How generated code is verified.
- What code should not be delegated to AI.
- How the candidate reviews AI-generated diffs.

Strong answers mention tests, contracts, security review, rollback, incremental changes, and human ownership.

## Applied AI / Evaluation / Data Flywheel

Probe:

- Offline evaluation sets.
- Human labeling and adjudication.
- Golden cases and regression suites.
- Metrics: quality, latency, cost, failure rate, hallucination rate, task completion.
- A/B tests and canary release.
- Feedback capture and data flywheel.
- Prompt/model/workflow versioning.

Strong answers separate model quality, product experience, and business outcome metrics.

## Soft Skills

Probe:

- Cross-functional conflict.
- Ambiguous ownership.
- Driving adoption across multiple business systems.
- Mentoring and code review.
- Handling production incidents.
- Communicating tradeoffs to non-technical stakeholders.
