# Git & GitHub Notes

## Status
✅ Completed

---

# What is Git?

Git is a **Distributed Version Control System (VCS)**.

It helps developers:

- Track changes in code.
- Work with multiple developers.
- Maintain different versions of a project.
- Restore older versions if needed.
- Backup source code.

Think of Git as a **time machine for your code**.

---

# What is a Repository (Repo)?

A repository is a folder that stores:

- Project files
- Complete history of changes
- Commits
- Branches

Every Git repository contains a hidden folder called:

```bash
.git
```

which stores all Git information.

---

# Why Git is Important

Git is used by:

- Google
- Microsoft
- Apple
- Meta
- Open-source projects
- Individual developers

Git is an essential skill for almost every software developer.

---

# Key Features of Git

- Distributed Version Control
- Decentralized
- Fast and efficient
- Tracks file history
- Supports collaboration
- Branching & Merging
- Works offline
- Open Source
- Uses SHA-1 hashing for data integrity

---

# Git vs GitHub

## Git

- Version Control System
- Installed on your computer
- Tracks code changes
- Works offline

## GitHub

- Cloud platform
- Hosts Git repositories
- Enables collaboration
- Stores remote repositories
- Provides Issues, Pull Requests, Actions, Wikis and more

**Remember**

```
Git = Version Control Tool

GitHub = Website that hosts Git repositories
```

---

# Install Git

Check if Git is installed:

```bash
git --version
```

Download Git:

https://git-scm.com

---

# Configure Git

Set username:

```bash
git config --global user.name "Your Name"
```

Set email:

```bash
git config --global user.email "you@example.com"
```

Every commit records this information.

---

# Git Workflow

```
Working Directory
        ↓
Staging Area
        ↓
Local Repository
        ↓
Remote Repository (GitHub)
```

---

# Working Directory

The place where you create and edit files.

Nothing is saved in Git until you stage and commit.

---

# Staging Area

Temporary area where files are prepared before committing.

Command:

```bash
git add
```

---

# Local Repository

Stores commits on your computer.

Command:

```bash
git commit
```

---

# Remote Repository

Online repository hosted on:

- GitHub
- GitLab
- Bitbucket

Command:

```bash
git push
```

---

# Basic Git Workflow

## 1. Initialize Repository

```bash
git init
```

Creates a hidden:

```bash
.git
```

folder.

---

## 2. Check Status

```bash
git status
```

Shows:

- Modified files
- Untracked files
- Staged files

---

## 3. Stage Files

Single file:

```bash
git add filename
```

All files:

```bash
git add .
```

Moves files into the staging area.

---

## 4. Commit Changes

```bash
git commit -m "Initial commit"
```

Creates a snapshot of your project.

Good commit messages:

```
Initial commit
Add login page
Fix navbar bug
Update README
```

---

## 5. View Commit History

```bash
git log
```

Displays:

- Commit ID
- Author
- Date
- Commit message

---

# Create a GitHub Repository

1. Login to GitHub.
2. Click **New Repository**.
3. Choose:
   - Public
   - Private
4. Create Repository.

---

# Connect Local Repository to GitHub

```bash
git remote add origin REPOSITORY_URL
```

`origin` is the default name of the remote repository.

---

# Push Code

First push:

```bash
git push -u origin main
```

Future pushes:

```bash
git push
```

---

# Pull Changes

```bash
git pull
```

Downloads the latest changes from GitHub.

Use it when:

- Someone else updated the repository.
- You changed files directly on GitHub.

---

# Clone Repository

```bash
git clone REPOSITORY_URL
```

Creates a complete copy of a repository on your computer.

---

# Branches

Branches allow you to work without affecting the main project.

Useful for:

- New features
- Bug fixes
- Experiments

Example:

```
main

feature/login

feature/payment

bug/navbar
```

---

# Create a Branch

```bash
git checkout -b feature/login
```

Creates and switches to the branch.

---

# View Branches

```bash
git branch
```

Lists all local branches.

---

# Switch Branch

```bash
git checkout main
```

Moves to another branch.

---

# Merge Branch

```bash
git merge feature/login
```

Combines another branch into the current branch.

---

# Delete Branch

```bash
git branch -d feature/login
```

Deletes the branch after merging.

---

# Pull Request (PR)

A Pull Request is a request to merge changes into another branch.

Typical workflow:

```
Create Branch
      ↓
Make Changes
      ↓
Commit
      ↓
Push
      ↓
Open Pull Request
      ↓
Review
      ↓
Merge
```

---

# README.md

README is the homepage of a repository.

Usually contains:

- Project description
- Features
- Installation
- Usage
- Screenshots
- License
- Author

README files use **Markdown**.

---

# Markdown Basics

Heading:

```md
# Heading
```

Subheading:

```md
## Heading
```

Bullet List:

```md
- Item
```

Code Block:


# .gitignore File

A `.gitignore` file tells Git which files and folders should **NOT** be uploaded to GitHub.

This is one of the most important files in any project because it protects sensitive or unnecessary files.

---

## Why use .gitignore?

Without a `.gitignore`, Git will upload everything you add.

Some files should never be pushed to GitHub, such as:

- API keys
- Passwords
- Environment variables
- Build files
- Dependency folders
- Temporary files
- OS-generated files

---

## Common Examples

```text
.env
node_modules/
dist/
build/
.vscode/
.idea/
*.log
```

---

## Example

Suppose your project contains:

```text
Project
│
├── index.html
├── style.css
├── script.js
├── .env
├── node_modules/
└── README.md
```

Your `.gitignore` could look like:

```text
.env
node_modules/
```

Git will upload:

- index.html
- style.css
- script.js
- README.md

Git will ignore:

- .env
- node_modules/

---

## Why is .env ignored?

