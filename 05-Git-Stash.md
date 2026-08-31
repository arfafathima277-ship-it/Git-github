# Git Stash

## What is Git Stash?

Git Stash is a feature that temporarily saves your uncommitted changes without committing them to the repository. It allows you to switch branches or work on another task and later restore your saved changes.

In simple words, Git Stash acts like a temporary storage area for your unfinished work.


---

## Why Do We Use Git Stash?

Suppose you are working on a feature branch and suddenly receive a high-priority bug to fix on another branch.

You cannot switch branches because you have uncommitted changes.

Instead of committing incomplete work, you can use Git Stash to save your changes temporarily, switch branches, complete the urgent task, and then restore your previous work.

---

## Git Stash Workflow

```
Working Directory
       │
       ▼
git stash
       │
       ▼
Changes saved temporarily
       │
Switch Branch
       │
Complete another task
       │
Return to previous branch
       │
git stash pop
       │
       ▼
Changes restored
```

---

# Common Git Stash Commands

## Save Current Changes

```bash
git stash
```

Temporarily saves all tracked changes.

---

## View Stashed Changes

```bash
git stash list
```

Displays all saved stashes.

Example:

```
stash@{0}: WIP on feature-login
stash@{1}: WIP on main
```

---

## Restore Latest Stash

```bash
git stash pop
```

Restores the latest stash and removes it from the stash list.

---

## Restore Without Removing

```bash
git stash apply
```

Restores the stash but keeps it in the stash list.

---

## Delete Latest Stash

```bash
git stash drop
```

Deletes the most recent stash.

---

## Delete All Stashes

```bash
git stash clear
```

Removes all saved stashes.

---

## Stash Including Untracked Files

```bash
git stash -u
```

or

```bash
git stash --include-untracked
```

Saves both tracked and untracked files.

---

## Give a Name to a Stash

```bash
git stash save "Login Page Changes"
```

or (recommended)

```bash
git stash push -m "Login Page Changes"
```

Adds a meaningful message to the stash.

---

# Real-Time Example

You are developing a login page.

```
login.html
login.css
login.js
```

Before completing your work, your manager asks you to fix a production issue.

Instead of committing incomplete code:

```bash
git stash
```

Switch to the production branch:

```bash
git checkout main
```

Fix the issue and push your changes.

Return to your feature branch:

```bash
git checkout feature-login
```

Restore your previous work:

```bash
git stash pop
```

Continue working where you left off.

---

# Advantages of Git Stash

- Saves unfinished work temporarily
- No need to create unnecessary commits
- Makes branch switching easier
- Helps handle urgent production fixes
- Keeps commit history clean

---

# Interview Questions

## What is Git Stash?

Git Stash is used to temporarily save uncommitted changes so you can switch branches or work on another task without committing incomplete work.

---

## Why is Git Stash used?

Git Stash is used when you want to temporarily store your current changes without creating a commit.

---

## Difference Between git stash pop and git stash apply

| git stash pop | git stash apply |
|----------------|-----------------|
| Restores changes | Restores changes |
| Removes stash after restoring | Keeps the stash |
| Used when you no longer need the stash | Used when you may need the stash again |

---

## Difference Between Commit and Stash

| Commit | Stash |
|---------|-------|
| Permanent | Temporary |
| Saved in Git history | Not saved in commit history |
| Can be pushed to remote | Cannot be pushed |
| Used for completed work | Used for unfinished work |

---

# Summary

- Git Stash temporarily saves uncommitted changes.
- It allows developers to switch branches without committing incomplete work.
- `git stash` saves changes.
- `git stash list` displays saved stashes.
- `git stash pop` restores and removes the stash.
- `git stash apply` restores the stash without removing it.
- `git stash clear` deletes all stashes.
