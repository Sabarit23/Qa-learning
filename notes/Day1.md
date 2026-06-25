# Git & GitHub Learning Notes

## ✅ What is Git?

**Git** is a Version Control System (VCS) that helps developers track changes in code over time.

### Why Git is Used?

* Track code changes
* Maintain version history
* Collaborate with team members
* Restore previous versions if something breaks
* Manage multiple features simultaneously

### Example

Without Git:

```text
project_final.zip
project_final_v2.zip
project_final_latest.zip
project_final_latest_final.zip
```

With Git:

```text
Version 1
Version 2
Version 3
```

Git automatically manages all versions.

---

## ✅ What is GitHub?

**GitHub** is a cloud-based platform that hosts Git repositories online.

### Uses of GitHub

* Store code online
* Backup projects
* Collaborate with teams
* Review code changes
* Build a portfolio

### Simple Understanding

| Git                         | GitHub                     |
| --------------------------- | -------------------------- |
| Tracks code changes locally | Stores code online         |
| Installed on your system    | Web platform               |
| Version Control Tool        | Repository Hosting Service |

---

## ✅ Difference Between Git and GitHub

| Git                  | GitHub                       |
| -------------------- | ---------------------------- |
| Software             | Web Platform                 |
| Works locally        | Works online                 |
| Tracks code history  | Hosts repositories           |
| No internet required | Internet required            |
| Command-line tool    | Website & collaboration tool |

---

# Basic Git Workflow

```text
Modified Files (Working Directory)
        ↓
     git add
        ↓
   Staging Area
        ↓
   git commit
        ↓
 Local Repository
        ↓
    git push
        ↓
GitHub Repository (Remote Repository)
```

---

# ✅ git clone

### Purpose

Download a GitHub repository to your local machine.

### Syntax

```bash
git clone <repository-url>
```

### Example

```bash
git clone https://github.com/username/qa-learning.git
```

---

# ✅ git status

### Purpose

Check the current status of files.

### Command

```bash
git status
```

### Example Output

```bash
On branch main

Modified:
notes.txt

Untracked:
api_collection.json
```

### Status Meaning

| Status    | Meaning               |
| --------- | --------------------- |
| Untracked | New file              |
| Modified  | Existing file changed |
| Staged    | Ready for commit      |

---

# ✅ git add

### Purpose

Move files to the staging area before committing.

### Add Single File

```bash
git add notes.txt
```

### Add All Files

```bash
git add .
```

---

# ✅ git commit

### Purpose

Save a snapshot of staged changes.

### Syntax

```bash
git commit -m "commit message"
```

### Example

```bash
git commit -m "Added Git notes"
```

Think of commit as:

```text
Save Game Progress
```

Every commit creates a checkpoint.

---

# ✅ git push

### Purpose

Upload local commits to GitHub.

### Syntax

```bash
git push origin main
```

### Example

```bash
git push origin main
```

---

# ✅ git pull

### Purpose

Download latest changes from GitHub to your local repository.

### Syntax

```bash
git pull origin main
```

### Example

```bash
git pull origin main
```

Use this before starting work to ensure you have the latest code.

---

# ✅ Branches

Branches allow developers to work on features independently without affecting the main code.

### Why Use Branches?

```text
main
 |
 ├── Feature A
 ├── Feature B
 └── Bug Fix
```

Multiple developers can work simultaneously.

---

## Create a Branch

```bash
git branch feature-login
```

or

```bash
git switch -c feature-login
```

---

## View Branches

```bash
git branch
```

Example:

```bash
* main
  feature-login
```

`*` indicates the current branch.

---

## Switch Branch

```bash
git switch feature-login
```

or

```bash
git checkout feature-login
```

---

## Delete Branch

```bash
git branch -d feature-login
```

---

# ✅ Basic Merge Workflow

### Scenario

Create a login feature and merge it into main.

### Step 1: Create Branch

```bash
git switch -c feature-login
```

### Step 2: Make Changes

Create or modify files.

---

### Step 3: Add Changes

```bash
git add .
```

---

### Step 4: Commit Changes

```bash
git commit -m "Added login functionality"
```

---

### Step 5: Switch to Main

```bash
git switch main
```

---

### Step 6: Merge Branch

```bash
git merge feature-login
```

---

### Step 7: Push Changes

```bash
git push origin main
```

---

### Merge Workflow Diagram

```text
main
 |
 └── feature-login
       |
       ├── Changes
       ├── Commit
       |
       └── Merge Back
              ↓
            main
```

---

# ✅ Pull Request (PR) Concept

In real companies, developers generally do not merge directly into the main branch.

Instead, they create a Pull Request (PR).

### Workflow

```text
Create Branch
      ↓
Make Changes
      ↓
Commit Changes
      ↓
Push Branch
      ↓
Create Pull Request
      ↓
Code Review
      ↓
Approval
      ↓
Merge to Main
```

---

### Example

Push feature branch:

```bash
git push origin feature-login
```

Then on GitHub:

```text
Compare & Pull Request
          ↓
Reviewer Checks Code
          ↓
Approve
          ↓
Merge
```

---

### Why Pull Requests Are Used?

* Code review
* Quality checks
* Team collaboration
* Prevent bugs from entering main
* Maintain coding standards

---

# ✅ Complete Git Workflow (Most Important)

```bash
# Clone repository
git clone <repository-url>

# Check status
git status

# Add files
git add .

# Commit changes
git commit -m "Added new feature"

# Push changes
git push origin main

# Pull latest changes
git pull origin main
```

---

# ✅ Industry Workflow Example

```bash
# Pull latest code
git pull origin main

# Create branch
git switch -c feature-login

# Make changes

# Add changes
git add .

# Commit changes
git commit -m "Added login page"

# Push branch
git push origin feature-login

# Create Pull Request on GitHub

# After approval, merge PR

# Pull latest main branch
git pull origin main
```

---

# ✅ Practice Project Structure

Create a repository:

```text
qa-learning
```

Inside it:

```text
qa-learning/
│
├── Git/
│   └── notes.md
│
├── API/
│   └── postman_notes.md
│
├── SQL/
│   └── queries.sql
│
└── Automation/
    └── selenium_notes.md
```

Practice the following sequence repeatedly:

```bash
git clone
git status
git add .
git commit -m "message"
git push
git pull
git branch
git switch
git merge
```

By completing these topics, you'll have a solid foundation in Git and GitHub and be ready to move on to advanced topics such as GitHub Actions, CI/CD pipelines, and team-based development workflows.
