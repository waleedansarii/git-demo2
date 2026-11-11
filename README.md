# Git Cheat Sheet

A beginner-friendly reference guide to commonly used Git commands for version control, repository management, branching, collaboration, and history management.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Initial Configuration](#initial-configuration)
- [Create or Clone a Repository](#create-or-clone-a-repository)
- [Stage and Commit Changes](#stage-and-commit-changes)
- [Branching and Merging](#branching-and-merging)
- [Inspect and Compare](#inspect-and-compare)
- [Remote Repositories](#remote-repositories)
- [Track File Changes](#track-file-changes)
- [Ignore Files](#ignore-files)
- [Stash Temporary Changes](#stash-temporary-changes)
- [Rewrite History](#rewrite-history)
- [Typical Git Workflow](#typical-git-workflow)

## 1. Introduction

Git is a free and open-source distributed version control system. It helps developers track changes, maintain project history, and collaborate with others.

Git runs locally on your computer, while GitHub provides a platform to host and share Git repositories.

## 2. Installation

Install Git according to your operating system:

- Windows: https://git-scm.com/download/win
- Linux: https://git-scm.com/download/linux
- macOS: https://git-scm.com/download/mac

Check Git installation:

    git --version

## 3. Initial Configuration

Configure your username and email:

    git config --global user.name "Your Name"
    git config --global user.email "you@example.com"

Enable automatic command-line coloring:

    git config --global color.ui auto

View configuration:

    git config --list

## 4. Create or Clone a Repository

Initialize a Git repository:

    git init

Clone an existing repository:

    git clone <repository-url>

Example:

    git clone https://github.com/username/project.git

## 5. Stage and Commit Changes

Check repository status:

    git status

Stage a specific file:

    git add <filename>

Stage all changes:

    git add .

Unstage a file:

    git reset <filename>

View unstaged changes:

    git diff

View staged changes:

    git diff --staged

Commit changes:

    git commit -m "Your commit message"

## 6. Branching and Merging

List branches:

    git branch

Create a new branch:

    git branch <branch-name>

Switch branches:

    git checkout <branch-name>

Merge a branch:

    git merge <branch-name>

View commit history:

    git log

## 7. Inspect and Compare

Display commit history:

    git log

Show commits available in branchA but not branchB:

    git log branchB..branchA

Show file-specific commit history:

    git log --follow <filename>

Compare branches:

    git diff branchB...branchA

Display a particular commit:

    git show <commit-SHA>

## 8. Remote Repositories

Add a remote repository:

    git remote add origin <repository-url>

Fetch updates:

    git fetch origin

Merge a remote branch:

    git merge origin/main

Push changes to GitHub:

    git push origin main

Pull updates from the remote repository:

    git pull

## 9. Track File Changes

Remove a file:

    git rm <filename>

Move or rename a file:

    git mv <old-path> <new-path>

View file movement history:

    git log --stat -M

## 10. Ignore Files

Create a `.gitignore` file to exclude files and directories from Git tracking.

Example:

    logs/
    *.notes
    pattern*/
    .env
    __pycache__/

Configure a global ignore file:

    git config --global core.excludesfile <file-path>

Note: `.gitignore` does not automatically stop tracking files that have already been committed.

## 11. Stash Temporary Changes

Save temporary changes:

    git stash

List saved stashes:

    git stash list

Apply and remove the latest stash:

    git stash pop

Delete the latest stash:

    git stash drop

## 12. Rewrite History

Rebase the current branch:

    git rebase <branch-name>

Reset the staging area and working directory:

    git reset --hard <commit-SHA>

Warning: `git reset --hard` permanently discards uncommitted changes in the working tree.

## 13. Typical Git Workflow

A basic workflow for uploading project changes to GitHub:

    # Check repository status
    git status

    # Stage all changes
    git add .

    # Commit changes
    git commit -m "Update project files"

    # Push changes to GitHub
    git push origin main

## 14. Useful Resources

- Git Official Website: https://git-scm.com/
- Git Documentation: https://git-scm.com/doc
- GitHub Documentation: https://docs.github.com/
- GitHub Education: https://education.github.com/

---

**Happy Learning!**
