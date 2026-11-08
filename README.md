# Agent Evaluation Skill

A Claude Code skill for testing, benchmarking, and improving the reliability of LLM-powered agents. It focuses on behavioral evaluation, capability assessment, repeatability, tool-use quality, safety boundaries, regression testing, and production monitoring.

The central principle is that agent quality must be measured across representative tasks and repeated runs. A single successful response or one benchmark score is not enough to establish reliability.

## What This Skill Covers

- Define behavioral contracts and task success criteria.
- Build representative evaluation datasets and test scenarios.
- Measure task completion, correctness, and constraint adherence.
- Evaluate tool selection, execution, and side effects.
- Test safety, permissions, and resistance to adversarial inputs.
- Measure consistency across repeated runs.
- Track latency, token usage, tool calls, and other operational costs.
- Build regression suites from observed failures.
- Compare agent versions and configurations.
- Monitor real-world performance after deployment.

## When to Use It

Use this skill when evaluating a new agent, comparing model or prompt versions, investigating inconsistent behavior, assessing tool-use reliability, creating benchmark tasks, or preparing a production monitoring plan.

It is useful for both pre-release evaluation and ongoing regression testing. It does not replace domain expert review, security testing, or a carefully designed production rollout.

## Installation

Clone the skill into the Claude Code skills directory:

~~~bash
git clone https://github.com/Brajesh31/claude-agent-evaluation-skill.git ~/.claude/skills/agent-evaluation
~~~

Invoke it in Claude Code:

~~~text
/agent-evaluation
~~~

Provide the agent's intended behavior, available tools, representative tasks, acceptable outcomes, constraints, and known failure cases.

## Evaluation Workflow

1. **Define the decision.** State what release, configuration, or remediation decision the evaluation must support.
2. **Write a behavioral contract.** Describe required behavior, forbidden behavior, and acceptable alternatives.
3. **Build a representative task set.** Include common tasks, difficult cases, ambiguity, missing information, and out-of-scope requests.
4. **Set scoring criteria.** Define observable pass conditions and partial-credit rules before running the agent.
5. **Control the test conditions.** Record agent version, model, prompt, tools, temperature or sampling settings, data, and environment.
6. **Run repeated trials.** Capture variability instead of relying on a single response.
7. **Evaluate the complete trace.** Inspect decisions, tool calls, tool results, final output, and side effects.
8. **Classify failures.** Separate reasoning, retrieval, planning, tool, instruction-following, safety, and infrastructure failures.
9. **Compare fairly.** Use the same tasks and conditions when comparing agent versions.
10. **Create regression cases.** Preserve important failures and rerun them after changes.
11. **Review deployment readiness.** Consider quality, risk, latency, cost, and monitoring coverage.
12. **Monitor after release.** Track user outcomes and production failures that the offline evaluation missed.

## Evaluation Dimensions

| Dimension | What to inspect |
|---|---|
| Task success | Whether the intended outcome was achieved |
| Correctness | Factual, technical, or domain correctness |
| Instruction adherence | Whether required constraints and output formats were followed |
| Tool use | Tool choice, arguments, sequencing, and interpretation of results |
| Safety | Permission boundaries, policy constraints, and side effects |
| Consistency | Variation across repeated runs |
| Robustness | Behavior under ambiguity, malformed input, and adversarial cases |
| Recovery | Handling of tool errors, interruptions, and partial failure |
| Efficiency | Latency, token use, tool calls, and compute consumption |

## Scoring and Reporting

Define evaluation rubrics before looking at candidate results. Use observable criteria rather than subjective labels such as "good" or "smart". Report:

- Number of tasks and repeated trials.
- Pass rate and partial-credit distribution.
- Failure categories and severity.
- Variability across repeated runs.
- Tool-call and side-effect errors.
- Latency and resource cost.
- Model, prompt, and tool configuration.
- Important limitations and confidence constraints.

Do not collapse safety-critical failures into an average score. Report them separately. Avoid overfitting an agent to a narrow benchmark at the expense of real user outcomes.

## Included Resources

- [Evaluation plan template](resources/evaluation-plan-template.md): define scope, dataset, metrics, trial design, and release decision.
- [Evaluation case template](resources/evaluation-case-template.md): create reproducible task cases with explicit acceptance criteria.
- [Evaluation report template](resources/evaluation-report-template.md): summarize aggregate outcomes, failure analysis, costs, and limitations.

## Repository Structure

~~~text
claude-agent-evaluation-skill/
├── SKILL.md
├── README.md
├── LICENSE
└── resources/
    ├── evaluation-case-template.md
    ├── evaluation-plan-template.md
    └── evaluation-report-template.md
~~~

## Practical Guidelines

- Prefer realistic tasks over large collections of disconnected synthetic prompts.
- Test both intended triggers and nearby out-of-scope requests.
- Evaluate tool traces and side effects, not only final text.
- Repeat non-deterministic tests and report the number of runs.
- Keep a holdout set for final comparisons.
- Separate safety failures from ordinary quality errors.
- Preserve failing examples as regression tests.
- Report benchmark limitations honestly.

## Source and License Notes

The root LICENSE file contains the repository's declared MIT license for material covered by that license. The current SKILL.md also identifies upstream source material as "vibeship-spawner-skills (Apache 2.0)". The root MIT file does not, by itself, replace or remove license obligations that apply to upstream material. Preserve applicable upstream notices and terms when redistributing that material.

## License

See the root LICENSE file and the source note above for the applicable licensing context.
