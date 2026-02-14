# Day 22 – Git Fundamentals Notes

## 1. Difference between git add and git commit

git add moves changes to the staging area.
git commit saves staged changes as a snapshot in history.

---

## 2. What does the staging area do?

The staging area allows selective commits.
It lets you review and control what goes into the next snapshot.
Without it, Git would commit everything automatically.

---

## 3. What does git log show?

It shows:
- Commit hash
- Author
- Date
- Commit message

---

## 4. What is the .git folder?

The .git folder stores:
- Commit history
- Branches
- Objects
- Configuration

If deleted, all version history is lost.

---

## 5. Working Directory vs Staging Area vs Repository

Working Directory:
Where you edit files.

Staging Area:
Where you prepare changes before commit.

Repository:
Where committed snapshots are stored permanently.
