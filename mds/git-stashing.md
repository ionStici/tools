[&larr; Back](./README.md)

# Git Stash

Git won't let us switch branches if it detects potential uncommitted conflicts.

**Stashing** - stash uncommitted changes so that we can return to them later.

- `git stash` save changes that you are not yet ready to commit, then come back later.

  Running `git stash` will take all uncommitted changes (staged or unstaged) and tash them, reverting the changes in your working copy.

  In stash mode, we can switch branches, create new commits, etc.

- `git stash pop` remove the most recently stashed changes in your stash and re-apply them to your working copy.

- `git stash apply` apply whatever is stashed away, without removing it from the stash. Useful if you want to apply stashed changes to multiple branches.

- `git stash -u` use the `-u` option to tell git stash to include untracked files.

  Untracked files are not included in the stash without `-u` option.

- You can add multiples stashes onto the stack of stashes. They will all be stashed in the order you added them.

  `git stash list` to view all stashes.

  `git stash clear` clear out all stashes.

  `git stash apply stash@{2}` apply a particular stash instead of just the most recent stash.

  `git stash frop stash@{2}` delete a particular stash.

<br>

## Stashing

While working on a file, you find a small bug in a separate file from a previous commit that needs to be fixed before you continue.

- `git stash` will store your work temporarily for later use in a hidden directory.

  At this point, you can switch branches and do work elsewhere, then commit.

- `git stash pop` restore the previous code you were working on (once the bug is fixed).

<br>
