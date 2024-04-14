# Git Rebase

## git merge

`git merge` combines changes from one branch into another branch.

- When we merge two branches, the existing branches are not changed. Instead, a new "merge commit" is created.
- The original history of both branches remains intact and visible.
- Commonly used in scenarios where you want to incorporate changes from one branch into another while keeping the history.

Suppose you have two branches, **feature** and **master**:

```
A - - B - - C  master
             \
              D - - E  feature
```

After `git merge feature`, the commit history will look like this:

```
A - - B - - C - - - - F  master
             \       /
              D - - E
```

Here, `F` is a new merge commit.

## git rebase

Rebasing is used to integrate (not combine) commits from a branch to another.

- Rebasing rewrites the commit history by applying the commits from one branch to the top of another branch.
- No new merge commits are created if there are no conflicts.
- Preferred in situations where you want a cleaner, linear history.

```
A - - B - - C  master
             \
              D - - E  feature
```

Suppose we want to rebase the commits from the **feature** branch to **master**, then while on the **master** branch run:

```
git rebase feature
```

This will lead to:

```
A - - B - - C - D' - E'  master
```

Internally, Git accomplishes this by creating new commits and applying them to the specified base, this means that `D'` and `E'` are actually entirely new commits.

## Rebasing as a cleanup tool

Using `git rebase` we can rewrite, delete, rename, even reorder commits (before sharing them).

`git rebase -i HEAD~4`

Running `git rebase` with the `-i` option will enter "interactive mode", which allows us to edit commits, add files, drop commits, etc. `HEAD~4` indicates how far back we want to go and edit.

Here we are not rebasing onto another branch, instead we are rebasing a series of commits onto the HEAD that they currently are based on.

In our text editor, we'll see a list of commits alongside a list of commands that we can choose from.

- `pick` - use the commit
- `reword` - use the commit, but edit the commit message
- `edit` - use the commit, but stop for amending
- `fixup` - use commit contents but meld it into previous commit and discard the commit message
- `drop` - remove commit
