# Git Fetch

## Fetching

`git fetch` downloads the latest changes from a remote repository to your local machine, but does not merge them into your current working branch, instead it updates your _remote-tracking branches_.

**Remote-tracking branches** are references to the state of branches on your remote repositories. For instance, if you fetch from a remote named `origin`, and the remote has a branch named `main`, git stores this as `origin/main` in your local repository. These branches are read-only, you can't directly check out and commit to these changes. Instead, you use them to track progress against the remote.

- `git fetch origin` fetches all branches from the remote repository

- `git fetch origin main` fetches a specific branch from the remote

## Operations with Remote-tracking Branches

### 1. Checking out a Remote Branch Locally

If you want to work on a branch that exists on the remote but not locally, you can check it out, which will set up a new local branch to track the remote branch.

```
git checkout -b feature-branch origin/feature-branch
```

This command creates a local branch named `feature-branch` that tracks the remote `origin/feature-branch`.

### 2. Merging Changes

If you fetched changes in a branch and want to merge them into your local branch (e.g. merging updates from `origin/main` into your local `main` branch), you would:

```
git checkout main
git merge origin/main
```

This brings your local `main` branch up-to-date with the fetched remote changes.

### 3. Rebasing

Alternatively, you can rebase your local branch on top of the fetched remote branch (common in workflows that prefer a linear history).

```
git checkout feature-branch
git rebase origin/main
```

Git takes the commits that were made on your local `feature-branch` and re-applies them one by one on top of the latest commit from `origin/main`.

### 4. Inspecting Changes

You can compare your local branch with the fetched remote branch.

```
git diff main origin/main
```

This shows the differences between the local `main` branch and the fetched `origin/main`.
