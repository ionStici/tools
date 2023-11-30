[&larr; Back](./README.md)

# Git Rebase

## Rebase as an alternative to Merging

Rebasing can be thought as moving the base of a branch onto a different position.

If we have a feature branch with a bunch of commits, instead of merging it to main, in which other commits have meanwhile made, we can **rebase** the feature branch onto the master branch, and keep the git commit history clean and easy to follow.

By **rebasing** the new feature branch onto main, we more all the changes made from feature branch to the front of main and incorporate the new commits by rewriting its history.

_Instead of using a merge commit, rebasing rewrites history by **creating new commits** for each of the original feature branch commits._

```
git switch feature
git rebase master
```

Why Rebase? It eliminates unnecessary merge commits requried by git merge. We end up with a linear project history.

**Consider:** You do not want to rewrite any git history that other people already have. It's a pain to reconcile the alternate histories. **Preferably, rebasing should be used locally.** Don't rebase after something has been pushed.

<br>

## Rebasing as a cleanup tool

Using `git rebase` we can rewrite, delete, rename, even reorder commits (before sharing them).

`git rebase -i HEAD~4`

Running git rebase with the `-i` option will enter the interactive mode, which allows us to edit commits, add files, drop commits, etc. We also specify how far back we want to rewrite commits.

Here we are not rebasing onto another branch, instead, we are rebasing a series of commits onto the HEAD they currently are based on.

In our text editor, we'll see a list of commits alongside a list of commands that we can choose from.

- `pick` - use the commit
- `reword` - use the commit, but edit the commit message
- `edit` - use the commit, but stop for amending
- `fixup` - use commit contents but meld it into previous commit and discard the commit message
- `drop` - remove commit

<br>
