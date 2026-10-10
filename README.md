# Hackathon-IBM-Parkinson

**Team TheLebanese · ESILV × IBM × Probabl · Bobathon 2026**

[Official competition](https://www.kaggle.com/competitions/bobathon-esilv/) · [Official lab](https://github.com/probabl-ai/bobathon-esilv) · [Skore Hub](https://skore.probabl.ai/)

## Mission

Predict the **debiased true OFF MDS-UPDRS motor score** for Parkinson's patient visits (continuous regression target). Competition ranking uses **visit-level RMSE** on completely unseen **patients**, so patient-wise validation matters more than a random split of visits.

This repository is **public** for now and contains **public-safe documentation only**. It is **not** a mirror/fork of the organizer's dataset or an environment to publish predictions. Do not push CSVs, patient-level observations, submission files, Skore credentials, private reports, or unapproved code.

## Assessment priorities

| Assessment dimension | Contribution to overall grade |
|---|---:|
| Official Kaggle score | **35%** |
| Code documentation | **21%** |
| Model originality | **14%** |
| Video (strictly ≤ 5 minutes) | **30%** |

Source: ESILV kickoff assessment slide. A previous slide described the 30% challenge component as 'presentation'; the later kickoff document specifies **code documentation**. Confirm discrepancies with course staff.

## Confirmed progress (local team work; not publicly reproduced here)

- **Setup:** Python 3.13.7, Bob + skore, all 14 skills installed, Skore Hub workspace `TheLebanese`, **7/7 setup tests passed** on one teammate's machine.
- **Exploration:** performed through Bob on the competition-provided synthetic visit data.
- **Baseline:** mean DummyRegressor RMSE **16.83** on **one patient-grouped holdout** (not five-fold CV). This number must not be compared as if it were an identical GroupKFold estimate.
- **Next:** the organizers' [Day 2 guide](https://github.com/probabl-ai/bobathon-esilv/blob/main/docs/DAY2.md) covers Ridge, patient-grouped CV, gradient boosting, categorical handling, and final submissions through Bob/skore.

## Deliverables and navigation

- [Assessment and deadlines](docs/ASSESSMENT_AND_DEADLINES.md)
- [GitHub collaboration and credit budget](docs/TEAM_WORKFLOW.md)
- [Experiment journal](docs/EXPERIMENT_LOG.md)
- [Documentation / reproducibility](docs/TECHNICAL_DOCUMENTATION.md)
- [Methodological review points](docs/ML_REVIEW_CHECKLIST.md)
- [Team handoff template](docs/HANDOFF.md)
- [Permissions and competition rules](docs/RULES_AND_PERMISSION.md)
- [5-minute video storyboard](video/STORYBOARD.md)
- [Final delivery checklist](docs/FINAL_DELIVERABLES.md)

**Important:** A professor reportedly allowed external AI assistance, but the published competition rules still require Bob as the coding agent. Do not disguise code provenance. Seek explicit confirmation from the organizers that any relaxed rule also applies to **Kaggle eligibility**, before treating external-agent-authored submission code as eligible.

## Shared work process

Use the official organizer project locally in Bob; use this public repository for **safe, non-sensitive documentation** and collaboration notes. Reports live in the team's **Skore Hub** workspace. One change at a time, meaningful commit messages, short reviews, and an evidence-based final report. GitHub issues hold the work queue.

## Timeline

- **14 Oct 2026:** online competition session, **08:15–12:00 CEST**; official Kaggle submission deadline **12:00**.
- **20 Oct 2026, 18:00 CEST:** video and repository/code delivery on DVL. The kickoff PDF also mentions a ZIP due **14 Oct at noon**; verify that requirement now.

## Boundaries

The data and competition outputs have restricted use. Keep all four competition CSVs on **authorized local teammate systems** only. Never publish data, labels, predictions, API keys, or private reports in this public GitHub repository.

*The team will add only verified outcomes and claims supported by its own Bob/skore records. No leaderboard rank or final model performance is claimed yet.*
