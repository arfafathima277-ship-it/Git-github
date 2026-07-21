# ⚙️ Git Installation and Configuration

## What is Git?

Git is a distributed Version Control System (VCS) used to track changes in files, manage source code, and collaborate with other developers.

---

# Installing Git

## Ubuntu / Debian

```bash
sudo apt update
sudo apt install git
```

---

## Fedora

```bash
sudo dnf install git
```

---

## RHEL / CentOS

```bash
sudo yum install git
```

---

## Arch Linux

```bash
sudo pacman -S git
```

---

## Windows

1. Download Git from **https://git-scm.com/**
2. Run the installer.
3. Select the default options.
4. Finish the installation.

---

# Verify Git Installation

Check whether Git is installed successfully:

```bash
git --version
```

Example Output:

```text
git version 2.43.0
```

---

# Git Configuration

After installing Git, configure your identity. This information is attached to every commit you make.

## Configure Username

```bash
git config --global user.name "Your Name"
```

Example:

```bash
git config --global user.name "John Doe"
```

---

## Configure Email

```bash
git config --global user.email "john@example.com"
```

Example:

```bash
git config --global user.email "johndoe@gmail.com"
```

---

## View All Git Configuration

```bash
git config --list
```

---

## Check Configured Username

```bash
git config user.name
```

---

## Check Configured Email

```bash
git config user.email
```

---

## Global vs Local Configuration

### Global Configuration

Applies to all Git repositories for the current user.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

### Local Configuration

Applies only to the current repository.

```bash
git config --local user.name "Your Name"
git config --local user.email "you@example.com"
```

---

# Where Git Stores Configuration

| Configuration | Location |
|--------------|----------|
| Global | `~/.gitconfig` |
| Local | `.git/config` |
| System | `/etc/gitconfig` |

---

# Useful Git Configuration Commands

| Command | Description |
|---------|-------------|
| `git --version` | Check Git version |
| `git config --global user.name "Name"` | Set global username |
| `git config --global user.email "Email"` | Set global email |
| `git config --list` | Display all configurations |
| `git config user.name` | Show configured username |
| `git config user.email` | Show configured email |

---

# Interview Questions

### 1. What is Git?

Git is a distributed version control system used to track changes in source code and collaborate with other developers.

---

### 2. How do you install Git on Ubuntu?

```bash
sudo apt update
sudo apt install git
```

---

### 3. How do you verify Git installation?

```bash
git --version
```

---

### 4. How do you configure Git username?

```bash
git config --global user.name "Your Name"
```

---

### 5. How do you configure Git email?

```bash
git config --global user.email "you@example.com"
```

---

### 6. What is the difference between Global and Local configuration?

- **Global Configuration:** Applies to all repositories for the current user.
- **Local Configuration:** Applies only to the current repository.

---

# Summary

- Install Git using your distribution's package manager or the official installer.
- Verify the installation with `git --version`.
- Configure your username and email before making commits.
- Use **global configuration** for all repositories and **local configuration** for repository-specific settings.
- View current settings using `git config --list`.