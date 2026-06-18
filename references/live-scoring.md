# Live Scoring Workflow

Use this when the interviewer provides a candidate answer during or after the interview.

## Comparison Steps

1. Restate the question and assessment target.
2. Compare the answer to the expected answer.
3. Identify matched implementation details.
4. Identify missing implementation details.
5. Identify contradictions or suspicious claims.
6. Decide whether the gap is severe, moderate, or minor.
7. Generate a follow-up that tests whether the candidate has a coherent reason.
8. Revise the score if the follow-up answer is technically self-consistent.

## Scoring Guidance

- 5: Deep implementation ownership. Explains architecture, edge cases, tradeoffs, incidents, and alternatives.
- 4: Solid practical implementation. Misses some advanced details but handles core risks.
- 3: Plausible participant. Understands flow but lacks depth in failure modes or ownership details.
- 2: Surface-level familiarity. Repeats concepts but cannot explain implementation.
- 1: Incoherent, contradictory, or clearly outside claimed experience.

## Candidate-Selected vs Interviewer-Selected

- Candidate-selected question answered well: expected baseline.
- Candidate-selected question answered poorly: strong risk signal.
- Interviewer-selected question answered well: positive seniority signal.
- Interviewer-selected question answered poorly: evaluate whether it was within the candidate's claimed boundary before penalizing.

## Rescore Rule

If the first answer misses a standard expectation, ask why the candidate chose that design. If the candidate gives a coherent business or technical tradeoff, revise upward. If the answer remains vague, keep or lower the score.

Example:

- Initial answer: "Timeouts are retried three times."
- Follow-up: "If the tool creates a translation task and the first request succeeded but timed out, how do you avoid duplicate tasks?"
- Strong repair: "We use an idempotency key derived from video id, language, batch id, and strategy version; retry returns the existing task id."
- Revised score: raise from 2.5 to 4.
