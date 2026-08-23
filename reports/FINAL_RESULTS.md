# Final Results Summary

## Primary temporal test performance

The final temporal test cohort contained 4,458 participants, including 263 participants meeting the primary screen-detected diabetes definition (5.9%).

At the prespecified approximately 35% laboratory operating point, the learned cascade referred 38.7% of the temporal test cohort for laboratory testing.

The resulting cascade achieved sensitivity of 81.7%, specificity of 93.9%, balanced accuracy of 87.8%, and precision of 45.6%.

The corresponding missed-case rate was 18.3%.

## Learned laboratory referral mechanism

Integrated Gradients identified the strongest drivers of laboratory referral as: age, systolic_bp, waist_cm, height_cm, bmi.

Features with disproportionately greater importance for referral than for cheap-stage risk prediction included: systolic_bp, bmi, weight_kg, age, obesity.

The defer score's ability to identify cases for which laboratory information changed the cheap-stage decision had AUROC 0.896 and AUPRC 0.761.

The learned gate referred 80.4% of participants for whom laboratory testing changed the cheap-stage classification.

It also referred 32.4% of otherwise avoidable cheap-stage false negatives.

## Robustness

The most consequential cheap-feature group ablation was demographics, associated with a sensitivity change of -0.103.

With 20% additional random missingness imposed on cheap-stage features, mean sensitivity was 74.4%.

Across resource budgets, outcome definitions, feature ablations, missingness stress tests, and alternative cost assumptions, performance was evaluated as a policy frontier rather than assuming a single universally optimal laboratory threshold.