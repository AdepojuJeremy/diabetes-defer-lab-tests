# Reproducibility Notes

The computational study was originally executed on an Ubuntu 22.04 AWS EC2 environment with an NVIDIA L4 GPU.

The repository has subsequently been sanitized for public release. Machine-specific paths, instance IP addresses, credentials, raw participant-level datasets, caches, and large transient artifacts are not included.

The notebooks constitute the canonical computational workflow.

## Reproduction order

Follow `RUN_ORDER.md`.

## Environment

For a concise dependency specification:

`requirements.txt`

For provenance describing the original execution environment:

`requirements-aws-freeze.txt`

## Data

NHANES source data are publicly available from the U.S. Centers for Disease Control and Prevention / National Center for Health Statistics.

Raw and derived participant-level files are intentionally excluded from Git version control. See:

`DATA_AVAILABILITY.md`

and:

`data/README.md`

## Results

All retained research figures and tables are catalogued in:

`RESULTS_INDEX.md`

The `results/main/` directory contains manuscript-facing outputs.

The `results/supplementary/` directory contains additional analyses, diagnostics, robustness checks, ablations, and appendix material.

## Important interpretation note

The study's operational outcome uses one-time NHANES laboratory measurements for retrospective screening research. It should not be interpreted as a substitute for confirmatory clinical diagnosis.
