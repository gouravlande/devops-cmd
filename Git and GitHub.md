# Git and GitHub Commands & Notes

## What is Git?

Git is a distributed version control system used to:
- Track code changes
- Manage project versions
- Collaborate with teams
- Restore previous versions of code

Git helps developers manage source code efficiently.

---

# What is GitHub?

GitHub is a cloud-based platform used to:
- Store Git repositories online
- Collaborate with developers
- Share code
- Manage projects

GitHub works with Git.

---

# Difference Between Git and GitHub

| Git | GitHub |
|---|---|
| Version control tool | Cloud hosting platform |
| Installed locally | Web-based platform |
| Tracks changes | Stores repositories online |
| Command-line tool | Collaboration platform |

---

# Why Use Git?

Without Git:
- Code can be lost
- Difficult collaboration
- No version history
- Hard to track changes

Git solves these problems.

---

# Git Workflow

```text
Working Directory
        ↓
Staging Area
        ↓
Local Repository
        ↓
Remote Repository (GitHub)
```

---

# Install Git

## Ubuntu

```bash
sudo apt update
sudo apt install git -y
```

---

# Check Git Version

```bash
git --version
```

---

# Configure Git

Set username:

```bash
git config --global user.name "Your Name"
```

Set email:

```bash
git config --global user.email "yourmail@gmail.com"
```

Check configuration:

```bash
git config --list
```

---

# Git Basic Commands

---

# Initialize Git Repository

```bash
git init
```

Creates a local Git repository.

---

# Check Repository Status

```bash
git status
```

Shows:
- Modified files
- Staged files
- Untracked files

---

# Add Files to Staging Area

Add single file:

```bash
git add filename
```

Add all files:

```bash
git add .
```

---

# Commit Changes

```bash
git commit -m "Initial Commit"
```

Commit means:
> Save snapshot/version of code.

---

# View Commit History

```bash
git log
```

Short version:

```bash
git log --oneline
```

---

# Clone Repository

```bash
git clone repository_url
```

Example:

```bash
git clone https://github.com/user/repo.git
```

---

# Branching in Git

Branches allow parallel development.

---

# Create Branch

```bash
git branch branch_name
```

---

# View Branches

```bash
git branch
```

---

# Switch Branch

```bash
git checkout branch_name
```

---

# Create and Switch Branch

```bash
git checkout -b branch_name
```

---

# Merge Branch

```bash
git merge branch_name
```

---

# Delete Branch

```bash
git branch -d branch_name
```

---

# Remote Repository Commands

---

# Connect GitHub Repository

```bash
git remote add origin repository_url
```

Example:

```bash
git remote add origin https://github.com/user/repo.git
```

---

# View Remote Repositories

```bash
git remote -v
```

---

# Push Code to GitHub

```bash
git push origin main
```

---

# Pull Latest Changes

```bash
git pull origin main
```

---

# Fetch Latest Changes

```bash
git fetch
```

---

# GitHub Authentication

GitHub may require:
- Username
- Personal Access Token (PAT)

instead of password.

---

# Remove Files from Git

Remove tracked file:

```bash
git rm filename
```

---

# Undo Changes

Discard changes:

```bash
git checkout -- filename
```

---

# Reset Commit

Soft reset:

```bash
git reset --soft HEAD~1
```

Hard reset:

```bash
git reset --hard HEAD~1
```

---

# Stash Changes

Temporarily save changes:

```bash
git stash
```

Restore stash:

```bash
git stash pop
```

---

# Git Ignore

## What is .gitignore?

Used to ignore:
- Temporary files
- Virtual environments
- Secrets
- Logs

---

# Example .gitignore

```bash
venv/
__pycache__/
.env
*.log
```

---

# GitHub Important Concepts

| Concept | Description |
|---|---|
| Repository | Project storage |
| Fork | Copy of repository |
| Pull Request | Request to merge changes |
| Issue | Bug/task tracking |
| Star | Bookmark repository |

---

# GitHub Workflow

```text
Create Repository
       ↓
Clone Repository
       ↓
Add Files
       ↓
Commit Changes
       ↓
Push to GitHub
```

---

# GitHub Collaboration Flow

```text
Fork Repository
       ↓
Create Branch
       ↓
Make Changes
       ↓
Commit Changes
       ↓
Push Branch
       ↓
Create Pull Request
```

---

# GitHub Useful Commands Summary

| Command | Purpose |
|---|---|
| git init | Initialize repository |
| git status | Check status |
| git add . | Add files |
| git commit | Save changes |
| git push | Upload code |
| git pull | Download changes |
| git clone | Copy repository |
| git branch | Manage branches |
| git checkout | Switch branch |

---

# Advantages of Git & GitHub

- Version control
- Team collaboration
- Backup of code
- Easy rollback
- Open-source collaboration

---

# GitHub Best Practices

- Write meaningful commit messages
- Use branches
- Maintain README.md
- Use .gitignore
- Commit frequently

---

# Real-World Use Cases

- Software development
- DevOps pipelines
- Machine Learning projects
- Open-source contribution
- CI/CD integration

---

# GitHub in DevOps

GitHub is widely used for:
- Source code management
- CI/CD automation
- Collaboration
- Version control

Integrated with:
- Jenkins
- Docker
- Kubernetes
- GitHub Actions

---

# Learning Outcome

After learning Git & GitHub:
- You can manage projects efficiently
- Track code changes
- Collaborate with teams
- Work on DevOps and ML projects

---

# Recommended Next Topics

After Git & GitHub learn:
1. Linux
2. Docker
3. Jenkins
4. Kubernetes
5. GitHub Actions
6. CI/CD Pipelines

---

# Author

## Gourav Lande

Interested in:
- DevOps
- Cloud Computing
- AI Engineering
- MLOps

GitHub:
https://github.com/gouravlande

---

# Conclusion

Git and GitHub are essential tools for developers and DevOps engineers. They provide powerful version control, collaboration, and project management capabilities used in modern software development.
