# My Personal Git Tutorial

A customized guide to everyday Git commands, tailored for my workflow and projects.

Inspired by various Git resources, but made unique with personal examples and notes.

Don't forget to ⭐ this repo if you find it helpful!

---

## Table of Contents

- [Getting Started](#getting-started)
- [Basic Workflow](#basic-workflow)
- [Branching](#branching)
- [Fixing Mistakes](#fixing-mistakes)
- [Collaboration](#collaboration)
- [Advanced Tips](#advanced-tips)
- [Emergency Fixes](#emergency-fixes)

---

## Getting Started

### Cloning a Repository

To start working on a project:

```bash
git clone <repository-url>
cd <project-directory>
```

### Switching Branches

Change to a different branch:

```bash
git switch <branch-name>
```

### Pulling Latest Changes

Get updates from the remote:

```bash
git pull
```

---

## Basic Workflow

### Checking Changes

See what you've modified:

```bash
git status
```

### Staging and Committing

Save your work:

```bash
git add .
git commit -m "Your descriptive message here"
```

### Pushing to Remote

Share your changes:

```bash
git push
```

### Selective Staging

Only stage specific files:

```bash
git add file1.txt file2.js
git commit -m "Updated specific files"
```

### Unstaging Files

Remove from staging area:

```bash
git restore --staged <filename>
```

---

## Branching

### Creating a New Branch

Start a new feature branch:

```bash
git switch -c <new-branch-name>
```

### Deleting Branches

Remove a local branch:

```bash
git branch -d <branch-name>
```

Force delete if needed:

```bash
git branch -D <branch-name>
```

Delete remote branch:

```bash
git push origin --delete <branch-name>
```

### Renaming Branches

Rename your current branch:

```bash
git branch -m <new-name>
git push origin -u <new-name>
git push origin --delete <old-name>
```

---

## Fixing Mistakes

### Reverting File Changes

Undo modifications:

```bash
git restore .
```

Or for a specific file:

```bash
git restore <filename>
```

### Amending Commits

Add forgotten files or change message:

```bash
git add <forgotten-files>
git commit --amend --no-edit
```

Change commit message:

```bash
git commit --amend -m "New message"
```

### Undoing Commits

Keep changes:

```bash
git reset --soft HEAD~1
```

Discard changes:

```bash
git reset --hard HEAD~1
```

### Fixing Pushed Commits

Amend and force push (use carefully):

```bash
git commit --amend
git push --force
```

**Note:** Avoid on shared branches!

---

## Collaboration

### Pulling Changes

Get team updates:

```bash
git pull
```

### Handling Conflicts

If pull fails due to changes:

Stash your work:

```bash
git stash
```

Pull and restore:

```bash
git pull
git stash pop
```

Resolve conflicts by editing files, then:

```bash
git add <resolved-files>
git merge --continue
```

Or abort:

```bash
git merge --abort
```

### Merging Main Branch

Update your branch:

```bash
git switch main
git pull
git switch <your-branch>
git merge main
```

Resolve conflicts if any, then push.

---

## Advanced Tips

### Squashing Commits

Combine multiple commits:

```bash
git reset --soft HEAD~<number>
git commit -m "Squashed commits"
git push --force
```

### Cherry-Picking

Copy a commit from another branch:

```bash
git log  # Find commit hash
git cherry-pick <commit-hash>
```

### Rebasing

Update without merge commit:

```bash
git pull --rebase
```

If conflicts, fix and:

```bash
git add <files>
git rebase --continue
```

Or abort:

```bash
git rebase --abort
```

---

## Emergency Fixes

### Reverting Pushed Changes

Undo a commit safely:

```bash
git revert <commit-hash>
git push
```

### Resetting to Another Branch

Make branch identical (destructive):

```bash
git reset --hard origin/<other-branch>
```

### Recovering Deleted Commits

Use reflog:

```bash
git reflog
git cherry-pick <commit-hash>
```

### Removing Recent Commits

Permanently delete:

```bash
git reset --hard HEAD~<number>
git push --force
```

---

## Examples in This Repo

To practice the commands above, try modifying the `hello.txt` file in this repository:

1. Edit `hello.txt` and add your name.
2. Run `git status` to see changes.
3. Stage with `git add hello.txt`.
4. Commit with `git commit -m "Added my name to hello.txt"`.
5. Push with `git push`.

Create a new branch for experiments:

```bash
git switch -c experiment
# Make changes, commit, then merge back
git switch master
git merge experiment
```

---

## Common Issues

- **Branch diverged:** `git pull --rebase`
- **Merge conflict:** Edit files, `git add`, `git merge --continue`
- **Permission denied:** Check credentials and access

---

This is my personalized Git guide. Feel free to fork and adapt for your needs!