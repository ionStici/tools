# Git Stash

**Git Stashing** - temporarily shelve changes from the working directory so that you can work on something else, and then come back and re-apply them later on.

- `git stash` takes all uncommitted changes (staged or unstaged) and saves them on a stack of unfinished changes that you can reapply at any time.

  Stashing will leave you with a clean working directory, meaning it will look like the state of the last commit.

- `git stash -u` use the `-u` option to tell `git stash` to include untracked (unstaged) files, in addition to the tracked ones.

- `git stash pop` applies to the working directory the changes from the most recently created stash (also it will remove the stash from the stash list).

  If there are conflicts, you will need to resolve them.

- `git stash apply` it applies the stash, but it doesn't remove the stash from the stash list. **Usecase:** if you want to apply stashed changes to multiple branches.

- We can add multiple stashes on the stash stack. They will be stashed in the order you added them.

- `git stash list` displays the list of stashed changesets. Each entry is listed with an index, starting with `stash@{0}` for the latest stash.

- `git stash clear` deletes all the stashes recorded in the stash list.

- `git stash apply stash@{n}` applies a specific stash from your stash list, where `n` is the index of the stash. **Usecase:** when you have multiple stashes and want to apply one that is not the most recent.

- `git stash drop stash@{n}` removes a particular stash from the stash list without applying it.

## Stashing Workflow

While working on a file, you find a small bug in a separate file from a previous commit that needs to be fixed before you continue.

- `git stash` will store your work temporarily for later use in a hidden directory.

  At this point, you can switch branches and do work elsewhere, then commit.

- `git stash pop` restore the previous code you were working on (once the bug is fixed).
