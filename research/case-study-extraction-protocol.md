# Case Study Extraction Protocol

## Purpose

This protocol defines how published AI deployment cases should be reviewed and extracted for the AI Half-Life dataset.

The goal is to make the dataset defensible, repeatable, and auditable.

## Research question

Which published AI deployment case studies contain measurable post-deployment outcomes that can help evaluate value persistence over time?

## Priority case types

The project prioritizes deployments that report at least one of the following:

- Adoption after deployment
- Workflow change
- Financial impact
- Clinical or operational outcome
- Technical performance in production
- Recalibration or maintenance activity
- Retirement or replacement
- Follow-up duration

## Extraction workflow

### Step 1: Identify candidate source

Sources may include:

- Peer-reviewed papers
- Preprints
- Government reports
- Industry reports
- Company technical blogs
- Conference proceedings
- Major news articles
- Health system case studies

### Step 2: Confirm deployment

The case must include evidence that the AI system was deployed, piloted, tested in a live operational workflow, or evaluated after implementation.

Pure model development papers should not be included as verified deployments.

### Step 3: Extract deployment metadata

Capture:

- Organization
- Industry
- Use case
- Deployment year
- Model type
- Deployment setting
- Source title
- Source URL
- Source type

### Step 4: Extract outcome observations

Each distinct measurable result becomes a separate outcome observation.

Examples:

- 4,000 clinicians adopted the tool
- Burnout dropped by 31 percent
- Manual work fell by 90 percent
- Length of stay declined by 0.67 days
- Pick failure rate dropped by 20 percent
- Engagement would decline by 12 percent if production recommender were replaced

### Step 5: Assign evidence tier

Gold:

Peer-reviewed, official, or highly detailed technical source with measurable post-deployment outcomes.

Silver:

Credible public source with measurable outcome, but not fully peer-reviewed or not deeply technical.

Bronze:

Candidate or incomplete evidence requiring validation.

### Step 6: Assign status

Survived:

Source indicates the system is active, expanding, or continuing to produce measurable value.

Recalibrated:

Source indicates the model or workflow was recalibrated, reweighted, updated, or redesigned after deployment.

Retired:

Source indicates the system was discontinued, replaced, or abandoned.

Unknown:

Source reports deployment but does not provide enough follow-up evidence to classify persistence.

## Quality rules

Do not infer missing values as facts.

Do not treat marketing language as outcome evidence unless it includes measurable results.

Do not merge separate deployments unless the source clearly describes them as the same system.

Do not treat a model development paper as deployment evidence unless implementation or live evaluation is documented.

Do not treat backlog candidates as verified rows.

## Notes for reviewers

The most common problem is overclaiming. A source may report that a tool exists, but not whether it produced value after deployment.

The second most common problem is confusing activity with value. User counts, encounter counts, or model calls are adoption signals. They are not automatically proof of financial, clinical, or operational value.

The third most common problem is follow-up duration. A six-week pilot is useful, but it does not prove multi-year value persistence.

## Desired future improvement

Future versions should include dual-review extraction, disagreement resolution, and inter-rater reliability scoring.
