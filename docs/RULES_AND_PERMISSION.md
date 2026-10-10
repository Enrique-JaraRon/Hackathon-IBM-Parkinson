# Eligibility, authoring provenance and AI permission

## Competition rules originally published

The Kaggle rules originally supplied for **bobathon-esilv** say:
- Bob IDE / Bob CLI is the **only coding agent and submission-code environment**.
- `skore` is required for evaluation, reports and tracking.
- The Kaggle CSV must be generated in the allowed toolchain, and the Submission Description must link to its matching EstimatorReport URL on Skore Hub.
- No external training data, target-label scraping, third-party team predictions, or unauthorized Kaggle Notebooks.
- Competition data use is limited to the competition and authorized team members.

## Reported professor authorization (unverified wording)

The team states that a professor explicitly allowed all forms of help from ChatGPT, Gemini, Claude and other AI assistants due to Bob credit limits. **The exact message has not been supplied or independently authenticated here.**

This creates an unresolved conflict with the **published Kaggle-specific Bob-only coding-agent rule**. Ask the person empowered to set competition eligibility, in writing:

1. Does the professor's authorization explicitly **override the Kaggle competition's Bob-only authorship restriction**?
2. Is external-AI-produced executable source code eligible for the official leaderboard if later run in Bob?
3. Is help permitted for code, experiment design, documentation and video, and must external assistance be declared?
4. Do the remaining conditions (Bob runtime, skore report, CSV generation, patient holdout, four data files) remain mandatory?

Do **not** misstate who authored code or pass external-agent-written scripts through Bob while claiming Bob wrote them. Disclose provenance truthfully in any reporting required by the organizers.

## Public GitHub safeguard

Never commit competition tables, visit-level rows, Kaggle prediction CSVs, non-public files, `.skore`, API keys, authorization URLs, or secret environment files to this public repository.

For every *actual* Kaggle submission keep privately: model/report key, matching CSV path, EstimatorReport URL, Kaggle row/URL, exact toolchain, operator, and time.

Course learning, explanations, manuscript/video preparation, and public-source documentation can proceed immediately while eligibility is clarified.
