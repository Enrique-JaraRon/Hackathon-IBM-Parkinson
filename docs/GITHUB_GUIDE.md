# GitHub collaboration — beginner's guide

Repository: https://github.com/Enrique-JaraRon/Hackathon-IBM-Parkinson

**Current visibility: PUBLIC.** Never upload any competition CSV, predictions, secret files, patient rows, or the organizer repository history. This public repository is only for prepared documentation and safe coordination.

## Invite teammates
Repository > Settings > Collaborators > Add people. The owner must accept GitHub's prompts and teammates must accept invitations. Each member needs a distinct GitHub account. The connected GitHub tool currently cannot issue these invitations automatically.

## Work from a separate folder

In PowerShell, choose a directory **outside** the existing Bob contest folder, then:
```powershell
git clone https://github.com/Enrique-JaraRon/Hackathon-IBM-Parkinson.git
cd Hackathon-IBM-Parkinson
git switch -c docs/my-task
```

Edit only non-sensitive text documentation. Review changes with `git status` and `git diff`, then:
```powershell
git add docs/ video/
git commit -m "docs: update learning notes"
git push -u origin docs/my-task
```

Open a GitHub Pull Request to `main`. Another teammate checks no sensitive files or misleading claims have been included.

## After teammates merge
```powershell
git switch main
git pull
```

**Do not run `git add .` blindly from the original `bobathon-esilv` folder.** Its organizer data and original Git history are outside the scope of this public documentation repository.

## GitHub vs Bob vs Skore
- GitHub = public-safe notes, tasks and reviewed files.
- Bob = official workspace for contest coding/experiments per published rules.
- Skore Hub = team experiment tracking and evidence.
- Kaggle = official ranking on hidden test labels.