A `.env` file usually contains secret information such as:

```text
API_KEY=123456789
DATABASE_PASSWORD=password123
SECRET_TOKEN=abcd1234
```

If you upload it to a public repository, anyone can see your secrets.

Always ignore `.env`.

---

## After Creating .gitignore

Save the file.

Then continue the normal workflow:

```bash
git add .
git commit -m "Add .gitignore"
git push
```

Only files that are **not ignored** will be uploaded.

---

# Commit Shortcuts

Instead of typing two commands:

```bash
git add .
git commit -m "Added Login Page"
```

you can use:

```bash
git commit -am "Added Login Page"
```

### Important

`git commit -am` only works for files that Git is already tracking.

It **does not** stage newly created files.

If you created a brand-new file, you must first use:

```bash
git add filename
```

or

```bash
git add .
```

---

# GitHub Interface Basics

A GitHub repository contains several tabs.

## Code

Shows:

- Files
- Folders
- Branches
- Latest commits

This is the main page of your repository.

---

## Commits

Every commit is saved permanently.

Clicking a commit lets you see:

- What changed
- Which lines were added
- Which lines were removed
- When it happened
- Who made it

GitHub keeps the complete history of every project.

---

## Issues

Used to report:

- Bugs
- Problems
- Feature requests
- Improvements

Example:

```
Issue:
Login button doesn't work.
```

Developers can discuss and close issues after fixing them.

---

## Pull Requests

A Pull Request (PR) is a request to merge one branch into another.

Typical workflow:

```
Create Branch
      ↓
Write Code
      ↓
Commit
      ↓
Push
      ↓
Open Pull Request
      ↓
Review
      ↓
Merge
```

Large companies use Pull Requests for code reviews before changes become part of the main project.

---

## Actions

GitHub Actions allows you to automate tasks.

Examples:

- Run tests automatically
- Build the project
- Deploy the project
- Check code quality

This is part of CI/CD (Continuous Integration and Continuous Deployment).

---

## Projects

GitHub Projects is a built-in project management tool.

It can track:

- Tasks
- Features
- Bugs
- Progress

Similar to a Kanban board.

---

## Wiki

A Wiki is extra documentation for a project.

Useful for:

- Tutorials
- Guides
- Architecture
- FAQs

---

## Insights

Shows repository statistics such as:

- Contributors
- Commits
- Traffic
- Activity
- Languages used

---

## Settings

Repository settings allow you to:

- Change repository name
- Make repository Public or Private
- Delete repository
- Archive repository
- Add collaborators
- Manage security

---

# Downloading a Repository

There are two ways.

## Download ZIP

Click:

```
Code → Download ZIP
```

Useful if you only want the files.

Not recommended for active development.

---

## Clone Repository

```bash
git clone REPOSITORY_URL
```

Creates a complete Git repository on your computer.

Unlike a ZIP download, cloning preserves:

- Commit history
- Branches
- Remote connection

This is the recommended method.

---

# SSH Keys

SSH allows GitHub to recognize your computer securely.

Instead of typing your password every time, Git uses SSH authentication.

---

## Generate SSH Key

```bash
ssh-keygen
```

or

```bash
ssh-keygen -t rsa -b 4096
```

Git creates:

```
Private Key
Public Key
```

Never share the private key.

Only upload the public key to GitHub.

---

## Test SSH Connection

```bash
ssh -T git@github.com
```

If successful, GitHub confirms your identity.

---

# Branching

A branch is an independent copy of your project.

Branches allow developers to work without affecting the main code.

Example:

```
main

feature/login

feature/payment

bug/navbar
```

Each branch has its own changes.

---

## Create a Branch

```bash
git checkout -b feature/login
```

Creates the branch and switches to it.

---

## View Branches

```bash
git branch
```

Shows all local branches.

---

## Switch Branch

```bash
git checkout main
```

Moves to another branch.

---

## Make Changes

Edit files normally.

Then:

```bash
git add .
git commit -m "Added Login Page"
```

---

## Push Branch

```bash
git push -u origin feature/login
```

Uploads the branch to GitHub.

---

# Pull Requests

After pushing a branch, GitHub allows you to create a Pull Request.

A Pull Request asks:

> "Can my changes be merged into the main branch?"

Repository owners review the code before merging.

---

# Merge

After approval:

```
feature/login
        ↓
Merge
        ↓
main
```

The feature becomes part of the main project.

---

## Merge Locally

```bash
git merge feature/login
```

Combines another branch into the current branch.

---

## Delete Branch

Remote:

Delete from GitHub after merging.

Local:

```bash
git branch -d feature/login
```

Deletes the branch from your computer.

---

# CI/CD (Continuous Integration & Continuous Deployment)

CI/CD automates software delivery.

Typical pipeline:

```
Write Code
      ↓
Push to GitHub
      ↓
GitHub Actions runs
      ↓
Tests
      ↓
Build
      ↓
Deploy
```

Benefits:

- Faster deployment
- Automatic testing
- Fewer mistakes

---

# Vercel Deployment

The video demonstrates deploying a project using **Vercel**.

Workflow:

```
Push Code to GitHub
        ↓
Vercel detects new commit
        ↓
Automatically builds project
        ↓
Deploys website
```

Every future `git push` automatically updates the deployed website.

---

# Key Takeaways

- `.gitignore` protects sensitive files.
- Never upload `.env` or API keys.
- GitHub provides tools beyond storing code (Issues, Pull Requests, Actions, Projects, Wiki).
- Clone repositories instead of downloading ZIPs when developing.
- SSH provides secure authentication with GitHub.
- Branches let you develop features safely.
- Pull Requests are the standard way to merge code.
- CI/CD automates testing and deployment.
- Services like Vercel can deploy websites automatically whenever you push new code.
