# Data Availability

This project uses publicly available data from the US National Health and Nutrition Examination Survey (NHANES).

The primary analysis uses the 2011–2012, 2013–2014, 2015–2016, and 2017–2018 survey cycles.

Raw NHANES files should not be redistributed as part of the repository when they can instead be retrieved directly from the official data provider. The repository should contain acquisition code, file manifests, harmonization logic, and documentation sufficient to reproduce the analytic dataset.

Participants are linked across NHANES components using the respondent identifier `SEQN`.

The 2017–2018 OGTT component is not required for the primary endpoint. HbA1c and fasting plasma glucose are the primary laboratory measurements used to define screen-detected diabetes.