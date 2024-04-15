# Git Pull

## Pulling

`git pull` does what `git fetch` does, and then it merges the changes into your local branch.

Essentially, `git pull` is a combination of `git fetch` followed by `git merge`. This means that when you execute `git pull`, git will first fetch the latest changes from the remote repository (updating the remote-tracking branches) and then immediately merge the changes into the current branch you are on.

- `git pull` pull changes from the default tracked repository and branch
- `git pull origin main` pull changes from a specific remote and branch

## Options and Variants

- `git pull --rebase` rebase the local commits on top of the remote branch instead of merging.

- `git pull --tags` pull tags from the remote.

## Resolving Conflicts

1. If a `git pull` results in conflicts, you must manually resolve these conflicts.

2. Git will mark the files and you will need to edit these files to resolve the conflicts.

3. After resolving, you add the resolved files with `git add`, and then you can continue with a `git commit` to finalize the merge.

## Differences Between git fetch and git pull

### 1. Change to Working Directory

- `git fetch` does not change your working directory. Your current working code remains the same, and you can decide to merge later manually.
- `git pull` changes your working directory by automatically merging changes from the remote.

### 2. Control Over Merging

- With `git fetch`, you can review the changes fetched from the remote repository before deciding to merge them into your branch.
- `git pull` provides less control since it fetches and merges in a single command.

### 3. Use Case

- Use `git fetch` when you want to see the updates on the remote repository but might want to merge those changes at a later time or not at all.
- Use `git pull` when you are ready to incorporate the changes from the remote repository into your local working files immediately.
