# Git & GitHub Basics

## What is Git?

Git is a version control system.

It helps us:

* Track changes in code
* Save checkpoints
* Restore previous versions
* Collaborate with other developers

Think of Git as a game save system.

Every commit is a save point.

---

## What is GitHub?

GitHub is an online platform that stores Git repositories.

Flow:

My Computer → Git → GitHub

Git tracks changes locally.

GitHub stores them online.

---

# Basic Git Commands

## 1. git status

```bash
git status
```

Shows the current state of the repository.

Use this command before every commit.

Example output:

```text
modified: notes/github-basics.md
```

Meaning:

Git has detected changes.

---

## 2. git add .

```bash
git add .
```

Adds all changed files to the staging area.

Think:

"I want Git to include these files in the next commit."

The dot (.) means:

Everything inside the current folder.

---

## 3. git commit -m

```bash
git commit -m "Day 1 - Git Basics"
```

Creates a save point.

Example:

```bash
git commit -m "Added JavaScript notes"
```

Good commit messages should describe what changed.

---

## 4. git push

```bash
git push
```

Uploads local commits to GitHub.

Flow:

Code Changes
↓
git add .
↓
git commit
↓
git push
↓
GitHub Updated

---

## 5. git pull

```bash
git pull
```

Downloads the latest changes from GitHub.

Useful when:

* Working on multiple devices
* Collaborating with others

---

## 6. git clone

```bash
git clone REPOSITORY_URL
```

Example:

```bash
git clone https://github.com/username/project.git
```

Downloads a GitHub repository to your computer.

Usually done only once.

---

# Daily Workflow

1. Make changes
2. Check status
3. Add files
4. Commit changes
5. Push to GitHub

Commands:

```bash
git status
git add .
git commit -m "Describe your work"
git push
```

---

# Example

Create:

```text
javascript/day-01/practice.js
```

Run:

```bash
git status
git add .
git commit -m "Day 1 - Variables and Strings"
git push
```

Changes are now saved on GitHub.

---

These commands cover most day-to-day Git usage.
