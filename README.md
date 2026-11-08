# claude-agent-evaluation-skill

A Claude Code skill for testing, benchmarking, and improving the reliability of LLM-powered agents.

## Overview

Agent evaluation differs from conventional unit testing because the same input can produce different outputs and many tasks have more than one acceptable solution. This skill helps define behavioral expectations, create representative test cases, measure performance across repeated runs, and identify failure patterns before deployment.

## Main Capabilities

- Define behavioral contracts for agents.
- Design task-based evaluation datasets.
- Measure task completion and reliability.
- Evaluate tool selection and tool execution.
- Assess response quality and constraint adherence.
- Create regression tests for known failures.
- Build adversarial and edge-case test scenarios.
- Compare agent versions and configurations.
- Monitor performance after deployment.

## Evaluation Dimensions

| Dimension | What to measure |
|---|---|
| Task success | Whether the intended outcome was achieved |
| Correctness | Whether the result is factually or technically sound |
| Tool use | Whether the right tools were selected and used correctly |
| Safety | Whether boundaries and permissions were respected |
| Consistency | How much results vary across repeated runs |
| Efficiency | Time, tool calls, and resource consumption |
| Recovery | How well the agent handles errors and interruptions |

## Installation

```bash
git clone https://github.com/Brajesh31/claude-agent-evaluation-skill.git ~/.claude/skills/agent-evaluation
```

## Usage

Invoke the skill when creating an evaluation plan or investigating agent reliability:

```text
/agent-evaluation
```

Provide the agent's intended behavior, available tools, representative tasks, acceptable outcomes, and known failure cases.

## Recommended Evaluation Workflow

1. Define the agent's scope and success criteria.
2. Create a representative set of realistic tasks.
3. Specify acceptable and unacceptable behavior.
4. Include edge cases and adversarial inputs.
5. Run repeated trials with controlled configurations.
6. Measure task outcomes and operational costs.
7. Review failures and classify their causes.
8. Convert important failures into regression cases.
9. Compare versions using the same evaluation conditions.
10. Monitor real-world behavior after deployment.

## Metrics and Reporting

Report distributions and failure rates rather than relying on one successful run. Include sample size, test conditions, model and tool configuration, and confidence limitations.

Avoid optimizing only for a single benchmark score. A system can improve on a test set while becoming less useful in production if the evaluation does not represent real user tasks.

## Repository Contents

- `SKILL.md`: Main agent evaluation instructions and methods.
- `README.md`: Evaluation dimensions, workflow, and reporting guidance.

## Evaluation Checklist

- Test cases represent actual user tasks.
- Expected behavior is documented.
- Repeated runs capture variability.
- Tool calls and side effects are evaluated.
- Safety and permission boundaries are tested.
- Failure cases are retained as regression tests.
- Metrics include task quality and operational cost.
- Benchmark limitations are stated clearly.

## Practical Principle

A benchmark is useful only when it predicts behavior that matters. Prefer a smaller, realistic evaluation suite over a large collection of disconnected tests.
