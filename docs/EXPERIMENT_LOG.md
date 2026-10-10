# Experiment log

This is a public-safe experiment journal. Record only non-sensitive summaries; keep actual competition data and private credentials outside GitHub.

| Experiment | Validation | RMSE | Status |
|---|---|---:|---|
| 01_dummy | One patient-grouped holdout (GroupShuffleSplit) | 16.83 | Verified from Bob screenshot |
| 02_ridge | To be confirmed | — | Pending verification |
| Other experiments | Five-fold patient-grouped CV | — | Pending |

The Dummy RMSE of 16.83 is **not** a result from GroupKFold. Re-evaluate against the same patient-grouped folds for fair comparisons.

## Record for each future experiment
- Date, Bob operator, report key
- Scientific hypothesis and exactly what changed
- Feature exclusions and pre-processing
- Same grouped-CV folds used? Which ones?
- RMSE per fold, average, variability, runtime
- Comparison against same-fold baseline
- Evidence of leakage checks, limitations and errors
- Decision: keep, discard or retest
- Skore URL and Kaggle result: track in the restricted team workspace, not in this public document

Do not invent results.
