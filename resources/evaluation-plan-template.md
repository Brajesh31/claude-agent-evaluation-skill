# Agent Evaluation Plan

Use this plan before running a benchmark or release evaluation. Define success criteria and evaluation conditions before reviewing candidate results.

## Evaluation Identity

- **Evaluation ID:**
- **Owner:**
- **Date:**
- **Agent name and version:**
- **Decision to support:** release / compare / investigate / monitor / other

## Scope

- **Intended agent responsibility:**
- **In-scope tasks:**
- **Out-of-scope tasks:**
- **Target users and environment:**
- **Expected tool access:**
- **Critical safety or permission boundaries:**

## Evaluation Dataset

- **Dataset name and version:**
- **Number of task cases:**
- **Task categories:**
- **Data source and licensing:**
- **Sensitive data removed or protected:**
- **Train / development / holdout separation, if applicable:**
- **Known coverage gaps:**

## Test Conditions

- **Model and version:**
- **System prompt / agent revision:**
- **Tools and permissions:**
- **Sampling settings:**
- **Runtime environment:**
- **Maximum trials per case:**
- **Timeout and retry policy:**
- **Logging and trace retention:**

## Metrics and Acceptance Criteria

| Metric | Definition | Minimum / target | Critical? |
|---|---|---|---|
| Task success | | | |
| Correctness | | | |
| Instruction adherence | | | |
| Tool-use correctness | | | |
| Safety boundary compliance | | | |
| Latency / cost | | | |
| Repeatability | | | |

Document pass, partial-pass, and fail conditions. Define critical failures that cannot be averaged away.

## Trial Design

- **Repeated runs per case:**
- **Randomization or ordering approach:**
- **Human review process:**
- **Reviewer calibration approach:**
- **Disagreement resolution:**
- **Statistical summary to report:**

## Release Decision

- **Required thresholds met:**
- **Critical failures observed:**
- **Known limitations:**
- **Mitigations required:**
- **Decision:** approve / conditional / reject
- **Reviewer and date:**
