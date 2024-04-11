# GitHub CLI

**GitHub CLI** is a powerful command-line tool that enables developers to handle several of the critical functionalities of GitHub from a terminal. We can see open issues, make pull requests, link pull requests to issues, and even merge pull requests without touching the GitHub UI.

## Installation

[**Download and Install GitHub CLI**](https://cli.github.com/)

After the installation is complete, open a new terminal and verify the default configuration:

- `gh --version`

- `gh --help` review the list of supported APIs and functionalities.

## GitHub CLI in Action

- `gh auth login` authenticate to GitHub

- `gh issue create --title "fix bug" --body "bug description"` create a GitHub issues within a repo.

  Follow the instruction in the terminal and select the forked repo to create the issue.

  Once the issue is created, you can view it on gh UI under the issues tab.

- `gh issue status` list all opened issues so far.

- `git switch -c "fix this bug"` create a new branch to fix the issue

- `git commit -a -m "bug fixed"` and `git push --set-upstream origin main` commit and push your changes to the remote.

- `gh pr create` now that feature branch is on the remote, create a pull request directly from gh CLI.

  Follow the prompts and add the proper title and description for the pull request. Mention the id of the issue in the description following `#[id]` format so that gh automatically links the pull request to the issue.

  You can check is the pull request appeared under the Pull Requests tab. Observe that the issue is linked to the PR.

- `gh pr merge` assuming the your PR is good to go, you can merge your PR using gh CLI as well.

- `gh issue status` check back the status of the issues and notice that the issue is now closed and no longed listed under open issues.
