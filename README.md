# Git & GitHub Comprehensive Guide

This guide provides a detailed overview of the most common Git commands and GitHub workflow for version control and collaboration.

---

## 1. Configure Git

Before using Git, you should configure your username and email. You can set them globally (applies to all repositories) or locally (applies to current repository only).

- Set username (current repo):  
  ```bash
  git config user.name "Your Name"
  ```
- Set username (global):  
  ```bash
  git config --global user.name "Your Name"
  ```
- Set email (current repo):  
  ```bash
  git config user.email "your_email@example.com"
  ```
- Set email (global):  
  ```bash
  git config --global user.email "your_email@example.com"
  ```
- View current configuration:  
  ```bash
  git config --list
  ```

---

## 2. Initialize Repository & Basic Workflow

- Initialize a new Git repository in your project folder:  
  ```bash
  git init
  ```
- Add files to staging area:  
  - Single file:  
    ```bash
    git add filename.ext
    ```  
  - All changed files:  
    ```bash
    git add .
    ```
- Commit your changes with a message:  
  ```bash
  git commit -m "Write a clear commit message"
  ```
- Check status of files (modified / staged / untracked):  
  ```bash
  git status
  ```
- View commit history (verbose):  
  ```bash
  git log -v
  ```
- View short commit history graphically:  
  ```bash
  git log --oneline --graph --decorate
  ```
- Compare changes before committing:  
  ```bash
  git diff
  ```

---

## 3. Branches and HEAD

Branches allow you to work on different features or experiments without affecting the main code.

- Create a new branch without switching:  
  ```bash
  git branch feature-branch
  ```
- Create a new branch and switch to it:  
  ```bash
  git checkout -b feature-branch
  ```
- Switch to an existing branch (example: main):  
  ```bash
  git checkout main
  ```
- Switch back to the previous branch:  
  ```bash
  git switch -
  ```
- **HEAD** points to the current commit on the checked-out branch.  
  Example: `"HEAD -> main"` means you are on the latest commit of `main`.

---

## 4. Checkout Older Commits

- Show commits with short IDs:  
  ```bash
  git log --oneline
  ```
- Checkout a specific commit (detached HEAD state):  
  ```bash
  git checkout COMMIT_ID
  ```
- Return to the latest commit on the main branch:  
  ```bash
  git checkout main
  ```

---

## 5. Working with Feature Branches and Merging

- Create a branch for experiments to avoid touching `main`:  
  ```bash
  git checkout -b experiment
  ```
- Make edits and commit them on the `experiment` branch.
- Switch back to main:  
  ```bash
  git checkout main
  ```
- Merge changes from the experiment branch into main:  
  ```bash
  git merge experiment
  ```

---

## 6. Remote Repositories (GitHub)

- Add a remote repository (example for GitHub):  
  ```bash
  git remote add origin https://github.com/username/repo.git
  ```
- Show configured remotes:  
  ```bash
  git remote -v
  ```
- Fetch latest changes from remote (without merging):  
  ```bash
  git fetch origin
  ```
- Pull latest changes and merge into the current branch:  
  ```bash
  git pull
  git pull origin branch-name
  ```
- Push commits to remote (first time, set upstream):  
  ```bash
  git push -u origin branch-name
  ```
- Push commits for subsequent changes:  
  ```bash
  git push
  ```

---

## 7. Clone a Repository

To copy an existing repository from GitHub to your local machine:

```bash
git clone https://github.com/username/repo.git
```

This will create a folder named `repo` with all files and commit history. You can then navigate into the folder and start working:

```bash
cd repo
git status
```

---

## 8. Mini GitHub Workflow

1. Create a GitHub account: [https://github.com](https://github.com)  
2. Create a new repository:  
   - Choose repository name  
   - Public or Private  
   - Optionally add a README  
3. Link local project to GitHub:  
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/username/repo.git
   git push -u origin main
   ```

---

**Made with ❤️ by Ezzat 3mmar**
