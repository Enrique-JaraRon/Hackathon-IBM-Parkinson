# Team collaboration — public repo, Bob credits, shared Skore Hub

## Golden rule

This repository is **public**: publish only public-safe commentary, process documentation, and generic templates. The actual competition training tables / hidden predictions / credentials / sensitive reports **stay off GitHub**. A Git `.gitignore` is useful but **not a substitute for reviewing every `git add`**.

## Responsibilities (assign names in team chat)

| Role | Tasks | Evidence |
|---|---|---|
| Captain / Kaggle operator | Timeboxing, rule checks, final valid Kaggle submission | official Kaggle row + matching Hub URL (privately recorded) |
| Bob/skore operator | Runs authorized experiments and saves reports | Bob history and EstimatorReport |
| Methodology + documentation reviewer | Checks patient grouping, reproducibility, methodology, narratives | reviewed docs and validation tables |
| Video + delivery owner | Records and edits video, manages ZIP and DVL confirmations | ≤5-minute final recording and DVL receipt |

Roles can rotate; everyone should understand RMSE, GroupKFold, target, and leakage.

## Credit-conscious protocol

1. **Before each Bob request**: identify a single question, check the existing experiment journal, define what result counts as success, and ensure the task is permitted by the organizers.
2. Reuse official docs and built-in installed Bob skills, rather than paying credits to rediscover setup.
3. Run at most **one primary new experiment at a time**, and record output before changing anything.
4. Another teammate can simultaneously write non-data documentation, analyze official learning material, or prepare video assets **without consuming Bob calls**.
5. After each session, save *the question, exact validation protocol, final metrics, report key, artifacts, and next task* in a handoff note.
6. Avoid repeating models, large blind searches, untracked feature changes, and public-leaderboard chasing.

## Team GitHub workflow (documentation only while public)

- Each member: clone this public project to a **separate clean folder**, NOT inside the organizer's Git history.
- Create a branch (`docs/<member>-<topic>`) and commit only reviewed Markdown / authorized files.
- Open a pull request; another teammate checks confidentiality, truthfulness and typos before merge.
- Leave the **four organizer CSV files** and actual Kaggle predictions in the approved local Bob project; do not copy the organizer project's `.git` into this repository.
- Use **Skore Hub** for experiment reports, not GitHub.

## Before changing to private

Public is the team's current preference. Making the repository private would reduce exposure, but **still would not by itself authorize copying restricted data**. Only teammates who accepted competition terms may access such data.

## Handoff format

See [HANDOFF.md](HANDOFF.md). One report key per Kaggle CSV, never silently overwrite the prior artifact.
