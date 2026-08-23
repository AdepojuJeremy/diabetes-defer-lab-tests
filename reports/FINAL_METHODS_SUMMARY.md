# Final Methods Summary

## Study design

This study develops and evaluates a cost-sensitive selective prediction cascade for diabetes screening. The first-stage predictor uses inexpensive demographic, anthropometric, blood-pressure, lifestyle, and non-diabetes medical-history information. A learned defer gate observes only these inexpensive variables and determines whether the first-stage decision should be accepted or whether laboratory testing should be requested.

## Data

The primary dataset is the US National Health and Nutrition Examination Survey (NHANES), pooling the 2011–2012, 2013–2014, 2015–2016, and 2017–2018 cycles.

Participants are linked across NHANES components using SEQN.

The temporal evaluation design uses:

- 2011–2014 for training;
- 2015–2016 for validation;
- 2017–2018 for final testing.

## Primary outcome

The primary screening cohort consists of adults with at least one of HbA1c or fasting plasma glucose measured, excluding participants with known diabetes.

Screen-detected diabetes is defined as:

- HbA1c ≥ 6.5%, or
- fasting plasma glucose ≥ 126 mg/dL.

OGTT is treated as a secondary laboratory source rather than a requirement for the primary endpoint.

## Model architecture

The neural cascade contains three components:

1. cheap-stage predictor;
2. full-information predictor;
3. laboratory defer gate.

The defer gate receives only cheap-stage features.

The principal optimization objective combines prediction loss, laboratory-use cost, and a budget constraint on expected deferral.

## Laboratory allocation

The learned defer score is converted to deterministic referral decisions by selecting thresholds on the validation set for specified laboratory budgets.

The primary operating point is approximately 35% laboratory utilization.

## Comparators

The learned referral policy is compared with:

- cheap prediction without referral;
- referral of all participants;
- cheap-risk threshold referral;
- uncertainty-based referral;
- random referral;
- an oracle upper bound used only as a nondeployable benchmark.

## Evaluation

Primary metrics include sensitivity, specificity, balanced accuracy, precision, F1 score, missed-case rate, laboratory utilization, and normalized clinical cost.

Subgroup analyses evaluate referral coverage, under-referral among true cases, sensitivity, specificity, and calibration.

Interpretability uses Integrated Gradients and grouped feature ablation.

Robustness analyses vary laboratory budgets, cost assumptions, feature availability, outcome definitions, missingness, and selected training-time budget constraints.