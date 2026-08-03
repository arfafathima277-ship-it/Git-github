# Git & GitHub Interview Questions

## 1. What is Git?

Git is a distributed version control system used to track changes in source code and collaborate with other developers.

---

## 2. What is GitHub?

GitHub is a cloud-based platform used to host Git repositories and collaborate on software projects.

---

## 3. Difference between Git and GitHub?

| Git | GitHub |
|-----|--------|
| Version Control System | Git Repository Hosting Platform |
| Works locally | Works on the cloud |
| Tracks code changes | Stores and shares repositories |

---

## 4. What is a repository?

A repository (repo) is a storage location that contains project files, commit history, and Git configuration.

---

## 5. What is a commit?

A commit is a snapshot of your project's changes at a specific point in time.

Example:

```bash
git commit -m "Initial commit"
```

---

## 6. What is the difference between git add and git commit?

**git add**
- Moves changes to the staging area.

**git commit**
- Saves staged changes to the repository.

---

## 7. What is the staging area?

The staging area is an intermediate space where changes are prepared before committing.

---

## 8. What is the difference between git fetch and git pull?

| git fetch | git pull |
|-----------|----------|
| Downloads changes | Downloads and merges changes |
| Doesn't modify local branch | Updates local branch |

---

## 9. What is the difference between git clone and git fork?

**git clone**
- Creates a local copy of a repository.

**Fork**
- Creates a copy of another user's repository on GitHub.

---

## 10. What is a branch?

A branch is an independent line of development used to work on new features or fixes without affecting the main code.

---

## 11. How do you create a new branch?

```bash
git branch feature-login
```

---

## 12. How do you switch branches?

```bash
git checkout feature-login
```

or

```bash
git switch feature-login
```

---

## 13. How do you create and switch to a branch in one command?

```bash
git checkout -b feature-login
```

---

## 14. What is merging?

Merging combines changes from one branch into another.

Example:

```bash
git merge feature-login
```

---

## 15. What is a merge conflict?

A merge conflict occurs when Git cannot automatically merge changes because the same lines were modified in different branches.

---

## 16. What is Git Rebase?

Git Rebase moves commits from one branch onto another, creating a cleaner project history.

Example:

```bash
git rebase main
```

---

## 17. What is Git Stash?

Git Stash temporarily saves uncommitted changes without creating a commit.

Example:

```bash
git stash
git stash pop
```

---

## 18. How do you check repository status?

```bash
git status
```

---

## 19. How do you view commit history?

```bash
git log
```

Compact version:

```bash
git log --oneline
```

---

## 20. How do you see the differences between file changes?

```bash
git diff
```

---

## 21. How do you undo the last commit without deleting changes?

```bash
git reset --soft HEAD~1
```

---

## 22. How do you discard local changes?

```bash
git restore file.txt
```

---

## 23. How do you remove an untracked file?

```bash
git clean -f
```

---

## 24. What is the purpose of .gitignore?

The `.gitignore` file specifies files and folders that Git should ignore and not track.

Examples:
- node_modules/
- *.log
- .env

---

## 25. What is origin in Git?

`origin` is the default name of the remote repository.

Check it using:

```bash
git remote -v
```

---

## 26. How do you push code to GitHub?

```bash
git push origin main
```

---

## 27. How do you pull the latest changes?

```bash
git pull origin main
```

---

## 28. What is HEAD in Git?

HEAD is a pointer that refers to the current commit or active branch.

---

## 29. What is the difference between Git Reset and Git Revert?

| Git Reset | Git Revert |
|-----------|------------|
| Removes commits from history | Creates a new commit that reverses changes |
| Rewrites history | Preserves history |

---

## 30. Why is Git important in DevOps?

- Version control
- Team collaboration
- Supports CI/CD pipelines
- Tracks code history
- Easy rollback
- Branch management
- Integrates with Jenkins, GitHub Actions, GitLab CI, Azure DevOps
