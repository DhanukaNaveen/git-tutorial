# My Personal Git Tutorial with GitKraken

A customized guide to everyday Git commands and GitKraken, tailored for my workflow and projects.

Inspired by various Git resources, but made unique with personal examples and notes.

Don't forget to ⭐ this repo if you find it helpful!

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

*(Screenshot: Initializing Git Repository - Replace with actual screenshot showing terminal with the git init command.)*

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

*(Screenshot: Committing Changes - Replace with actual screenshot showing VS Code or GitKraken commit window.)*

---

## 4. Using GitKraken to Enhance Your Workflow

GitKraken helps visualize commits, branches, and changes. Here's how to get started:

- Download and install GitKraken.
- Log in with your GitHub account.
- Open your repository in GitKraken to see all your commits visually.

*(Screenshot: GitKraken Interface - Replace with actual screenshot showing GitKraken interface with a repository.)*

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

*(Screenshot: Creating a New Branch in GitKraken - Replace with actual screenshot showing GitKraken branch creation interface.)*

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

*(Screenshot: Pushing Code to GitHub - Replace with actual screenshot showing GitKraken push action.)*

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

---

## 8. Using AI Features in GitKraken

GitKraken offers AI-assisted commit message generation and commit reorganization, making it easier to maintain clean and efficient commit histories. For example, you can use AI to generate meaningful commit messages or recompose multiple commits into one.

*(Screenshot: AI-Assisted Commit Messages - Replace with actual screenshot showing AI commit feature in GitKraken.)*

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