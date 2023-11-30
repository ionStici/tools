[&larr; Back](./README.md)

# GitHub Introduction

[**GitHub**](https://github.com/) is a hosting platform for git repositories that helps people share and collaborate.

_Why GitHub?_

- **Collaboration** - GitHub is an essential tool for working on a project with other people.
- **Open Source Projects** - GitHub is the home of open source projects on the internet. If you want to contribute to open source projects, you'll need to work with GitHub.
- **Exposure** - Your GitHub profile acts as a resume in the hiring process.
- **Stay Up To Date** - Being active on GitHub is the best way to stay up to date with the projects and tools you rely on.

<br>

## Hosting on GitHub

How do we get our code on GitHub?

**Option 1:** _Existing Repo._ If we already have an existing repo locally that we want to get on GitHub.

1. Create a new repo on GitHub
2. Connect your local repo (add a remote)
3. Push up your changes yo GitHub

**Option 2:** _Start from Scratch._ If you haven't begun work on your local repo..

1. Create a brand new repo on GitHub
2. Clone it down to your local machine
3. Do some work locally
4. Push up your changes to GitHub

<br>

## Pushing a local Repo to GitHub

- **Authentication** - first, we need to generate an SSH key that will authenticate our local machine. In your GitHub settings, go to SSH keys and generate a new key that you will use in your terminal when pushing repositories for the first time.

- **Create a new repository on GitHub**

- **Connect the newly created repository on GitHub with your existing work** - on the repo page, copy the suggested commands and paste them into the project's local terminal. This will create a remote repository and will push your local repo to the remote repo.

- Type your GitHub username and password if prompted.

- At this point, you should be able to see your local repo hosted on GitHub.

<br>

## Cloning

We can clone a remote repository hosted on GitHub, all we need is the repo URL.

`git clone <url> clone_name` clone a repository.

Git will retrieve all the files associated with the repository and will copy them to your local machine. In addition, Git initializes a new repository on your machine, giving you access to the full Git history of the cloned project.

We can clone any public repositories, we don't need any kind of permission.

_p.s._ `git clone` is a standard git command, it can be used to clone repositories that are hosted anywhere, not just on GitHub.

<br>

## GitHub Flow

Following a specific workflow allows the project to more in more orderly way.

_Basic workflow used with GitHub:_

1. Create a branch
2. Commit changes
3. Create a pull request
4. Review pull request
5. Merge and delete branch

By sticking to this workflow, team members are able to isolate their work and avoid any conflicting code from being merged.

<br>

## GitHub Repos

- **Public Repos** - are accessible to everyone on the internet.

- **Private Repos** - are only accessible to the owner and people who have been granted access.

- **README** files are used to communicate important information about a repository.

- **GitHub Gists** - are a simple way to share code snippets and useful fragmets with others.

- **GitHub Pages** - are public (static) webpages that are hosted and published via GitHub.

<br>
