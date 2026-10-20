# Parkinson's Disease Progression — Machine Learning Hackathon

**ESILV × IBM × Probabl · Bobathon 2026 · Team TheLebanese**

A four-person team project to predict a debiased **OFF-state MDS-UPDRS motor score** from visit-level information. The main machine-learning challenge is **generalisation to patients absent from the training data**, making patient-level validation and leakage prevention essential.

[Competition](https://www.kaggle.com/competitions/bobathon-esilv/) · [Official workshop repository](https://github.com/probabl-ai/bobathon-esilv) · [Skore](https://skore.probabl.ai/)

## Project at a glance

| Dimension | Approach |
| --- | --- |
| **Task** | Continuous regression: estimate patient-visit motor severity |
| **Evaluation metric** | Root Mean Squared Error (RMSE); lower is better |
| **Validation** | Patient-grouped cross-validation so the same patient is not split across training and validation folds |
| **Model development** | Baselines, tabular preprocessing, gradient boosting and ensemble experiments |
| **Experiment tracking** | Local experiment records and Skore reports |
| **Main methodological concern** | Patient-level data leakage, appropriate splitting and fair model comparison |

## Reported team results

The team reported the following results from its **restricted local workspace**:

- **Selected experiment:** `exp26`, an ensemble involving histogram-based gradient boosting and LightGBM.
- **Out-of-fold RMSE:** approximately **3.263** (reported local result: 3.263067).
- **Skore cross-validation mean RMSE:** approximately **3.263** (reported: 3.262757).
- **Early DummyRegressor baseline:** RMSE **16.83** on **one patient-grouped holdout**, not the same cross-validation protocol.

**Interpretation:** The early dummy baseline and final grouped cross-validation score come from **different validation designs** and should not be used to claim a precise percentage improvement. The final score is a **team-reported result**, not independently reproducible from this public repository.

## Methodology

1. **Define the target and patient identifier.** Treat visits from the same patient as related observations.
2. **Keep validation groups disjoint.** Patient-grouped folds better reflect performance on unseen patients than random visit splits.
3. **Fit preprocessing inside training folds.** Avoid using validation patients to learn feature transformations or target information.
4. **Compare baselines and nonlinear models.** Track the changes in features, parameters and validation design.
5. **Inspect errors and limitations.** Report out-of-fold error, leakage checks and modelling assumptions.

This structure matters more than a single leaderboard figure: a strong Kaggle score without patient-level validation can be misleading.

## What is public here

This repository intentionally contains **documentation, experiment-tracking templates, methodological checklists and a video outline**. It is **not the executable final model repository**. The competition data, patient-level rows, submission files, model artefacts and restricted reports are not published here.

- [Technical documentation](docs/TECHNICAL_DOCUMENTATION.md)
- [Experiment log (public-safe summary)](docs/EXPERIMENT_LOG.md)
- [Methodological review checklist](docs/ML_REVIEW_CHECKLIST.md)
- [Rules and publication boundaries](docs/RULES_AND_PERMISSION.md)
- [Final deliverables checklist](docs/FINAL_DELIVERABLES.md)

Earlier [session plan](docs/DAY2_COMMAND_CENTER.md), [team collaboration guide](docs/TEAM_WORKFLOW.md) and [video storyboard](video/STORYBOARD.md) are retained as **historical project materials**, not as an indication that the competition is still ongoing.

## Lessons and limitations

- Grouped cross-validation is critical when visits are nested within patients.
- Reported RMSE depends on both the model and the validation protocol.
- Ensembles can improve predictive performance but also increase complexity and reproducibility requirements.
- The public repository does not contain sufficient source code or permitted data to rerun the reported results.

**Scope:** an educational collaborative machine-learning project; not a clinical prediction tool.
