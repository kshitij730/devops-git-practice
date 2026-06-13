# Git Commands Cheat Sheet

## Setup & Configuration

### Check Git Version

```bash
git --version
```

Displays installed Git version.

---

### Configure Username

```bash
git config --global user.name "Your Name"
```

Sets Git username.

---

### Configure Email

```bash
git config --global user.email "yourmail@gmail.com"
```

Sets Git email.

---

## Repository Management

### Initialize Repository

```bash
git init
```

Creates a new Git repository.

---

### Repository Root

```bash
git rev-parse --show-toplevel
```

Shows repository root path.

---

## Basic Workflow

### Check Status

```bash
git status
```

Shows repository state.

---

### Stage Changes

```bash
git add filename
```

Adds file to staging area.

Example:

```bash
git add git-commands.md
```

---

### Stage All Changes

```bash
git add .
```

Stages all modified files.

---

### Commit Changes

```bash
git commit -m "message"
```

Creates a snapshot of staged changes.

Example:

```bash
git commit -m "Add Git branching commands"
```

---

## Viewing Changes

### View History

```bash
git log
```

Shows detailed commit history.

---

### Compact History

```bash
git log --oneline
```

Shows one-line commit history.

---

### View Changes

```bash
git diff
```

Shows unstaged changes.

---

### View Staged Changes

```bash
git diff --staged
```

Shows staged changes.

---

### Show Commit Details

```bash
git show
```

Displays commit details.

---

## Branching

### View Branches

```bash
git branch
```

Lists local branches.

---

### Create Branch

```bash
git branch feature-1
```

Creates a new branch.

---

### Switch Branch

```bash
git checkout feature-1
```

Switches to a branch.

---

### Switch Branch (Modern)

```bash
git switch feature-1
```

Modern alternative to checkout.

---

### Create and Switch Branch

```bash
git checkout -b feature-2
```

Creates and switches to a new branch.

---

### Create and Switch Branch (Modern)

```bash
git switch -c feature-2
```

Modern alternative.

---

### Delete Branch

```bash
git branch -d feature-2
```

Deletes merged branch.

---

### Force Delete Branch

```bash
git branch -D feature-2
```

Deletes branch forcefully.

---

## Remote Repositories

### Add Remote Repository

```bash
git remote add origin https://github.com/username/repository.git
```

Connects local repository to GitHub.

---

### View Remotes

```bash
git remote -v
```

Displays configured remote repositories.

---

### Push Main Branch

```bash
git push -u origin main
```

Pushes local branch to GitHub.

---

### Push Feature Branch

```bash
git push -u origin feature-1
```

Pushes feature branch to GitHub.

---

### Fetch Changes

```bash
git fetch origin
```

Downloads remote changes without merging.

---

### Pull Changes

```bash
git pull origin main
```

Downloads and merges remote changes.

---

## Clone & Fork

### Clone Repository

```bash
git clone https://github.com/user/repo.git
```

Creates a local copy of a repository.

---

### Add Upstream Repository

```bash
git remote add upstream https://github.com/original-owner/repo.git
```

Adds original repository reference after forking.

---

### Fetch Upstream Changes

```bash
git fetch upstream
```

Downloads latest changes from original repository.

---

### Merge Upstream Changes

```bash
git merge upstream/main
```

Updates fork with latest changes from original repository.

```
## Advanced Git Operations (Day 24)

### Merge Branch

```bash
git merge feature-login
```

Merges a branch into the current branch.

---

### Squash Merge

```bash
git merge --squash feature-profile
```

Combines all commits from a branch into a single commit before merging.

---

### Abort Merge

```bash
git merge --abort
```

Cancels an ongoing merge operation.

---

## Rebase

### Rebase Current Branch

```bash
git rebase main
```

Moves current branch commits on top of another branch.

---

### Continue Rebase

```bash
git rebase --continue
```

Continues rebase after conflict resolution.

---

### Abort Rebase

```bash
git rebase --abort
```

Cancels the rebase operation.

---

## Visualizing Git History

### Graph View

```bash
git log --oneline --graph --all
```

Displays commit history along with branch structure.

Example:

```text
* a1b2c3 Feature Commit
|\
| * d4e5f6 Main Commit
|/
* f7g8h9 Initial Commit
```

---

## Git Stash

### Save Current Work

```bash
git stash
```

Temporarily saves uncommitted changes.

---

### Stash With Message

```bash
git stash push -m "work in progress"
```

Creates a named stash entry.

---

### View Stashes

```bash
git stash list
```

Lists all saved stashes.

---

### Apply Latest Stash

```bash
git stash apply
```

Restores latest stash but keeps it in stash history.

---

### Apply and Remove Stash

```bash
git stash pop
```

Restores latest stash and removes it from stash history.

---

### Apply Specific Stash

```bash
git stash apply stash@{1}
```

Applies a selected stash.

---

### Delete Specific Stash

```bash
git stash drop stash@{0}
```

Deletes a specific stash.

---

### Remove All Stashes

```bash
git stash clear
```

Deletes all saved stashes.

---

## Cherry Pick

### Apply Specific Commit

```bash
git cherry-pick <commit-hash>
```

Copies a specific commit from another branch.

Example:

```bash
git cherry-pick d4e5f6
```

---

### Continue Cherry Pick

```bash
git cherry-pick --continue
```

Continues cherry-pick after resolving conflicts.

---

### Abort Cherry Pick

```bash
git cherry-pick --abort
```

Cancels cherry-pick operation.

---

## Conflict Resolution

### Check Conflicted Files

```bash
git status
```

Shows files that require conflict resolution.

---

### Conflict Markers

```text
<<<<<<< HEAD
Current Branch Changes
=======
Incoming Branch Changes
>>>>>>> feature-branch
```

Git inserts these markers when the same lines are modified in different branches.

---

## Branch Information

### Show Current Branch

```bash
git branch --show-current
```

Displays active branch name.

---

### Show All References

```bash
git log --oneline --decorate --all
```

Displays commits across all branches with references.

---

## Cleanup Commands

### Delete Remote Branch

```bash
git push origin --delete feature-1
```

Deletes a branch from GitHub.

---

### Remove Stale Remote References

```bash
git fetch --prune
```

Removes references to deleted remote branches.

```
