# Git Commands Reference Guide

This document contains commonly used Git commands and their purpose. It will be updated regularly as I learn more Git concepts.

---

# Setup & Configuration

## Check Git Version

### Command

```bash
git --version
```

### Purpose

Displays the installed Git version.

### Example

```bash
git --version
```

---

## Configure Username

### Command

```bash
git config --global user.name "Kshitij Sharma"
```

### Purpose

Sets the username used for commits.

---

## Configure Email

### Command

```bash
git config --global user.email "yourmail@gmail.com"
```

### Purpose

Sets the email associated with commits.

---

## View Configuration

### Command

```bash
git config --list
```

### Purpose

Displays all Git configuration settings.

---

# Basic Workflow

## Initialize Repository

### Command

```bash
git init
```

### Purpose

Creates a new Git repository.

### Example

```bash
mkdir devops-git-practice

cd devops-git-practice

git init
```

---

## Check Repository Status

### Command

```bash
git status
```

### Purpose

Shows the current state of the repository.

### Example

```bash
git status
```

---

## Add File to Staging Area

### Command

```bash
git add filename
```

### Purpose

Moves changes from working directory to staging area.

### Example

```bash
git add git-commands.md
```

---

## Add All Files

### Command

```bash
git add .
```

### Purpose

Stages all modified files.

---

## Commit Changes

### Command

```bash
git commit -m "message"
```

### Purpose

Creates a snapshot of staged changes.

### Example

```bash
git commit -m "Add Git command documentation"
```

---

# Viewing Changes

## View Commit History

### Command

```bash
git log
```

### Purpose

Displays complete commit history.

---

## Compact Commit History

### Command

```bash
git log --oneline
```

### Purpose

Shows commits in a short format.

### Example

```bash
git log --oneline
```

Output:

```text
f3a4b2c Add branch commands
c8d4e2a Add git diff notes
9f7e2d1 Initial commit
```

---

## Show File Differences

### Command

```bash
git diff
```

### Purpose

Displays changes not yet staged.

---

## Show Staged Changes

### Command

```bash
git diff --staged
```

### Purpose

Displays staged changes before commit.

---

# Repository Information

## Current Repository Root

### Command

```bash
git rev-parse --show-toplevel
```

### Purpose

Shows repository root directory.

---

## View Branches

### Command

```bash
git branch
```

### Purpose

Displays local branches.

---

## View Detailed Commit Information

### Command

```bash
git show
```

### Purpose

Displays details of the latest commit.

---

# Important Git Areas

| Area              | Description                  |
| ----------------- | ---------------------------- |
| Working Directory | Files currently being edited |
| Staging Area      | Temporary area before commit |
| Repository        | Permanent Git history        |
| .git Directory    | Stores all Git metadata      |

---

# Commands Learned So Far

```bash
git --version
git config --global user.name
git config --global user.email
git config --list
git init
git status
git add
git commit
git log
git log --oneline
git diff
git diff --staged
git show
git branch
```

