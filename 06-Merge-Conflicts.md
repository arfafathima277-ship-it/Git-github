# Merge Conflicts

## What is a Merge Conflict?

A merge conflict occurs when Git is unable to automatically merge changes from two different branches because the same part of a file has been modified differently.

In simple words, Git gets confused about which change to keep and asks the developer to resolve the conflict manually.

---

# Why Do Merge Conflicts Occur?

Merge conflicts usually occur when:

- Two developers modify the same line of code.
- One developer deletes a file while another modifies it.
- The same file is edited differently in different branches.

---

# Example

Suppose there are two branches:

### Main Branch

```java
System.out.println("Welcome");
```

### Feature Branch

```java
System.out.println("Welcome to DevOps");
```

When you merge the feature branch into the main branch, Git cannot decide which version to keep because both branches modified the same line.

This results in a merge conflict.

---

# Conflict Markers

Git displays conflict markers inside the file.

```text
<<<<<<< HEAD
System.out.println("Welcome");
=======
System.out.println("Welcome to DevOps");
>>>>>>> feature-branch
```

### Meaning

- `<<<<<<< HEAD` → Changes from the current branch.
- `=======` → Separator between both versions.
- `>>>>>>> feature-branch` → Changes from the branch being merged.

The developer must choose the correct code and remove the conflict markers.

---

# How to Resolve a Merge Conflict

### Step 1: Merge the branch

```bash
git merge feature-branch
```

Git reports a merge conflict.

---

### Step 2: Open the conflicted file.

Git displays conflict markers.

---

### Step 3: Edit the file.

Keep the correct code and remove the conflict markers.

Example:

```java
System.out.println("Welcome to DevOps");
```

---

### Step 4: Stage the resolved file.

```bash
git add .
```

---

### Step 5: Commit the merge.

```bash
git commit -m "Resolved merge conflict"
```

The conflict is now resolved.

---

# Merge Conflict Workflow

```
Main Branch
      │
      ▼
Feature Branch
      │
      ▼
Both modify same file
      │
      ▼
git merge
      │
      ▼
Merge Conflict
      │
      ▼
Resolve Manually
      │
      ▼
git add .
      │
      ▼
git commit
```

---

# Best Practices

- Pull the latest changes before starting work.
- Commit your work regularly.
- Create small feature branches.
- Communicate with team members before modifying the same files.
- Resolve conflicts carefully before committing.

---

# Advantages of Resolving Conflicts Properly

- Prevents code loss.
- Maintains project consistency.
- Improves team collaboration.
- Ensures a stable codebase.

---

# Interview Questions

## What is a Merge Conflict?

A merge conflict occurs when Git cannot automatically merge changes because the same file or line has been modified differently in different branches.

---

## Why do Merge Conflicts occur?

Merge conflicts occur when multiple branches modify the same part of a file or when one branch deletes a file that another branch modifies.

---

## How do you resolve a Merge Conflict?

1. Merge the branch.
2. Open the conflicted file.
3. Remove the conflict markers.
4. Keep the correct code.
5. Stage the file using `git add`.
6. Commit the resolved changes.

---

## Which command is used to merge branches?

```bash
git merge <branch-name>
```

---

## Which command stages the resolved file?

```bash
git add .
```

---

## Which command completes the merge after resolving the conflict?

```bash
git commit -m "Resolved merge conflict"
```

---

# Summary

- Merge conflicts occur when Git cannot automatically combine changes.
- Developers resolve conflicts manually.
- Conflict markers identify the conflicting code.
- After resolving the conflict:
  - Stage the file using `git add`.
  - Commit the merge using `git commit`.
- Merge conflicts are common in collaborative development.
