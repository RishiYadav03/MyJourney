# Git & GitHub Interview Questions - Day 1

## Q1. What is Git?

Git is a distributed version control system used to track changes in code and collaborate with other developers.

---

## Q2. What is GitHub?

GitHub is a cloud-based platform used to host Git repositories and manage code online.

Git = Version Control Tool

GitHub = Online Platform for Git Repositories

---

## Q3. What is the difference between Git and GitHub?

Git:

* Installed on local machine
* Tracks code changes

GitHub:

* Stores repositories online
* Used for collaboration and backup

---

## Q4. What is a Repository?

A repository (repo) is a project folder tracked by Git.

It contains:

* Source code
* Documentation
* Commit history

Example:

developer-journey-2026

---

## Q5. What does `git status` do?

Command:

```bash
git status
```

Purpose:

Shows:

* Modified files
* New files
* Staged files
* Branch information

---

## Q6. What does `git add .` do?

Command:

```bash
git add .
```

Purpose:

Adds all changed files to the staging area.

The `.` means:

Current folder and all subfolders.

---

## Q7. What is a Commit?

A commit is a saved checkpoint of your project.

It records:

* What changed
* Who changed it
* When it was changed

Example:

```bash
git commit -m "Added JavaScript notes"
```

---

## Q8. What does `git push` do?

Command:

```bash
git push
```

Purpose:

Uploads local commits to GitHub.

Flow:

Local Computer
↓
Commit
↓
Push
↓
GitHub

---

## Q9. What does `git pull` do?

Command:

```bash
git pull
```

Purpose:

Downloads the latest changes from GitHub to your local machine.

---

## Q10. What does `git clone` do?

Command:

```bash
git clone <repository-url>
```

Purpose:

Downloads a repository from GitHub to your computer.

Usually used when working on a project for the first time.

---

## Q11. What is the staging area?

The staging area is where files are prepared before creating a commit.

Example:

```bash
git add .
```

moves files into the staging area.

```bash
git commit -m "message"
```

saves them permanently in Git history.

---

## Q12. Explain the Git workflow.

Step 1:

```bash
git status
```

Check changes.

Step 2:

```bash
git add .
```

Stage files.

Step 3:

```bash
git commit -m "message"
```

Create checkpoint.

Step 4:

```bash
git push
```

Upload to GitHub.

This is the most common Git workflow used by developers.
