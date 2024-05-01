# Open Source

## Overview

**Open Source Software** is software whose code is free to view, modify, and distribute. Developers can view the code, suggest changes, point out issues that need to be fixed. It is usually created and maintained by a community of volunteer software developers who collaborate on websites like GitHub.

Every active open source software project has one or more **maintainers**. Besides writing code, their main priority is to review and organize contributions from others. The people who make those contributions are called **contributors**. These are people who submit new code, documentation, or even bug reports to open source projects.

Open Source provides a standard way of implementing common features that the entire developer community can build, test, and maintain together. Many of the commonly used tools in the industry, such as operating systems, internet browsers, and coding languages, are open source projects.

Open source presents important opportunities for develoeprs. Working on an open source project is a great way to network with and learn coding and communication skills from software developers all over the world.

## Open Source Repository Docs

Git repositories, or code bases, are often hosted online using services such as GitHub.

On GitHub, we can configure which groups of people may view or make changes to the source code of our public repositories.

- **README.md** is the standard file for basic repository documentation: Title, summary, code snippet examples.

- **LICENSE.md** file is used to describe the licensing terms for the repository: restrictions for what circumstances it is allowed to be used.

  Commonly used license: The MIT license. Resource: [ChooseALicense.com](https://choosealicense.com/).

- **CONTRIBUTING.md** file for contributing guidelines, see: [example](https://contributing.md/example/).

- **CODE_OF_CONDUCT.md** files contain policies regarding what behavior is acceptable or not.

  Standard code of conduct: [Contributor Covenant](https://www.contributor-covenant.org/).

### README.md Files in Open Source Projects

Standard practice: write a project overview inside a README.md file, which contains:

- The project name -> What the project does
- How to get started contributing to the project
- Links to other relevant documentation, such as architecture overviews

## Contributing to an Open Source Project

### Contributing Issues

An **issue** is a written description of something that could be improved about a project, such as a bug report, or a feature request.

Most open source repositories have an **issue tracker**, which is a site where people submit issues for that project.

The project maintainers then use the issue tracker to keep track of which issues are being worked on and by whom.

Three common types of issues:

- **Bug reports** let the maintainers know about a bug or error in their project.
- **Feature requests** suggest an entirely new feature or behavior for the project.
- **Clarifying questions** ask a question about the project that isn’t already answered by the project’s documentation.

GitHub has an issue tracker built into every project, but some maintainers may choose to use different software such as [Jira](https://www.atlassian.com/software/jira) or [Trello](https://trello.com/). Before submitting an issue to an open source project, be sure to check out the project’s README for any specific instructions.

An issue report template would look like this:

```
## Expected Behavior
I expected clicking the "User Profile" link in the dropdown menu to bring me to my profile page.

## Actual Behavior
Clicking the "User Profile" link did nothing.

## Browser Version
Safari 16
```

The label **good first issue** indicates that a GitHub issue is suitable for new contributors.

### Contributing Documentation

Another type of open source contribution is to write documentation.

Types of documentation:

- **README:** introduces people to the project and often contains links to the rest of the project’s documentation.
- **Getting started guide:** a short demonstration of how to use the project for the most simple use cases.
- **Usage guide:** a more detailed explanation of how to use all of the project’s features.
- **Contribution guide:** an explanation of how to set up the project on a local machine for the purpose of contributing code.

### Contributing Code

Before writing our first code contribution, good idea to first read through the issues in the issue tracker. Many project maintainers will put the “good first issue” label on issues that they think are best suited for beginners.

The issue tracker will also show you which issues are **assigned** – meaning they have someone actively working on them. Checking whether an issue is assigned will prevent you from working on the same issue as somebody else. If you want to work on an issue, make sure to leave a comment saying you’re working on it so the maintainers can assign it to you and save others the same trouble.

If you’ve found an issue you want to work on but don’t know where to start, it’s okay to ask for help! Many project maintainers and experienced contributors are willing to pair program with newcomers. Leave a comment on the issue asking if anybody would be willing to pair, and don’t get discouraged if you don’t hear back immediately. Open source maintainers are often busy, and it may take them some time to reply.

### Other Ways to Contribute

- Review contributions
- Triage issues (e.g. by adding labels or identifying and deleting duplicates)
- Respond to questions relating to the project on StackOverflow or Reddit
- Make video tutorials or host workshops for the project

### Tips to create a strong contribution

- **Carefully read any available guidelines.** If a project has contribution guidelines, be sure to read them over and follow any instructions provided. This will help you avoid any common pitfalls that might cause your contribution to be rejected.
- **Ask for feedback.** Before you invest a lot of time in a contribution, talk to the maintainers about what you have in mind. They may give you some helpful guidance.
- **Look at other contributions.** Read through other issues or pull requests, especially the ones that have already been accepted, and use them as guidance while crafting your own contributions.
