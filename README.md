 # Git Command Reference for DevOps 

A personal Git command reference built through hands-on practice and real development workflows.

Every command in this repository has been explored, tested, and used in practical scenarios as I continue strengthening my skills in version control, collaboration, and code management.

This repository serves as both a learning log and a growing reference guide, reflecting my ongoing journey toward mastering Git in real-world engineering environments.

---
## 📚 Table of Contents

1. [Repository Setup](#1-repository-setup)
2. [Staging & Committing](#2-staging--committing)
3. [Viewing History](#3-viewing-history)
4. [Branching & Navigation](#4-branching--navigation)
5. [Comparing Changes](#5-comparing-changes)
6. [Remote Operations](#6-remote-operations)
7. [Merging & Rebasing](#7-merging--rebasing)
8. [Undoing Changes](#8-undoing-changes)
9. [Stashing](#9-stashing)
10. [Advanced Operations](#10-advanced-operations)
11. [Submodules](#11-submodules)
12. [Cleanup & Maintenance](#12-cleanup--maintenance)
---

## 1. Repository Setup

| Command | My Definition / Logic | Flag / Example | Flag Definition |
|---|---|---|---|
| `git init` | initialize git local repository in your current working directory. | `git init` | initialize an empty repository in the current directory. |
| `git clone` | get a duplicate copy of a remote repository in your local current working directory. | `git clone <repo_url>` | clone a remote repository to your local machine. |
|  |  | `git clone <repo_url> <folder_name>` | clone repository into a specific directory. |
| `git remote add` | connecting local repository to a remote repository. | `git remote add origin <url>` | link local repository to a remote repository. |
| `git remote set-url` | update the remote repository URL in the local repository. | `git remote set-url origin <url>` | change the existing remote repository URL. |
| `git config --global` | setting configurations for system-wide use. | `git config --global user.name "your_name"` | set global username for commits. |
|  |  | `git config --global user.email "your_email"` | set global email for commits. |
| `git config --local` | setting configurations for only the specific project you're working in. | `git config --local user.name "your_name"` | set username for current repository only. |
|  |  | `git config --local user.email "your_email"` | set email for current repository only. |
<p align="right"><a href="#git-command-reference-for-devops--developers">⬆ Back to Top</a></p>

---

## 2. Staging & Committing

| Command | My Definition / Logic | Flag / Example | Flag Definition |
|---|---|---|---|
| `git add` | adding a change to the staging area. | `git add .` | add all changes in the current directory to staging area. |
|  |  | `git add <file_name>` | add a specific file to staging area. |
| `git restore --staged` | unstaging a file from the staging area. | `git restore --staged <file_name>` | remove a file from staging area but keep changes in working directory. |
| `git commit` | saving a change from the staging area to saved changes. | `git commit -m "commit message"` | commit staged changes with a message. |
| `git commit --amend` | combine the current change with the last commit at HEAD. | `git commit --amend` | modify the most recent commit. |
|  |  | `git commit --amend -m "new message"` | update the last commit message. |

<p align="right"><a href="#git-command-reference-for-devops--developers">⬆ Back to Top</a></p>

---
## 3. Viewing History

| Command | My Definition / Logic | Flag / Example | Flag Definition |
|---|---|---|---|
| `git status` | show the current state of a branch, unstaged, uncommitted and unpushed changes. | `git status` | display the current working directory and staging area status. |
| `git log` | show the commit history of saved changes (commits). | `git log` | display full commit history. |
|  |  | `git log --oneline` | squeeze log output into one line per commit. |
|  |  | `git log -p` | show commit history and changes made to each commit. |
|  |  | `git log -p <commit1>..<commit2>` | show differences between two commits. |
|  |  | `git log -no` | show the the specified no of commits. |
|  |  | `git log --after="Y-M-D"` | show commits after a specific date. |
|  |  | `git log --before="Y-M-D"` | show commits before a specific date. |
|  |  | `git log --author="name"` | search commits made by a specific user. |
|  |  | `git log --grep="pattern"` | search commits with a specific message pattern. |
|  |  | `git log -- <file_name>` | show history of a specific file. |
|  |  | `git log <remote/branch>..<local_branch> --oneline` | show commits in local branch not in remote branch. |
| `git show` | show the changes applied in specific commits. | `git show <commit_hash>` | display details of a specific commit. |
|  |  | `git show <hash1> <hash2>` | show changes from multiple commits. |
| `git reflog` | show entire history including deleted or changed commits. | `git reflog` | track all HEAD changes and recover lost commits. |

<p align="right"><a href="#git-command-reference-for-devops--developers">⬆ Back to Top</a></p>

---
## 4. Branching & Navigation

| Command | My Definition / Logic | Flag / Example | Flag Definition |
|---|---|---|---|
| `git branch` | creating a duplicate copy of the main source code to a new working area to make changes and tests without affecting the main working area directly. | `git branch` | list all local branches. |
|  |  | `git branch -a` | show all branches from both local and remote repositories. |
|  |  | `git branch -vv` | show local branches and their tracking remote branches. |
|  |  | `git branch <branch_name>` | create a new branch. |
|  |  | `git branch -m <old_name> <new_name>` | rename a branch in local repo. |
|  |  | `git branch -d <branch_name>` | delete a branch from local repository. |
|  |  | `git branch <branch_name> <commit_hash>` | create a branch from a specific commit. |
|  |  | `git push origin --delete/-d <branch_name>` | deleting a remote branch from the local branch (cli). |
|  |  | ` git push origin :<old_name> <new_name>` | renaming a remote branch from the local branch (cli). N:B ensure you 1st rename the local branch |
| `git checkout` | move from current branch to a specific branch. | `git checkout <branch_name>` | switch to an existing branch. |
|  |  | `git checkout -b <branch_name>` | create a new branch and switch to it. |
| `git switch` | move from current branch to a specific branch (modern alternative to checkout). | `git switch <branch_name>` | switch to an existing branch. |
|  |  | `git switch -c <branch_name>` | create a new branch and switch to it. |
|  |  | `git switch -` | switch back to the previous branch. |

<p align="right"><a href="#git-command-reference-for-devops--developers">⬆ Back to Top</a></p>

---
## 5. Comparing Changes

| Command | My Definition / Logic | Flag / Example | Flag Definition |
|---|---|---|---|
| `git diff` | show the difference between files, commits, repositories, branches or code. | `git diff` | show unstaged changes in the working directory. |
|  |  | `git diff --staged` | show staged changes ready to be committed. |
|  |  | `git diff <commit1> <commit2>` | show differences between two commits. |
|  |  | `git diff <local_branch>..<remote/branch>` | show the difference between local and remote branches. |
|  |  | `git diff <remote/branch>` | show the difference between current branch and a remote branch. |
|  |  | `git diff <remote/branch> -- <file_path>` | show difference for a specific file between local and remote. |
|  |  | `git diff --stat` | show a summarized output of changes. |

<p align="right"><a href="#git-command-reference-for-devops--developers">⬆ Back to Top</a></p>

---