[&larr; Back](./README.md)

# Git

## Table of Content

- [Git Introduction](#git-introduction)
- [Git and GitHub Differences](#git-and-github-differences)
- [Git Configuration](#git-configuration)

<br>

## Git Introduction

- **Git** - Version Control System
- **Version Control System** - a software that tracks and manages changes to files over time.

_Version Control Systems_ allow users to revisit earlier versions of the files, compare changes between versions, undo changes, collaborate and share, combine changes and more.

Thus, **Git** is a software that allows you to keep track of changes made to a project over time. It works by recording and storing changes you make to a project, then allowing you to reference them as needed.

Git is _(primarily)_ a **Terminal Tool**. To use it, we run various git commands in a Unix Shell.

**Git History:** Linus Torvalds is the creator and main developer behind Linux and Git. The first official Git release came in 2005.

**Who Uses Git:** Engineers and Coders, Tech-Adjacent Roles like Designers (for collaborating reasons), Governments, Scientists, Writiers, Anyone (keeping a dairy, drafting PhD).

<br>

## Git and GitHub Differences

**Git** is the version control software that runs locally on your machine. You don't need to register for an account. You don't need the internet to use it. You can use Git without ever touching GitHub.

**GitHub** is a service that hosts Git repositories in the cloud and makes it easier to collaborate with other people. You do need to sign up for an account to use GitHub. _It's an online place to share work that is done using Git._

After finishing the Git repository on our local machine, we can upload the history to GitHub to share with others.

| Git                                         | GitHub                                           |
| ------------------------------------------- | ------------------------------------------------ |
| Git is a Software                           | GitHub is a Service                              |
| Git is maintained by Linux                  | GitHub is maintained by Microsoft                |
| Git can manage source code history          | GitHub is a hosting service for git repositories |
| Git was released in 2005                    | GitHub was launched in 2008                      |
| focused on version control and code sharing | focused on centralized source code hosting       |
| Git has no user management feature          | GitHub has a built-in user management feature    |

<br>

## Git Configuration

`git --version` command to see if git is installed, or [Install Git](https://git-scm.com/)

**Configuring Git Name & Email** that Git will associate with your work:

```
git config --global user.name "John"
git config --global user.email "me@example.com"
git config user.name // check the configured name
```

When we get to GitHub, you’ll want your Git email address to match your GitHub account.

<br>
