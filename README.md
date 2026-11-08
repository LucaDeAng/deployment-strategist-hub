# deployment-strategist-hub

**Open tools, templates and reading for people who take AI agents from demo to production:**
deployment strategists, forward deployed engineers, and the CX and ops leads who work with them.

The templates are CC BY 4.0 and the linked code is MIT, so everything is free to reuse. Questions,
failure stories and new assets go in
[Discussions](https://github.com/LucaDeAng/deployment-strategist-hub/discussions). Posting needs only a
GitHub account; there is no newsletter and nothing to buy. The web version is at
[genai4business.com/hub](https://genai4business.com/hub).

The examples use Brezzaluce Energia, a fictional Italian utility, so every asset can be read,
run and changed without touching real customer data.

## Assets you can run

| Asset | Use it when | Start here |
|---|---|---|
| [deployment-in-a-box](https://github.com/LucaDeAng/deployment-in-a-box) | You need a harness for a phone agent before you have real traffic: MCP back office, simulated callers, KPI tree with a safety gate | `uv sync && uv run pytest -q`, then `uv run python -m deployment_in_a_box.simulate --fault-rate 0.2 --seeds 5 --out runs/faults.jsonl` |
| [transcript-regression-kit](https://github.com/LucaDeAng/transcript-regression-kit) | A prompt change keeps breaking things that used to work, and you want annotated conversations to become CI tests | `pip install -r requirements.txt && python -m t2r.run --agent mock-v1` |
| [ai-to-ai-call-lab](https://github.com/LucaDeAng/ai-to-ai-call-lab) | Customers' AI assistants start calling your voice agent, and you need to decide what to let them do | `uv sync && uv run python -m ai_to_ai_call_lab.simulate` |
| [spoken-entities-it](https://github.com/LucaDeAng/spoken-entities-it) | Your voice agent captures codes, IBANs or readings by voice, and you need to know how often a misheard value gets through | `uv sync && uv run python -m spoken_entities.score` (no keys) |
| [agent-business-case](https://github.com/LucaDeAng/agent-business-case) · [web calculator](https://genai4business.com/tools/business-case) | Someone asks whether the agent pays back, and under per-minute or per-resolution pricing | `npm test && npm run example`, or open the calculator |

Each repo has a matching case study at [genai4business.com/work](https://genai4business.com/work)
with its limits and what I would do differently.

## Templates

Copy them into your own repo or doc. Each one is a page, and each section asks a question a
deployment review will ask anyway.

- [**Failure-first case study**](templates/case-study.md): Problem, Constraints, Architecture, What
  I did, What broke, What I would do differently. The format I use for case studies on the site.
- [**Ten-minute decomposition**](templates/decomposition.md): turn a first-meeting ask ("can the bot
  handle billing disputes?") into outcomes, the metric that hides them, systems and owners, risks and
  the cheapest first move.
- [**Evaluation plan**](templates/eval-plan.md): outcomes that cost money, pass^k over repeated trials,
  a judge checked against human labels, held-out data, pinned versions, results by category.
- [**Go-live checklist**](templates/go-live-readiness.md): the thresholds between lab, shadow, pilot
  and gradual rollout for a voice or chat agent, and the checks that block a release, AI disclosure
  included.

## Reading

Short list, one line on why each matters. Proposals welcome in Discussions.

- [τ-bench](https://arxiv.org/abs/2406.12045) (Sierra, 2024): tool-using agents tested against
  simulated users and domain policies, and the pass^k metric for reliability over repeated trials.
  The [benchmark repo](https://github.com/sierra-research/tau2-bench) has since moved to a 2.0
  release whose scores are not comparable with 1.x.
- [τ²-bench](https://arxiv.org/abs/2506.07982) (Sierra, 2025): the user can act on the shared state
  too, as in tech support, which changes what an agent has to coordinate.
- [τ-Entity](https://sierra.ai/blog/tau-entity-can-voice-agents-get-the-details-right) (Sierra,
  October 2026) and its paper [τ-Elicitation](https://arxiv.org/abs/2609.13602): can voice agents
  capture, verify and repair names, numbers and codes over a call, in six languages. Italian is not
  among the six.
- [The Agent Development Life Cycle](https://sierra.ai/blog/agent-development-life-cycle) (Sierra,
  2024): how a deployed agent is built, tested, released and improved as a loop, and who owns each
  step.
- [Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
  (Anthropic, January 2026): start from 20 to 50 tasks drawn from real failures, and use pass^k when
  customers meet the agent every time.
- [Your AI product needs evals](https://hamel.dev/blog/posts/evals/) (Hamel Husain, 2024): look at
  the data, write targeted checks for the failures you actually see, and keep a person reading
  transcripts. Its follow-up on [LLM judges](https://hamel.dev/blog/posts/llm-judge/) covers checking a
  judge against human labels.

## Community

Use [Discussions](https://github.com/LucaDeAng/deployment-strategist-hub/discussions) for:

- **Q&A**: a deployment question you are stuck on (scoping, evals, rollout, vendors, pricing);
- **Show and tell**: a failure you found and how you found it, or an asset you built on one of these
  (there is a form for failure stories);
- **Ideas**: a template or a test you wish existed.

Please anonymise: no employer or client names, no customer data, ranges instead of internal figures.
See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Templates and text: [CC BY 4.0](LICENSE). The linked repos are MIT, each with its own license file.

Maintained by [Luca De Angelis](https://genai4business.com).
