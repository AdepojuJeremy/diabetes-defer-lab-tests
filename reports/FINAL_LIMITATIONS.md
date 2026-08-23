# Limitations and Interpretation

1. NHANES is a cross-sectional survey. The analysis therefore evaluates screening and diagnostic classification rather than longitudinal progression to diabetes.

2. The primary endpoint is defined using laboratory measurements that are also supplied to the full-information branch. Interpretation of the full laboratory predictor is consequently not emphasized because HbA1c and fasting glucose directly define the endpoint.

3. Laboratory referral cost is represented using normalized relative costs rather than a single universal monetary value. The cost-sensitivity analysis is therefore more informative than any single assumed cost ratio.

4. The learned gate optimizes expected value under a constrained laboratory budget. Equal referral rates across demographic groups are not imposed as an objective because clinical need and disease prevalence can differ between groups. Equity conclusions should therefore consider positive-case referral coverage, under-referral, sensitivity, specificity, and calibration jointly.

5. The temporal split provides a stronger test than random splitting but does not constitute geographic or health-system external validation.

6. NHANES questionnaire and lifestyle measures may contain recall error, measurement error, or missingness.

7. The model should not be interpreted as a replacement for clinical diagnosis or existing screening guidelines. It is a resource-allocation framework for investigating when inexpensive screening information may justify additional laboratory testing.

8. Deployment would require prospective validation, externally defined laboratory costs, operational workflow analysis, and assessment under the target population's disease prevalence and clinical practice patterns.

9. The oracle referral strategy is strictly an analytical upper bound and is not deployable because it relies on information unavailable at the actual referral decision point.

10. Integrated Gradients and ablation analyses characterize model dependence and attribution but do not establish causal effects of patient characteristics on diabetes or referral decisions.