# Fetch and Pull

## Fetching

Fetching allows us to download changes from a remote repository, but those changes will not be automatically integrated into our working files.

`git fetch <remote>` command fetches branches and history from a specific remote repository. It only updates remote tracking branches.

`git fetch origin` would fetch all changes from the origin remote repository.

`git fetch <remote> <branch>` fetch a specific branch from a remote.

For example, `git fetch origin master` would retrieve the latest information from the master branch on the origin remote repository.

Again, this command will not merge changes from the remote into your local repo, it brings those changes into a remote branch.

## Pulling

`git pull` another command we can use to retrieve changes from a remote repository.

`git pull = git fetch + git merge` Unlike fetch, pull updates our HEAD branch with whatever changes are retrieved from the remote.

`git pull <remote> <branch>` specify a particular remote and branch we want to pull.

`git pull origin master` would fetch the latest information from the origin's master branch and merge those changes into our current branch.

Just like with git merge, it matters where we run this command from. Whatever branch we run it from is where the changes will be merged into.

Pulls can result in merge conflicts.

If we run `git pull` without specifying a particular remote or branch to pull from, git assumes the following: (1) remote will default to origin. (2) branch will default to whatever tracking connection is configured for your current branch.

## Cloning / Remote Branches

After cloning a remository, we get 2 branches:

- `master` a regular branch reference, I can move this around myself.

- `origin/master` This is a **"Remote Tracking Branch"**. It's a reference to the state of the master branch on the remote. I can't move this myself. It's like a bookmark pointing to the last known commit on the master branch on origin.

### Remote Tracking Branches

They follow this pattern `<remote>/<branch>`

`origin/master` references the state of the master branch on the remote repo named _origin_.

`git branch -r` to view the remote branches our local repo knows about.

We can make local commits and the `master` branch reference will update, but `origin/master` remote reference will stay the same.

### Remote Branches

For example, you've cloned a repository, we have all the data and Git history for the project at that moment in time. However, that does not mean it's all in my workspace. The github repo has a branch called `bugfix`, but when I run `git branch` I don't see it on my machine. All I see is the `master` branch.

`git branch -r` to view the remote branches our local repo knows about.

By default, the `master` branch is already tracking `origin/master`.

If we want to work on `bigfix` remote branch, run `git switch bugfix` to create a new local branch from the remote branch of the same name. This will create a local `bugfix` branch and set it up to track the remote branch `origin/bugfix`.
