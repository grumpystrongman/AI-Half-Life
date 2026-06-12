# Data Dictionary

This document defines the working schema for the AI Half-Life deployment dataset.

## Dataset design

The dataset is organized around two core tables:

1. Verified deployments
2. Outcome observations

A verified deployment is a public, source-backed AI system that was deployed or piloted in a real operational setting.

An outcome observation is a specific measurable result associated with that deployment.

## Verified deployments table

### deployment_id

Unique project identifier.

### organization

Organization responsible for the deployment or primary reported deployment site.

### industry

Sector or domain.

Examples:

- Healthcare
- Banking
- Logistics
- Retail
- Technology
- Insurance
- Manufacturing

### use_case

Plain-language description of the AI use case.

Examples:

- Ambient documentation
- Readmission targeting
- Fraud detection
- Recommendation system
- Robotic picking
- Coding assistant

### deployment_year

Year of deployment, pilot, public rollout, or publication if exact launch year is not reported.

### model_type

High-level model or system category.

Examples:

- Predictive ML
- Generative AI
- Recommendation system
- Computer vision
- Optimization model
- Robotics AI
- Clinical decision support
- Hybrid system

### deployment_setting

Operational environment where the system was used.

Examples:

- Hospital inpatient
- Ambulatory clinic
- Emergency department
- Supply chain
- Software engineering
- Customer service
- Consumer platform

### evidence_tier

Evidence quality category.

Gold: Peer-reviewed or official source with measurable post-deployment outcome.

Silver: Credible industry, government, or major media source with measurable outcome.

Bronze: Candidate source, conference material, vendor-reported case, or incomplete evidence requiring further validation.

### source_title

Title of the source.

### source_url

URL for the source.

### source_type

Type of source.

Examples:

- Peer-reviewed study
- Preprint
- Official report
- Industry report
- News article
- Company blog
- Conference proceeding

### follow_up_duration

Reported follow-up window or observed operational period.

Examples:

- 6 weeks
- 30 days
- 9 months
- 1 year
- Ongoing
- Not reported

### status

Initial status classification.

- Survived
- Recalibrated
- Retired
- Unknown

### status_rationale

Brief explanation for the classification.

## Outcome observations table

### observation_id

Unique observation identifier.

### deployment_id

Foreign key to the deployment table.

### metric_family

Measurement category.

Examples:

- Technical
- Adoption
- Workflow
- Financial
- Clinical
- Operational
- Governance
- Human experience

### metric_name

Name of the reported metric.

Examples:

- AUC
- Active users
- Encounters documented
- Hours saved
- Manual work reduction
- Burnout reduction
- Error reduction
- Engagement lift

### metric_value

Reported value.

### metric_unit

Unit of measurement.

Examples:

- Percent
- Dollars
- Users
- Encounters
- Minutes
- Days
- Events

### baseline_value

Baseline comparator if reported.

### comparator

Description of comparison.

Examples:

- Before deployment
- Heuristic baseline
- Control group
- Prior workflow
- Alternative model

### timepoint

When the outcome was measured.

Examples:

- 30 days after rollout
- 6-week pilot
- 9-month observation period
- 1-year follow-up

### extraction_note

Notes about interpretation, limitations, or ambiguity.

## Expansion backlog

The backlog tracks candidate deployments that may become verified cases after source validation.

Backlog records should never be treated as verified evidence until they meet inclusion criteria.

## Inclusion criteria

A case can enter the verified deployment dataset if it has:

1. A named organization or deployment context.
2. A specific AI use case.
3. Evidence of real deployment or pilot.
4. At least one measurable post-deployment outcome.
5. A public source.

## Exclusion criteria

A case should be excluded or left in the backlog if it is only:

- A model development paper with no deployment.
- A vendor claim with no measurable outcome.
- A press release with no post-deployment result.
- A general AI strategy announcement.
- A speculative use case.

## Important limitation

This dataset is not yet representative of all deployed AI systems.

Public reporting is biased toward positive cases, survivors, and high-profile deployments. Any later statistical inference should account for publication bias and survivorship bias.
