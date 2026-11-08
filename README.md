# Agent Evaluation Skill

A practical Claude skill for testing, benchmarking, and improving the reliability of LLM-powered agents. It focuses on evaluating agent behaviour rather than treating an agent like a deterministic function with one expected output.

## What This Skill Covers

- Designing repeatable tests for agent capabilities and task completion.
- Measuring reliability across multiple runs and interpreting result distributions.
- Creating behavioural contracts and regression checks.
- Building adversarial test cases that expose failure modes.
- Recognising benchmark overfitting, flaky results, and data leakage.

## Repository Structure

- `SKILL.md`: The complete skill definition, including capabilities, evaluation patterns, anti-patterns, and common failure modes.
- `LICENSE`: MIT License for this repository.

## When to Use It

Use this skill when building an evaluation plan for an AI agent, comparing agent versions, investigating inconsistent outputs, or deciding whether an agent is ready for production. It is especially useful when a simple pass/fail test cannot capture the quality of an agent's reasoning or actions.

## Evaluation Principles

A single successful run is weak evidence. Evaluate across varied inputs and repeated trials, measure more than one dimension of quality, and include realistic failure conditions. Keep benchmark performance connected to production outcomes so that optimising a score does not hide poor real-world behaviour.

## Getting Started

1. Add the skill to a Claude-compatible skills environment.
2. Invoke it when planning agent tests, benchmarks, or reliability reviews.
3. Define the behaviours and outcomes that matter for the target use case.
4. Run repeated, representative tests and review the resulting patterns.
5. Turn discovered failures into regression tests.

## License

Released under the MIT License. See [LICENSE](LICENSE) for details.
