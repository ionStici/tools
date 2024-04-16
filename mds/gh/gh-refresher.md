# GitHub Project

## Part 1 - Remotes

1. Create a local repository and make an initial commit
2. Create 2 more branches and make a commit on each

<div></div>

3. Create a new repository on GitHub
4. With the GitHub repo you created, add it as remote to your local repo (name it `origin`)

<div></div>

5. Rename the `master` branch to `main` and push the local repo to its remote (set upstream)
6. View existing remotes

<div></div>

7. Push another branch to the remote
8. List all branches, then list the branches that the remote knows about

<div></div>

9. Delete the remote tracking branch you pushed at step 7
10. Delete the remote from your local repository

<div></div>

11. Merge both branches you have in your local repository
12. Add again the remote and push the progress

## Part 2 - Fetching and Pulling

1. Hard reset your project to the first commit
2. Compare your local branch with the remote tracking branch using `diff`

<div></div>

3. Set up a `dev` local branch to track `origin/main`
4. Merge `origin/main` or the `dev` local branch into `main`

<div></div>

5. Delete the `dev` branch and perform a hard reset again
6. Pull the `main` branch from `origin` (so that merge will happen)

## Part 3 - Pull Request

1. Create a `dev` branch and make a commit
2. Push the `dev` branch to the remote

<div></div>

3. Open a pull request on the `dev` branch. Give a title that explains the purpose of the pull request. Add a description that reflects the thought process behind the new branch. Add a commend after submitting the PR.
4. Add a new commit on the `dev` branch, then push `dev` to the remote. Check it on GitHub at the PR section.

<div></div>

5. Create an issue and link it to the pull request
6. Merge the pull request, then delete the `dev` branch using the GitHub UI

<div></div>

7. Pull the `main` branch from the remote
8. Delete the `origin/dev` branch from your local repo using the `-dr` option

## Part 4 - Forking

1. Fork a project on GitHub
2. Clone the fork on your local machine
3. Add a remote pointing to the original project repo (name the remote "upstream")
4. Fetch the "upstream" remote to see if everything is up to date
5. Create a new branch and make a commit
6. Push the branch to the forked "origin" remote
7. Open a pull request to the original project repo containing the new work from your forked repo
