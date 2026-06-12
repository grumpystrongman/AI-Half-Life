# Upload Manifest

Some generated files were created locally during the research workflow but cannot be uploaded through the current GitHub connector because the connector only supports UTF-8 text file creation through the contents API.

Upload these files manually through the GitHub web UI or with a local git client.

## Data workbooks

Upload to `data/`:

- `ai_half_life_deployment_dataset_v0_1.xlsx`
- `ai_half_life_deployment_dataset_v0_1.json`
- `ai_half_life_verified_deployments_v0_1.csv`
- `ai_half_life_outcome_observations_v0_1.csv`

Note: Markdown-compatible seed CSV versions have already been pushed as:

- `data/verified-deployments-v0.1.csv`
- `data/outcome-observations-v0.1.csv`

## Research corpus

Upload to `research/`:

- `ai_half_life_research_corpus.xlsx`
- `ai_half_life_research_corpus_v2.xlsx`
- `ai_half_life_research_corpus.json`
- `ai_half_life_source_inventory.csv`

## Source synthesis document

Upload to `research/` or `whitepaper/source-materials/`:

- `Healthcare AI Deployment Governance Monitoring and Value Realization.docx`

## LinkedIn image pack

Upload to `assets/`:

- `00_contact_sheet.png`
- `01_ai_half_life_concept_curve.png`
- `02_ai_half_life_research_process.png`
- `03_ai_half_life_dataset_snapshot.png`
- `04_ai_half_life_metric_families.png`

## Recommended folder structure after manual upload

```text
assets/
  00_contact_sheet.png
  01_ai_half_life_concept_curve.png
  02_ai_half_life_research_process.png
  03_ai_half_life_dataset_snapshot.png
  04_ai_half_life_metric_families.png

data/
  ai_half_life_deployment_dataset_v0_1.xlsx
  ai_half_life_deployment_dataset_v0_1.json
  ai_half_life_verified_deployments_v0_1.csv
  ai_half_life_outcome_observations_v0_1.csv
  verified-deployments-v0.1.csv
  outcome-observations-v0.1.csv

research/
  ai_half_life_research_corpus.xlsx
  ai_half_life_research_corpus_v2.xlsx
  ai_half_life_research_corpus.json
  ai_half_life_source_inventory.csv
  Healthcare AI Deployment Governance Monitoring and Value Realization.docx
```

## Why this matters

The repository should remain transparent about what has been pushed directly and what still needs manual binary upload.

The project should not hide tooling limitations.
