# Evaluation plan

Write this before the first run. Most broken evaluations are broken in the plan: the outcome
that costs money is not scored, the test data shapes the result, or the system is tuned on the
data it is graded on. Examples of each, found and fixed in public:
[spoken-entities-it](https://github.com/LucaDeAng/spoken-entities-it) and
[ai-to-ai-call-lab](https://github.com/LucaDeAng/ai-to-ai-call-lab).

## 1. Decision

What will you decide with these numbers (ship, pick a model, change a prompt, add a check), and
what result would change that decision? If no result would, skip the evaluation.

## 2. Outcomes, by what they cost

Score outcomes, not accuracy. A typical split for an agent that captures a value or takes an action:

| Outcome | Meaning | Cost |
|---|---|---|
| correct | right, and the agent is sure | none |
| re-ask | no value, unsure (even if right), or rejected by a check | a turn |
| silent wrong | wrong, accepted, acted on | a complaint, a rebill, a breach |

Count "unsure but right" as a re-ask: the agent asks again either way.

## 3. Test data

- Where it comes from (production sample, synthetic, simulated callers) and what that cannot show.
- Listen to or read one example of each pattern before generating hundreds; synthetic values can
  make a benchmark hard or easy for reasons that are not the system.
- A held-out set nobody tuned on, even a small one. Say which numbers come from tuned data.

## 4. Repeated trials

Agents are not deterministic. Run each case k times and report pass^k (passes in all k trials)
next to the average, as in [τ-bench](https://arxiv.org/abs/2406.12045). Keep every trial's
failures, not just the first, so you can tell a stable failure from noise.

## 5. Checks

- Deterministic checks first (tool called, field present, checksum valid, words allowed).
- An LLM judge only where a rule cannot decide. Make it pass/fail, not 1–5. Label about 100 cases by
  hand and report agreement on passes and on fails separately (true-positive and true-negative
  rates): overall agreement hides misses on rare failures. Re-check it after any model change
  ([guide](https://hamel.dev/blog/posts/llm-judge/)). A judge that passes on a keyword is a finding.
- Zero tolerance where it matters (safety, privacy, emergencies): one failure blocks.

## 6. Versions and cost

Pin the model ids, settings, prompt hash, recogniser and date in the report. Write down what one
run costs (calls, characters, minutes) so someone else can decide whether to repeat it.

## 7. What the numbers do not say

Report results by category (intent, entity type, safety tag), not only the average: a release gate is
per category, and an average hides the category that fails.

Sample size and correlation (three channels of the same recording are not three samples), the
interval on a zero ("0 of 384" from 128 distinct recordings is not "never"), and the gap between
your data and real callers.
