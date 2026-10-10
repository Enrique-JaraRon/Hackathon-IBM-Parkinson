# Technical documentation checklist

This file will be completed from real, verified outputs created by the team in the officially authorized workflow.

## Sections for the final code report

1. **Goal:** estimate a continuous debiased OFF score per patient visit; visit-level RMSE.
2. **Data inventory:** explain X_train, y_train, X_test, sample_submission and the target column. Do not republish dataset rows.
3. **Environment:** Python, Bob, skore, official setup guide and setup test results.
4. **EDA:** group sizes, missing fields, categorical features and possible leakage.
5. **Methodology:** patient-grouped validation, data preparation fitted on training folds only, consistent RMSE.
6. **Experiments:** baseline, authorized candidate models and final comparison with the same folds.
7. **Results:** fold RMSE, variability, objective improvements, actual Kaggle score and permitted Skore evidence.
8. **Originality:** clinical hypothesis, what changed and what the experiment demonstrated.
9. **Reproducibility:** actual tool versions, dependency setup, authorized command sequence, known limitations.
10. **Integrity:** credit the tools, team work and the actual provenance of code.

Current verified reference: Dummy baseline RMSE 16.83 on one patient-grouped holdout, **not** on grouped five-fold cross-validation.

## Model comparison table

| Model | Common grouped-CV mean RMSE | Fold variability | Report | Decision |
|---|---|---|---|---|
| Dummy | pending common-fold score | pending | private Skore | baseline |
| Ridge | pending | pending | private Skore | pending |
| HistGradientBoosting | pending | pending | private Skore | pending |
| Mixed-type pipeline | pending | pending | private Skore | pending |
| Original team approach | pending | pending | private Skore | pending |

Never invent numerical results. In a public repository, record only aggregates cleared for public sharing.
