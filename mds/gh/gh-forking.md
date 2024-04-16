# Forking a Repository

**Forking a Repository on GitHub** - making a copy of a public repository into your own account so that you can modify the project freely.

To fork a GitHub repository - **click `Fork` on the repo page**.

## Get Updates

To get updates from the main project into our forked repository, copy the parent's project url, then in the project's terminal run:

```
git remote add upstream <url>
```

After the upstream is set to the parent repo, when we want to update the repo, use the command:

```
git fetch upstream
```

Then, our forked repo will become up to date with the parent repo.

## Fork & Clone Workflow

1. I **fork** the original project repo on GitHub

2. I **clone** my fork to my local machine

3. I **add a remote** pointing to the original project repo. This remote is often named "upstream"

4. I **make changes** and add/commit on a feature branch on my local machine

5. I **push up** my new feature branch to my forked repo (usually caled "origin")

6. I **open a pull request** to the original project repo containing the new work on my forked repo

7. Hopefully **the pull request is accepted** and my changes are merged in.
