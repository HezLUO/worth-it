# Evaluation Rubric

Use this rubric only when a value-type, disposition, overlap, or evidence-boundary decision remains unclear after the core workflow.

## Evidence Classes

- **Observed fact:** Directly verified in the allowed evidence.
- **Source claim:** Asserted by the material or its publisher but not independently established.
- **Analysis inference:** Derived from stated evidence and explicitly labeled as inference.
- **Disputed:** Contradicted by another decision-relevant allowed source.
- **Unknown:** Not supportable from the allowed evidence.

## Required Distinctions

- **Interesting:** Attention-worthy without implying product relevance.
- **Relevant:** Connected to a current goal, boundary, risk, or evaluation need.
- **Supported:** Backed by allowed evidence appropriate to the claim.
- **Novel:** Not already represented by current capability or decision evidence.
- **Incrementally valuable:** Able to change or improve a product decision, capability, evaluation, risk model, or reference set after overlap is removed.
- **Worth acting on now:** Supported, timely, affordable, and safe enough for the current priority.

## Value Types

- `directly-adoptable`: A sufficiently supported change that fits current priorities and constraints.
- `design-reference`: Reasoning or a pattern that should inform the product but not be copied directly.
- `evaluation-or-comparison-sample`: A useful benchmark, test case, or comparison target.
- `risk-or-negative-example`: A useful unsafe pattern, failure mode, adversarial sample, or example of what not to do.
- `general-inspiration-only`: Interesting material too indirect, weak, or distant to affect a current decision.
- `no-substantive-value`: No meaningful incremental value in the current Product Context.

## Disposition Gates

- `adopt-now`: Require sufficient evidence, concrete incremental value, current-priority fit, acceptable cost, and no unresolved critical risk.
- `evaluate-later`: Require plausible value with a present timing, evidence, cost, dependency, or readiness blocker.
- `retain-as-reference`: Require a useful future design, technical, or comparative reference without present action.
- `retain-as-negative-sample`: Require specific value as an anti-pattern, risk case, or adversarial example.
- `no-action`: Use for irrelevance, duplication without improvement, or no meaningful incremental value.
- `insufficient-evidence`: Use when missing material or Product Context evidence prevents a reliable disposition.

## Adopt-Now Gate

Reject `adopt-now` when any decisive claim lacks sufficient evidence, the incremental delta is unclear, current priority fit is absent, material adoption cost is unacceptable, or a critical risk remains unresolved. Truth, relevance, or novelty alone never opens this gate.

## Insufficient-Evidence Gate

Use `insufficient-evidence` when inaccessible content, missing current capability evidence, conflicting product direction, or another decisive gap prevents a reliable judgment. Name the missing evidence that could change the conclusion. Do not use this disposition when the available evidence already supports `no-action` or another negative judgment.

## Overlap Rule

Treat relevant material that duplicates current capability as having no incremental value unless it supplies a demonstrable improvement, stronger decision-relevant evidence, a new evaluation use, or a material risk insight. Identify the specific duplicated capability before claiming novelty.

## Confidence

- `high`: Allowed evidence directly supports the disposition and no material unresolved gap is likely to change it.
- `medium`: The disposition is supported, but one bounded uncertainty could change timing, type, or action.
- `low`: Evidence is sparse, conflicting, stale, or indirect; state the decisive uncertainty.
