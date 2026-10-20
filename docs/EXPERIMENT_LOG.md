# Public-safe experiment summary

The executable experiments, competition data, model artefacts and complete Skore reports were maintained **outside this public repository**. The table below records non-sensitive team-reported outcomes, not independently executable benchmarks.

| Experiment | Validation | RMSE | Evidence / status |
| --- | --- | ---: | --- |
| `01_dummy` | One patient-grouped holdout (GroupShuffleSplit) | 16.83 | Early baseline previously recorded in the public team notes |
| `exp26` — HGBR + LightGBM ensemble | Grouped out-of-fold evaluation | 3.263067 | Team-reported selected experiment (local workspace) |
| `exp26` — Skore summary | Grouped cross-validation (team report) | 3.262757 | Team-reported mean score |

**Do not interpret these as directly comparable rows.** The dummy result is from a single grouped holdout; `exp26` used grouped cross-validation. Their splitting and aggregation methods differ.

Other experiments were explored, but their complete metrics and configurations are **not published here**. No additional experiment scores are inferred.

## Methodological checklist

For a fully reproducible restricted experiment journal, record:

- experiment ID, model and preprocessing changes;
- patient grouping column and fold construction;
- feature exclusions and target leakage checks;
- per-fold and out-of-fold RMSE, with a consistent aggregation definition;
- comparison to baselines using the **same** folds;
- random seeds, library versions and runtime;
- error analysis and reason for selecting or rejecting the run.

**Publication boundaries:** keep patient-level data, private submissions, credentials, internal report URLs and restricted artefacts out of the public repository.
