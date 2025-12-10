# Git & GitHub Quick Guide

A concise reference for the most common Git and GitHub commands.

## 1. Configure Git
- Set username (local): `git config user.name "Your Name"`
- Set username (global): `git config --global user.name "Your Name"`
- Set email (local): `git config user.email "your_email@example.com"`
- Set email (global): `git config --global user.email "your_email@example.com"`
- Show configuration: `git config --list`

## 2. Basic Workflow
- Initialize repository: `git init`
- Stage files:  
  - One file: `git add filename.ext`  
  - All files: `git add .`
- Commit changes: `git commit -m "Message"`
- Check status: `git status`
- View history:  
  - Full: `git log -v`  
  - Short: `git log --oneline --graph --decorate`
- Check differences: `git diff`

## 3. Branches
- Create branch: `git branch feature-branch`
- Create & switch: `git checkout -b feature-branch`
- Switch branches: `git checkout main`
- Previous branch: `git switch -`
- **HEAD** → pointer to current commit and branch.

## 4. Checkout Older Commits
- Show IDs: `git log --oneline`
- Checkout commit: `git checkout COMMIT_ID`
- Return to latest: `git checkout main`

## 5. Merging
- Create experiment branch: `git checkout -b experiment`
- After changes → go to main: `git checkout main`
- Merge: `git merge experiment`

## 6. Remote Repositories (GitHub)
- Add remote: `git remote add origin https://github.com/user/repo.git`
- Show remotes: `git remote -v`
- Fetch: `git fetch origin`
- Pull: `git pull`
- Push (first time): `git push -u origin branch-name`
- Push (next times): `git push`

## 7. GitHub Workflow
1. Create a GitHub account  
2. Create a new repository  
3. Link local project:
