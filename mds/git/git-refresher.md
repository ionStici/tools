# Git Exercises

## Part 1 - Fundamentals

1. Initialize a git repository
2. Configure git name and email only for this repo
3. Check the current status
4. Add a file to the staging area
5. Make a commit
6. Amend a small change
7. Add a file to the staging area, then make further changes to it
8. Compare the difference between the staged changes and the working directory
9. Add that file to the staging area again and make a new commit
10. Log the commit history

## Part 2 - Branching

1. Create a new branch named "feature"
2. List all branches
3. Switch to "feature" branch
4. Make changes in the "feature" branch and commit them
5. Switch back to "master"
6. Merge the "feature" branch into "master"
7. Delete the "feature" branch

## Part 3 - Backtracking

1. Move HEAD to a previous commit and identify what changed
2. Create a new branch, list all branches, observe "HEAD detached at"
3. Switch to the new branch and make a commit
4. Switch back to "master" and merge the new branch then delete it
5. Log and examine the commit history

### Restore

1. Make some changes to a file, then use `restore` to discard them
2. Add a file to the staging area, then use `restore` to unstage it
3. `restore` a single file to its state from a previous commit

### Reset

1. Peform a mixed reset
2. Peform a soft reset
3. Peform a hard reset
4. Spot the differences

## Part 4 - Rebasing

1. Create a new branch and make a commit on it
2. Rebase the new branch on "master"
3. Log the commit history and spot the details

## Part 5 - Stashing

1. Perform 3 git stashes
2. List all stashes
3. Apply the first stash you made, using its order number
4. Manually delete the stash you applied
5. Pop the latest stash (so that it deletes automatically)
6. Apply the last stash (so that it will remain in the stash list)
7. Clear the stash list

## Part 6 - Aliases

Configure and use the following aliases:

```
aa = add .
cm = commit =m
```

## Part 7 - Tags

1. Create a lightweight tag
2. Create an annotated tag on a particular commit
3. List all tags
4. Move HEAD at a particular commit using a tag
5. Delete a tag
6. Push tags to a remote
