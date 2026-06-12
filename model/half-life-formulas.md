# AI Half-Life Formulas

This document captures the first-pass mathematical language for the AI Half-Life project.

The formulas are working definitions. They are intended to support research and discussion, not to imply that the model is fully validated.

## Realized value

Realized value is the observed value produced by an AI system after deployment.

It may include:

- Dollars saved
- Revenue captured
- Time saved
- Errors avoided
- Operational throughput improved
- Clinical outcomes improved
- User productivity improved

Realized value should be measured against a baseline or expected value whenever possible.

## Value Realization Ratio

```text
VRR(t) = Realized Value(t) / Projected Value(t)
```

VRR compares actual realized value to expected value.

## Adoption Retention Ratio

```text
ARR(t) = Active Use(t) / Active Use(0)
```

ARR compares current adoption to initial or peak adoption.

## Workflow Impact Retention

```text
WIR(t) = Workflow Impact(t) / Workflow Impact(0)
```

Workflow impact may be measured in minutes saved, hours saved, throughput, reduced duplication, or reduced manual review.

## Financial Retention Ratio

```text
FRR(t) = Financial Benefit(t) / Financial Benefit(0)
```

Financial benefit may include direct savings, cost avoidance, revenue impact, or productivity gains.

## Composite Model Utility Score

A generic composite score can be written as:

```text
MUS(t) = wT*T(t) + wA*A(t) + wW*W(t) + wF*F(t) + wO*O(t) + wG*G(t)
```

Where:

- T = technical performance
- A = adoption
- W = workflow impact
- F = financial value
- O = clinical or operational outcome
- G = governance sustainability
- w = governance-defined weights

Weights should not be universal. They should be selected based on use case, risk, regulatory context, and strategic importance.

## AI Half-Life

```text
AI Half-Life = min(t) where Value(t) <= 0.5 * Value(0)
```

This is the first point in time when realized value falls to half of baseline value.

## Exponential decay model

The simplest value decay model is:

```text
Value(t) = Value(0) * e^(-k*t)
```

Where:

- Value(t) = realized value at time t
- Value(0) = initial value
- k = decay constant
- t = time after deployment

The associated half-life is:

```text
t_half = ln(2) / k
```

## Survival framing

The event of interest is value failure.

```text
Event = 1 if Value(t) <= Threshold
Event = 0 otherwise
```

Survival analysis can estimate the probability that an AI system remains above the value threshold over time.

```text
S(t) = P(T > t)
```

Where T is the time until value failure.

## Hazard framing

Hazard represents the instantaneous risk of value failure at time t, given that the system has survived until time t.

```text
h(t) = instantaneous risk of value failure at time t
```

Potential predictors:

- Declining adoption
- Increasing overrides
- Workflow redesign
- Sponsor turnover
- Model drift
- Rising maintenance cost
- Reduced financial benefit

## Important caution

The math is useful only if the measurement is honest.

A precise formula applied to weak evidence creates false confidence.

This project therefore emphasizes source quality, evidence grading, and explicit uncertainty.
