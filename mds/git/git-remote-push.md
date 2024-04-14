# git remote

Before we can push anything up to GitHub, we need to tell Git about our remote repository on GitHub. We need to setup a "destination" to push up to.

In Git we refer to these "destinations" as remotes. Each remote is simply a URL where a hosted repository lives.

`git remote` view existing remotes. Add `-v` option for more info.

### Add new remote

A remote is really two things: a URL and a label. To add a new remote, we need to provide both to Git.

`git remote add myremote <url>`

_Anytime I use the name "myremote", I'm referring to this particular GitHub repo URL._

"Origin" is a conventional Git remote name, but it is not at all special. It's just a name for a URL. When we clone a GitHub repo, the default remote name setup for us is called "origin". We can change it.

By setting up a remote we are just telling Git about a remote repository URL. We have not "communicated" with the GitHub repo at all yet.

### Other commands

`git remote rename <old> <new>` rename a remote

`git remote remove <name>` delete a remote

## Pushing

After we have a remote set up, we can push our commits to GitHub.

`git push <remote> <branch>`

We need to specify the remote we want to push up to AND the specific local branch we want to push up to that remote.

`git push origin main` push up the "main" branch to the "origin" remote.

We can separately push branches up to the remote origin. From here, others can review our branch and merge our work into the main branch, making it part of the definitive project version.

<!-- git push -u origin main -->
