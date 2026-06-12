# Measurement Framework

This document describes the measurement concepts used by the AI Half-Life project.

## Measurement philosophy

The project is intentionally conservative. It separates what is observed from what is inferred.

A deployment case is not counted as verified unless a public source reports that the AI system was deployed or piloted in a real operational setting and reports at least one measurable post-deployment outcome.

Candidate cases are tracked separately until they can be validated.

## Core metrics

### Value Realization Ratio

Value Realization Ratio compares realized value to projected or baseline value.

```text
VRR = Realized Value / Projected Value
```

If projected annual value was $1,000,000 and realized annual value is $600,000, the VRR is 0.60.

VRR is useful because it focuses on the gap between promise and realized outcome.

### Adoption Retention Ratio

Adoption Retention Ratio compares current active use to initial or peak active use.

```text
ARR = Active Users at time t / Active Users at baseline
```

ARR is useful because deployed AI often fails through lack of use, even when technical performance is acceptable.

### Workflow Impact Retention

Workflow impact retention compares current measured workflow improvement to the initial measured improvement.

Examples:

- Minutes saved per encounter
- Hours saved per week
- Reduction in turnaround time
- Reduction in duplicate work
- Reduction in manual review

```text
WIR = Current Workflow Impact / Baseline Workflow Impact
```

### Financial Retention Ratio

Financial Retention Ratio compares current financial benefit to initial or projected financial benefit.

```text
FRR = Current Financial Benefit / Baseline Financial Benefit
```

This can include savings, revenue lift, productivity gain, cost avoidance, reduced leakage, or avoided loss.

### Model Utility Score

Model Utility Score is a composite construct. The exact weighting should vary by use case and governance context.

A simple starting expression is:

```text
MUS = w1(Technical Performance) + w2(Adoption) + w3(Workflow Impact) + w4(Financial Value) + w5(Outcome Impact) + w6(Governance Sustainability)
```

The project does not yet treat this as a final validated index. It is a research construct to be tested and refined.

## AI Half-Life

The AI Half-Life is reached when realized value has declined by 50 percent from the baseline or peak value state.

```text
AI Half-Life = time t where Value(t) <= 0.5 * Value(0)
```

This threshold can be applied to a single value metric or to a composite score.

## Decay models

The simplest conceptual model is exponential decay:

```text
Value(t) = Value(0) * e^(-k*t)
```

Where:

- Value(t) is realized value at time t
- Value(0) is baseline value
- k is the decay constant
- t is time after deployment

The half-life expression is:

```text
t_half = ln(2) / k
```

This does not mean every AI system decays exponentially. It gives the project a starting mathematical vocabulary that can later be compared against linear, Weibull, piecewise, or survival-analysis models.

## Event definition

A value failure event may occur when one or more of the following happens:

- Realized value falls below 50 percent of baseline
- Adoption falls below a governance-defined threshold
- Financial benefit no longer exceeds operating cost
- Workflow benefit disappears
- The model is formally retired
- The system remains deployed but is no longer meaningfully used

## Classification labels

### Survived

The deployment is reported as active, expanding, or continuing to create measurable value.

### Recalibrated

The deployment required reweighting, recalibration, redesign, workflow adjustment, model updating, or measurable intervention to maintain or improve value.

### Retired

The deployment was discontinued, replaced, or abandoned.

### Unknown

The available source does not provide enough follow-up evidence to classify persistence.

## Why this matters

Traditional monitoring can tell us whether a model changed.

AI Half-Life tries to tell us whether the value changed.
