# Data Directory

Participant-level NHANES data and derived analytic datasets are not distributed with this repository.

The analysis reconstructs the required datasets from publicly available NHANES source files.

## Local directory layout

When reproducing the project, the workflow may create:

- `raw_nhanes/` — downloaded NHANES XPT files
- `interim/` — merged and harmonized intermediate datasets
- `processed/` — modeling cohorts and analysis-ready datasets

These directories are excluded from Git version control.

See `../DATA_AVAILABILITY.md` and the Stage 0 data-acquisition notebook for details.
