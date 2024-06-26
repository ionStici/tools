# Git Branching

Create **branches** to experiment with versions of a project. We can work with a branch only, and not affecting the **master** default branch until we decide to merge our changes. Initially, the git repo has only the **master** branch.

- `git branch` will show in which branch we are

  `* master` the asterisk is showing the current branch.

- `git branch branch_name` create and name a new branch.

  Initially, both branches **master** and **branch_name** are identical, they share the same commit history.

- `git checkout branch_name` (old) switch between branches. Future commits belong to the active branch.

- `git switch -c branch_name` (new) switch between branches. The `-c` flag creates a branch at once.

- `git merge branch_name` merge a branch into the **master** branch.

  But first switch `git switch master` because we always merge to the current HEAD branch.

- `git branch -d branch_name` delete a branch that has merged. Use `-D` if the branch never merged into _master_.

- `git branch -r` to view remote branches our repo knows about.

## Overview

- `git branch` list all branches
- `git branch branch_name` create a new branch
- `git switch branch_name` switch from one branch to another
- `git merge branch_name` merge changes from a branch to master
- `git branch -d branch_name` delete a branch

## Branch Strategy

Isolate your work into different types of branches.

- **Primary branches :** `main` and `develop`
- **Supporting branches :** `feature`, `release`, `hotfix`

<div></div>

- `main` : The main branch where the source code reflects production-ready state
- `develop` : Integration branch for features, corrections, and other enhancements
- `feature` : Branches created from `develop` for new features
- `release` : Branches created from `develop`, for preparing a new production release
- `hotfix` : Branches from `main` for quick corrections to production issues

### Six Principles of an effective branching strategy

1. Any code in the `main` branch should be deployable

   The other branches should contain in-progress work that will be merged into `main` when the work is finished and properly reviewed

2. To work on something new, create a descriptively named branch off of `main`

   Create branches for each new feature, bug fix, or release. Use clear naming conventions, for example:

   `feature/feature-name`, `bugfix/bug-description`, `release/version-number`

3. Commit to that branch and regularly push your work to the same named branch on the remote

4. When you need feedback or help, or you think the branch is ready for merging, open a pull request

5. Merge only after the pull request has been reviewed and approved

6. Once it is merged into `main`, you can and should deploy immediately

## Merge Conflict

**A Git Fast-Forward** is when the branch we want to merge is ahead of the main branch.

If a commit has been made to the master branch in the meantime, instead of a simple fast-forward git performs a **merge commit**. We end up with a new commit on the master branch, so git will prompt you for a message.

The merge is successful if **master** had no changes since we made a commit on **branch_name**. If **master** had a commit before we merged the branches, git doesn't know which changes to keep if they overlap. This is called a **merge conflict**.

You've made commits on separate branches that alter the same line on conflicting ways. Now, when you try to merge **branch_name** into **master**, git will ask which changes of the file to keep. Output:

```
CONFLICT (content): Merge conflict in text.txt
Automatic merge failed; fix conflicts and then commit the result.
```

We must fix the merge conflict. Open the conflicting file. Git uses markers to indicate the conflicting branches.

```
<<<<<<< HEAD
master version of line
=======
branch_name version of line
>>>>>>> branch_name
```

Here, git asks us which version of the file to keep. Decide which branch's content you want to keep in each conflict. Or keep the content from both. Edit the file and remove the conflict markers. Lastly, add your changes and then make a commit.
