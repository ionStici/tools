# git remote

Before we can push anything up to GitHub, we need to tell Git about our remote repository on GitHub. We need to setup a "destination" to push up to.

In Git we refer to these "destinations" as **remotes**. Each remote is simply a URL where a hosted repository lives.

`git remote` view existing remotes. Add `-v` option for additional info.

## Add a new remote

To add a new remote to a git repository, we need to provide a remote **name** and the repository's **URL**.

`git remote add remote_name <remote-url>`

"Origin" is a conventional Git remote name, but it is not at all special. It's just a name for a URL. When we clone a GitHub repo, the default remote name setup for us is called "origin". We can change it.

By setting up a remote we are just telling Git about a remote repository URL. We have not "communicated" with the GitHub repo at all yet.

## Pushing

After we have a remote set up, we can push our commits to GitHub.

`git push <remote> <branch>`

We need to specify the remote we want to push up to AND the specific local branch we want to push up to that remote.

`git push origin main` push up the "main" branch to the "origin" remote.

We can separately push branches up to the remote origin. From here, others can review our branch and merge our work into the "main" branch, making it part of the definitive project version.

## Other related commands

- `git remote rename <old> <new>` rename a remote

- `git remote remove <name>` delete a remote

- `git branch -M main` rename the current branch to `main` (github convention)

- `git push -u origin main` the `-u` option (upstream) sets the local branch to track the remote branch, enabling simplified future commands for pulling and pushing changes between these branches.
