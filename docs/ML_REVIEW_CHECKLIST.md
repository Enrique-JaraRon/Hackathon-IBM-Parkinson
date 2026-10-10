# ML review checklist

This is a **conceptual review guide**, not model code. The official organizers' DAY2 guide remains the primary technical workflow.

## Scientific target
- [ ] Continuous 'true OFF' score; not a classification task.
- [ ] Observed ON and OFF are noisy clinical measurements, not the hidden unbiased target.
- [ ] Understand medication timing, disease progression, rater differences and missing observations.
- [ ] Synthetic data are not proof of real clinical efficacy.

## Data and leakage
- [ ] Patient-grouped cross-validation: no patient appears in both train and validation.
- [ ] Visit key `Index` and patient key `patient_id` are excluded as predictors.
- [ ] Preprocessing steps are trained only on each training fold.
- [ ] Any longitudinal information used for a prediction would be available at that moment.
- [ ] Train target and feature rows matched correctly by visit key.
- [ ] Test features have consistent names and types.

## Evaluation
- [ ] Compare models on **identical patient-grouped folds**.
- [ ] Use **visit-level RMSE** and inspect every fold, not only the mean.
- [ ] Compare to a Dummy evaluated on those same folds.
- [ ] Report variability and investigate unexpected failures.
- [ ] Do not use the public leaderboard as the only hyperparameter selection signal.

## Originality and interpretation
The official context highlights temporal progression, medication timing and informative missingness. Good questions to investigate using **authorized tools** include: what information is added by duration since diagnosis? does missingness correlate with outcome or visit type? do findings generalize across cohorts and raters? Which mistakes are more common when observed OFF is absent?

For originality credit, explain the scientific mechanism, show a valid comparison and state the observed benefit or failure. Do not claim novelty for simply repeating the guided Day 2 models.
