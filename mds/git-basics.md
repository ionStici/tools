[&larr; Back](./README.md)

# Git

## Resources

- [Git Documentation](https://git-scm.com/docs)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)

<br>
 
## Git Init

Run the following command in a particular project directory to initialize a new git repository:

```
git init
```

**Git Repository (Repo)** is a project directory that uses git to track changes.

_p.s._ Do not initiate a git repo inside of a repo, because git tracks a directory and all nested subdirectories. Use `git status` to verify if you are not currently inside of a repo.

<br>

## Git Workflow

A Git project can be thought of as having 3 parts:

1. **Working Directory:** where we are currently working on the project, before git tracking.
2. **Staging Area:** where you'll list changes you make to the working directory.
3. **Repository:** where git permanently stores those changes as different versions of the project.

<br>

## Git Basic Commands

- **`git status`** check the status of current changes

  This command will show us files that contain changes but are not yet tracked, as well as files added to the staging area.

- **`git add file.txt`** after making changes to the project, we add them to the staging area.

  Use the dot `.` instead of specific files to stage all changes at once.

- **`git commit -m "Style Hero"`** A commit saves the changes from the staging area to the repo as a new version.

  Every commit is identified with a message that we write in quotation marks after the `-m` flag.

  _Messages:_ Atomic Commits, Write in the present tense, Meaningful and Concise messages.

- **`git log`** view the commit history of a branch.

  `git log --oneline` lists the commit history in one line format.

  `git log -S "keyword"` displays the commits that contain the keyword in the message.

  <!-- `git log --oneline --graph` displays a visual representation of how the branches and commits were created in order to help you make sense of your repository history -->

<br>

## Git Amend

```
git add script.js
git commit --amend --no-edit
```

If you forgot to do a small change that belongs to the previous commit, use `--amend` option.

With this command, git replaces the whole previous commit with the current one. So, it asks you to update your commit message. To keep the same commit message, you can add the `--no-edit` flag.

<br>

## Overview

- `git init` creates a new Git repository
- `git status` inspects the contents of the working directory and staging area
- `git add` adds files from the working directory to the staging area
- `git diff` shows the difference between the working directory and the staging area in a file
- `git commit` permanently stores file changes from the staging area in the repository
- `git log` shows a list of all previous commits

<br>

## git diff

`git diff` command to view changes between commits, branches, files, our working directory, and more.

- **`git diff`** list all the changes in the working directory that are not staged for the next commit.

- **`git diff HEAD`** list all changes in the working tree since the last commit.

- **`git diff --staged`** list the changes between the staging area and our last commit.

- **`git diff HEAD file.txt`** list changes within a specific file. The `--staged` flag works as well.

- **`git diff branch1..branch2`** list changes between branches.

- **`git diff commit1..commit2`** compare 2 commits, provide the commit hashes of the commits.

<br>
