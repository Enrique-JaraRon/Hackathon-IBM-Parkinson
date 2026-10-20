# Technical Retrospective — Parkinson's Prediction Hackathon

**Project:** Bobathon 2026 (ESILV × IBM × Probabl)  
**Team:** TheLebanese (four-person group)  
**Availability:** This document is a public-safe methodological summary. Model code, organiser-provided data, submission files and full private reports are **not included**.

## 1. Predictive objective

The task was to estimate a continuous, debiased **OFF-state MDS-UPDRS motor score** for patient visits. The evaluation criterion was **root mean squared error (RMSE)**: lower values indicate smaller prediction errors, with large residuals penalised quadratically.

Observations were repeated visits nested within patients, so random row-wise validation could leak patient-specific information across folds.

## 2. Data and validation design

The official competition provided structured visit-level training/test files and submission formats. No patient-level observations are reproduced in this repository.

The central validation principle was **patient-grouped cross-validation**: each patient must appear entirely in either a fold's training set or its validation set. Candidate models should be assessed on the same group assignments when making fair comparisons.

Useful safeguards include:

- excluding identifiers that act as memorisation shortcuts;
- fitting imputers, encoders and other learned transformations **inside** training folds;
- checking features for information unavailable at prediction time;
- measuring each fold as well as aggregate/out-of-fold performance.

The presence of these recommendations does not by itself prove that every private training run passed every audit check.

## 3. Modelling approach

The team explored regression baselines and tabular machine-learning methods. Its reported selected run, **`exp26`**, combined **histogram-based gradient boosting** and **LightGBM** in an ensemble.

Conceptually, boosted tree models are appropriate candidates for tabular nonlinear interactions and heterogeneous features, but they require careful control of preprocessing, hyperparameter selection and validation leakage.

Implementation details, full feature lists and model artefacts remain in the restricted team workspace and cannot be reconstructed from this public documentation alone.

## 4. Results and interpretation

| Run | Evaluation procedure | Reported RMSE |
| --- | --- | ---: |
| Early dummy baseline | One patient-grouped holdout | 16.83 |
| `exp26` selected ensemble | Grouped out-of-fold evaluation | 3.263067 |
| `exp26` Skore summary | Grouped cross-validation mean | 3.262757 |

These are **team-reported summaries**. The public repository does not host the private reports or the code needed for independent replication.

The baseline and final results use **different splitting/aggregation protocols**. Therefore, it would be methodologically unsound to state an exact percentage improvement from these numbers alone.

No unverified per-fold metrics, leaderboard placement or confidence intervals are added here.

## 5. What would be required for full reproducibility

An authorised independent replication would require:

1. permitted competition data and a documented target definition;
2. the exact training/validation patient groups and random seeds;
3. the approved training code and preprocessing pipeline;
4. pinned dependency versions and execution instructions;
5. complete per-fold metrics and model-selection history.

These materials are not publicly distributed by this repository. See [the experiment summary](EXPERIMENT_LOG.md) and [the review checklist](ML_REVIEW_CHECKLIST.md) for the non-sensitive record.

## 6. Limitations and lessons

- Small apparent errors are not meaningful without a leakage-resistant validation protocol.
- Grouped splits simulate unseen patients better than naive visit-level splits, but do not guarantee transportability to a new hospital or population.
- An ensemble's complexity should be justified by consistent, same-fold comparisons.
- Report only results actually observed in the permitted environment, and distinguish internal experiment scores from external evaluation.
- Synthetic or challenge-specific data do **not** establish clinical utility.

**This project is educational and is not intended for clinical decision-making.**
