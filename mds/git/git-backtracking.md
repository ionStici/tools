# Git Backtracking

## HEAD and Checkout

**HEAD** is a reference to the latest commit in the current branch. When you make new commits, HEAD moves forward with each commit.

When you switch branches, **HEAD** moves to point to the tip of the new branch.

- `git checkout [commit-hash]` moves **HEAD** to the specified commit. This results in a "detached" HEAD state, meaning changes you make will not belong to any branch until you decide to create one.

  By pointing **HEAD** to a specific commit, we can examine previous versions of the project or even commence new changes from that particular commit.

- `git switch master` reattaches **HEAD** to the **master** branch.

### Checkout workflow

If you want to go back to an old commit and make some changes:

1. `git checkout [commit-hash]` will make HEAD point to a particular previous commit (detached HEAD state).

2. `git branch -c new-branch` creates a new branch from the detached HEAD state and switches to it, this will result in HEAD pointing back to a branch.

3. Commit the required changes to `new-branch` and switch to **master** branch.

4. `git merge new-branch --no-edit` merge your work into the master branch (without prompting for a merge commit message).

In summary, we reverted to an old commit, created a new branch at that point, made changes, and merged those changes back into the **master** branch.

### Discard Changes

Restore a file in your working directory to look exactly as it did right after the last commit.

- `git checkout HEAD file.txt` this will discard the changes made to file.txt until after the last commit.

## git restore

`git restore` is a tool for reverting changes in the working directory and the staging area.

- `git restore file.txt` will revert `file.txt` to its state at the last commit.

- `git restore --source=4e2a39b file.txt` will restore `file.txt` to its state at the specified commit `4e2a39b`. It’s a way to view or test an old version of a file without altering the current branch.

- `git restore --staged file.txt` will unstage `file.txt`

## git reset

`git reset` is used to undo changes by altering the commit history up to a specified point.

- `git reset --mixed 5d69206` will move the current branch pointer (HEAD) back to the commit `5d69206`. Commits after this point are not deleted, but become "orphaned" and can be lost if not referenced by another branch or tag.

  **Staging Area:** is reset to the state of the specified commit.

  **Working Directory:** is not touched.

  **Use Case:** When you want to undo a `git add` and leave the working directory unchanged.

- `git reset --soft 5d69206` will move the branch pointer back as above, but it keeps the changes from the "orphaned" commits in the staging area, ready to be re-committed if necessary.

  **Staging Area:** is not modified.

  **Working Directory:** is not touched.

  **Use Case:** When you want to undo a commit or several commits but want to keep the changes for a re-commit (essentially rewriting the commit history).

- `git reset --hard 5d69206` will move the branch pointer back and discard any changes in the working directory and staging area, aligning the project's working state with that of the `5d69206` commit.

  All changes in the working directory will be discarded sinse the specified commit. The state of your files will match exactly what was in the `hash` commit.

  **Staging Area:** is reset just like with a `--mixed` reset.

  **Working Directory:** All changes in the working directory will be discarded sinse the specified commit. The state of your files will match exactly what was in the `hash` commit.

  **Use Case:** When you need to discard all your current changes and fully revert to the state of a specific commit

### Unstage with reset

- `git reset HEAD file.txt` will unstage `file.txt` without altering the current commit history.

## git revert

`git revert` creates a new commit that undoes the changes introduced in a previous commit without altering the project's history.

- `git revert 5d69206` will create a new commit that is the inverse of the `5d69206` commit. This doesn't remove the original commit but instead applies changes that cancel out the effects of that commit.
