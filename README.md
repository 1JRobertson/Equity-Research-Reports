# Repository Setup Guide

This repository currently contains project assets such as the *Equity Research Report.pdf*. If you want to create a brand-new GitHub repository and connect it to a folder on your local computer (for example, inside **Documents**), follow the steps below.

## 1. Create a new repository on GitHub
1. Log in to [github.com](https://github.com/).
2. Click **New** (usually found on your profile page or the repositories tab).
3. Fill in the repository name, description (optional), and choose whether it should be public or private.
4. Skip creating a README, `.gitignore`, or license for now (we will add files locally).
5. Click **Create repository** and leave the page open—you will need the remote URL displayed on the page (it looks like `https://github.com/USERNAME/REPO.git`).

## 2. Prepare a local folder (e.g., in Documents)
These commands assume you are using macOS or Linux. On Windows, run them inside **Command Prompt**, **PowerShell**, or **Git Bash**.

```bash
# go to your Documents folder
cd ~/Documents

# make a folder for the project (replace with a name you like)
mkdir my-scheduling-project
cd my-scheduling-project
```

If you already have files you want to keep, move or copy them into this folder before continuing.

## 3. Initialize Git and connect the GitHub repository
```bash
# initialize a new Git repository
git init

# add every file in the folder to the first commit
git add .

git commit -m "Initial commit"

# add the GitHub repository URL as the remote named "origin"
git remote add origin https://github.com/USERNAME/REPO.git
```

Replace `https://github.com/USERNAME/REPO.git` with the URL you copied from GitHub in step 1.

## 4. Push your local content to GitHub
```bash
# push the commit to the main branch on GitHub
git branch -M main
git push -u origin main
```

You will be prompted to sign in. Use a personal access token (PAT) if GitHub requires one instead of your password.

## 5. Keep your repository in sync
Whenever you make changes:

```bash
# check which files changed
git status

# stage the files you want to commit
git add <path/to/file>

# save the changes locally
git commit -m "Describe what changed"

# upload to GitHub
git push
```

If you collaborate on the repository or switch computers, pull the latest changes before working:

```bash
git pull
```

## Troubleshooting
- **Git not installed?** Install it from [git-scm.com](https://git-scm.com/downloads).
- **Permission denied when pushing?** Make sure you are authenticated. You might need to set up SSH keys or generate a PAT.
- **Wrong remote URL?** Update it with `git remote set-url origin <new-url>`.

Feel free to adjust folder names and commit messages to match your project. These steps keep your files tidy and backed up to GitHub.
