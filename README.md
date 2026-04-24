# Git Tutorial with GitKraken

A customized guide to everyday Git commands and GitKraken.

---

## Table of Contents

- [Setting Up Git and GitKraken](#setting-up-git-and-gitkraken)
- [Creating and Initializing a Git Repository](#creating-and-initializing-a-git-repository)
- [Staging and Committing Changes](#staging-and-committing-changes)
- [Using GitKraken to Enhance Your Workflow](#using-gitkraken-to-enhance-your-workflow)
- [Working with Branches](#working-with-branches)
- [Pushing and Pulling Code to GitHub](#pushing-and-pulling-code-to-github)
- [Merging and Resolving Merge Conflicts](#merging-and-resolving-merge-conflicts)
- [Using AI Features in GitKraken](#using-ai-features-in-gitkraken)
- [Additional GitKraken Features](#additional-gitkraken-features)
- [Advanced Git Operations](#advanced-git-operations)
- [Emergency Fixes](#emergency-fixes)
- [Quick Reference](#quick-reference)
- [Troubleshooting](#troubleshooting)
- [Examples in This Repo](#examples-in-this-repo)

---

## Prerequisites

Before we begin, ensure you have the following installed on your system:

- Git: Download from [Git Official Site](https://git-scm.com/downloads)
- GitKraken: Free to use; download it from [GitKraken Official Site](https://www.gitkraken.com/)

---

## 1. Setting Up Git and GitKraken

To begin using Git in your development environment, first download and install Git. Follow these steps:

Go to the [Git Downloads page](https://git-scm.com/downloads) and select the appropriate version for your system (Windows, Mac, or Linux).

After installation, verify Git is installed by opening a terminal and typing:

```bash
git --version
```

Next, install GitKraken, a graphical interface for Git that makes managing repositories much easier. Download from [GitKraken Official](https://www.gitkraken.com/).

---

## 2. Creating and Initializing a Git Repository

Create a new project folder or open your existing project in VS Code.

Open your terminal and navigate to your project folder. Type:

```bash
git init
```

This will initialize an empty Git repository in your project folder.


---

## 3. Staging and Committing Changes

After initializing your repository, add files to Git:

Create or edit a file (e.g., index.html) in your project.

Stage the file to Git by typing:

```bash
git add index.html
```

Or stage all files:

```bash
git add .
```

Commit your changes:

```bash
git commit -m "Add index.html file"
```

![Committing Changes](images/Committing%20Changes.png)

---

## 4. Using GitKraken to Enhance Your Workflow

GitKraken helps visualize commits, branches, and changes. Here's how to get started:

- Download and install GitKraken.
- Log in with your GitHub account.
- Open your repository in GitKraken to see all your commits visually.

![GitKraken Interface](images/GitKraken%20Interface.png)

---

## 5. Working with Branches

### Create a New Branch

In Git, branches allow you to work on different features without affecting the main codebase.

To create a new branch, use:

```bash
git switch -c <branch-name>
```

Or in GitKraken, click Create Branch and enter the branch name.

### Switching Branches

Switch branches to work on different features:

```bash
git switch <branch-name>
```

![Creating a New Branch in GitKraken](images/Creating%20a%20New%20Branch%20in%20GitKraken.png)

---

## 6. Pushing and Pulling Code to GitHub

### Push Changes

To push your changes to a remote repository, first create a GitHub repository. Then, add the remote repository URL:

```bash
git remote add origin <repository-url>
git push -u origin master
```

### Pull Changes

To pull changes from GitHub:

```bash
git pull origin master
```

![Pushing Code to GitHub](images/Pushing%20Code%20to%20GitHub.png)

---

## 7. Merging and Resolving Merge Conflicts

When working with multiple branches, you may need to merge them. Here's how to do it:

Checkout the branch you want to merge into (usually master):

```bash
git switch master
```

Merge the feature branch into master:

```bash
git merge <feature-branch>
```

### Resolving Merge Conflicts

If there are conflicts, GitKraken helps you resolve them visually. You can accept incoming changes, keep the current changes, or merge both manually.

![Merging and Resolving Merge Conflicts](images/Merging%20and%20Resolving%20Merge%20Conflicts.png)

---

## 8. Using AI Features in GitKraken

GitKraken offers AI-assisted commit message generation and commit reorganization, making it easier to maintain clean and efficient commit histories. For example, you can use AI to generate meaningful commit messages or recompose multiple commits into one.

![AI-Assisted Commit Messages](images/AI-Assisted%20Commit%20Messages.png)

---

## Additional GitKraken Features

GitKraken is packed with powerful features to enhance your Git workflow beyond the basics. Here are some key ones:

### Interactive Rebase
Easily reorder, edit, or squash commits with a visual drag-and-drop interface. This helps clean up your commit history before merging.

### Fuzzy Finder
Quickly search and navigate through your repository files, commits, and branches using fuzzy matching.

### Git LFS Support
Handle large files efficiently with Git Large File Storage integration, keeping your repository lightweight.

### Pull Request Management
Create, review, and merge pull requests directly within GitKraken, integrated with GitHub, GitLab, and Bitbucket.

### Issue Tracking
Link commits to issues and track progress on projects with built-in issue management.

### Timelines
View a chronological timeline of your repository's activity, including commits, merges, and branch creations.

### Multiple Profiles
Switch between different Git identities and configurations for personal and work projects.

### Integrations and Extensions
Connect with various tools like Jira, Trello, Slack, and more for seamless project management.

### Dark Mode and Themes
Customize the interface with dark mode or various themes for comfortable coding sessions.

### Git Hooks
Manage and visualize Git hooks to automate tasks like pre-commit checks or post-merge actions.

These features make GitKraken a comprehensive tool for both beginners and advanced users, streamlining complex Git operations.

---

## Advanced Git Operations

### Squashing Commits
If you have too many commits, combine them into one for a cleaner history:

```bash
git reset --soft HEAD~<number-of-commits>
git commit -m "combined message"
git push --force
```

### Cherry-Picking Commits
Copy a specific commit from another branch:

```bash
git log  # Find the commit hash
git cherry-pick <commit-hash>
```

### Rebasing Branches
Update your branch without a merge commit:

```bash
git pull --rebase
```

If conflicts arise:
1. Fix the conflicts
2. Stage the files: `git add <files>`
3. Continue: `git rebase --continue`
4. Push: `git push --force`

To abort: `git rebase --abort`

---

## Emergency Fixes

### Reverting Pushed Commits
Undo a commit safely by creating a new commit that reverses it:

```bash
git revert <commit-hash>
git push
```

### Hard Reset to Match Another Branch
Make your branch identical to another (destructive):

```bash
git reset --hard origin/<other-branch-name>
```

**Warning:** This deletes all uncommitted changes!

### Removing Recent Commits Permanently
Delete the last few commits:

```bash
git reset --hard HEAD~<number-of-commits>
git push --force
```

**Warning:** This cannot be undone!

### Recovering Lost Commits
Use the reflog to find and restore deleted commits:

```bash
git reflog
git cherry-pick <commit-hash>
```

---

## Quick Reference

```bash
# Check status
git status

# Stage and commit all changes
git add .
git commit -m "message"
git push

# Pull latest changes
git pull

# Create and switch to a new branch
git switch -c <branch-name>

# Switch branches
git switch <branch-name>

# Undo all changes
git restore .

# Stash work temporarily
git stash
git stash pop
```

---

## Troubleshooting

### Branch Diverged
When your branch has diverged from the remote:

```bash
git pull --rebase
```

### Merge Conflicts
Resolve manually:
- Edit the conflicting files
- Remove conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
- Stage: `git add <file>`
- Continue: `git merge --continue`

### Permission Denied
- Verify your credentials
- Ensure you have access to the repository

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

This is my personalized Git guide with GitKraken integration. Feel free to fork and adapt for your needs!

