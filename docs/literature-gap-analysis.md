# Literature Gap Analysis

## Purpose

This document summarizes the research gap behind the AI Half-Life project.

The working question is:

Do current AI governance, monitoring, and evaluation frameworks measure long-term realized value decay after deployment?

## What the literature measures well

The existing literature and public frameworks are comparatively strong in several areas.

### Governance, safety, and responsible AI

Commonly measured or discussed dimensions include:

- Risk management
- Accountability
- Transparency
- Explainability
- Human oversight
- Safety
- Security
- Privacy
- Bias and fairness
- Responsible deployment controls

Representative source families include NIST, WHO, CHAI, FDA, Joint Commission, and other healthcare AI governance bodies.

### Technical performance and drift

The monitoring literature is mature around technical deterioration.

Commonly measured dimensions include:

- Accuracy
- Precision
- Recall
- AUC
- Calibration
- Data drift
- Concept drift
- Dataset shift
- Temporal performance drift
- Model updating

### Deployment and adoption snapshots

Healthcare surveys and industry reports increasingly measure:

- Whether organizations have deployed AI
- Which use cases are live
- Whether accuracy or bias is evaluated
- Whether post-implementation monitoring exists
- Whether clinicians or users report improvement
- Whether organizations report privacy or governance concerns

## What is measured less consistently

The literature becomes weaker when the question shifts from deployment to value persistence.

Less consistently reported dimensions include:

- Long-term active use
- Adoption decay
- Declining recommendation acceptance
- Workflow workarounds
- Alert fatigue over time
- Trust decay
- Financial benefit erosion
- Cost-to-maintain over time
- Governance review persistence
- Retirement criteria
- Time-to-value-failure

## The central gap

The literature has many ways to ask whether a model is accurate, safe, responsible, or drifting.

It has far fewer ways to ask whether a deployed AI system is still worth maintaining two or three years later.

That is the gap AI Half-Life is intended to address.

## Why this gap matters

A deployed AI system can fail in multiple ways:

1. The data changes.
2. The model performance changes.
3. The workflow changes.
4. The users stop trusting it.
5. The business case erodes.
6. The cost to maintain exceeds the benefit.
7. The sponsor leaves.
8. The governance process becomes inactive.

Current frameworks tend to address some of these factors separately. The AI Half-Life project asks whether they can be integrated into a practical post-deployment value measurement framework.

## Early research conclusion

The early literature review supports a cautious but promising conclusion:

The ingredients for AI Half-Life already exist across governance, MLOps, drift monitoring, implementation science, reliability engineering, survival analysis, and health economics. What appears to be missing is the integrated time-dependent value construct itself.

## Research posture

This project does not claim to have proven the final model.

It claims there is a meaningful measurement gap worth studying.

That distinction matters.
