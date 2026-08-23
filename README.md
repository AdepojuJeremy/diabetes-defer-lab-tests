# Learning to Defer to Lab Tests: Cost-Sensitive Selective Prediction for Diabetes Screening Cascades

## Overview

This repository contains the complete computational research release for a resource-aware diabetes screening cascade that learns when inexpensive clinical information is sufficient and when laboratory testing should be requested.

The framework combines a cheap-stage risk predictor, a laboratory-informed prediction stage, and a learned defer gate that determines when laboratory testing should be acquired.

The central research question is whether selective laboratory acquisition can retain much of the diagnostic value of universal testing while substantially reducing laboratory utilization.

## Data

The study uses NHANES 2011-2018.

Temporal evaluation:

- Training: NHANES 2011-2014
- Validation: NHANES 2015-2016
- Test: NHANES 2017-2018

Participant-level NHANES files and derived analytic datasets are not redistributed through this repository.

See DATA_AVAILABILITY.md and data/README.md.

## Primary endpoint

Participants with known diagnosed diabetes are excluded from the primary screening cohort.

Screen-detected diabetes is operationally defined as HbA1c >= 6.5% or fasting plasma glucose >= 126 mg/dL.

This retrospective research endpoint based on one-time NHANES laboratory measurements should not be interpreted as a substitute for confirmatory clinical diagnosis.

## Primary operating point

The principal selective-testing analysis targets approximately 35% laboratory utilization.

Primary normalized costs:

- Laboratory referral = 1
- False negative = 10
- False positive = 2

## Repository contents

- 
otebooks/ - complete computational workflow
- esults/main/ - manuscript-facing figures and tables
- esults/supplementary/ - supplementary and appendix analyses
- eports/ - final methods, results, limitations, and completion summaries
- metadata/ - reproducibility metadata, inventories, metrics, and claims registry
- download_registry/ - NHANES acquisition manifests and download records
- data/README.md - data reproduction guidance

## Results

The repository preserves the complete analytical output of the study.

Main-paper figures and tables are stored under esults/main/. All remaining EDA, calibration, fairness, interpretability, budget-sweep, ablation, cost-sensitivity, and robustness outputs are retained under esults/supplementary/.

See RESULTS_INDEX.md for the complete catalogue.

## Reproduction

Follow RUN_ORDER.md for the computational sequence.

Install the core Python dependencies with:

    pip install -r requirements.txt

equirements-aws-freeze.txt preserves the package environment used for the original AWS execution.

See REPRODUCIBILITY.md for additional details.

## Interpretation

This repository represents retrospective methodological research. The screening cascade is not a clinical diagnostic device and requires external and prospective validation before clinical deployment.

NHANES survey weights were not fully incorporated into all modeling analyses; results should therefore not be interpreted as population-representative prevalence estimates where survey weighting is required.

## Citation

Publication-specific citation information will be added when the associated manuscript is finalized.
