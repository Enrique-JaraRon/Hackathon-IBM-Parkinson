# Five-minute video: English script draft (replace all placeholders)

**Do not record the bracketed sections as if they are facts.** Complete this script with real evidence after the workshop. A dry run determines final timing.

## 0:00–1:10 — Challenge & Learning — Speaker A

Our challenge was to predict an unbiased OFF motor score for visits from people affected by Parkinson's disease. The OFF score helps describe movement difficulties when the beneficial effect of medication is no longer present. In the provided synthetic data, observed clinical scores are imperfect: they depend on medication timing, on the assessor, and on which examinations were performed.

We had to solve a regression problem, measured by RMSE. The central lesson was that we could not split visits at random. One patient could have several visits, so the model might otherwise encounter that person during both training and validation. We learned why patient-grouped evaluation matters for honest generalization.

## 1:10–2:20 — IBM Bob Usage — Speaker B

We used IBM Bob to work through the guided laboratory workflow, starting with data exploration. Bob helped organize our code and use the installed lab skills. We used skore reports to inspect model evaluation rather than relying on a single metric printed to the terminal.

In the initial phase, we confirmed the environment with seven passing setup checks and obtained a Dummy baseline with RMSE 16.83 on one patient-grouped holdout. **[AFTER EVENT: explain a real technical obstacle, the action taken with Bob, and its observed outcome; show an authentic screenshot.]** This helped us understand where the assistant added value, and where careful human review was still essential.

## 2:20–3:30 — Technical Continuity — Speaker C

The most reusable part of this project was the workflow: organize the data, record assumptions, check that validation matches the real problem, track experiments, and document results. Our team coordinated public-safe notes on GitHub while keeping competition data and credentials out of public repositories. Skore Hub provided a shared space for experiment reports.

**[AFTER EVENT: describe which actual component or method the team expects to reuse, how the workflow changed during the challenge, and what would have been harder without Bob.]** These lessons will remain relevant in future machine-learning projects.

## 3:30–4:45 — Overall Experience — Speaker D

Our team divided the tasks between [ACTUAL RESPONSIBILITIES]. We had to balance the time available, computing and assistant credits, documentation quality, and validation reliability.

One difficulty was [ACTUAL PROBLEM]. We addressed it by [ACTUAL TEAM RESPONSE], with support from [STAFF / DOCUMENTATION ONLY IF TRUE]. What worked well was [VERIFIED POSITIVE ASPECT]; what we would improve is [SPECIFIC IMPROVEMENT]. The main experience taught us to explain our modeling decisions instead of treating a high score as proof that everything was correct.

## 4:45–4:55 — Closing — All / Speaker A

Our main takeaway: trustworthy machine learning requires clear assumptions, honest validation, and teamwork. **[ADD ACTUAL FINAL RESULT ONLY IF VERIFIED.]**

---

Record four separate takes and edit around real screenshots. If your natural reading exceeds 5:00, shorten it rather than speeding it up unnaturally.
