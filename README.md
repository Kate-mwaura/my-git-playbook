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
<p align="right"><a href="#kathys-linux-command-reference-for-devops">⬆ Back to Top</a></p>
---
