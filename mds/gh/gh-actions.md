# GitHub Actions

[**GitHub Actions**](https://github.com/features/actions)

**GitHub Actions:** are an automation and CI/CD feature that allows you to automate your workflow by creating workflows to build, test, and deploy your code based on a series on events (like a push or a pull request).

**Key Features:**

- **Workflows:** Defined by a YAML file in your repo, workflows are custom automated processes.
- **Events:** Workflows are triggered by specific events within your GitHub repo, such as pushes, pull requests, or even scheduled events.
- **Jobs and Steps:** A workflow consists of jobs that can run multiple steps. These steps can execute commands, run scripts, or use actions created by the GitHub community.

**How to Use:**

1. Add a YAML file to the `.github/workflows` directory in your repo.
2. Define the events that trigger the workflow.
3. Specify the jobs and steps that should be executed.

**Example Workflow:**

```yaml
name: Example CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Run a one-line script
        run: echo Hello, world!
      - name: Run a multi-line script
        run: |
          echo Add other commands
          echo Build something
```

This YAML file defines a simple CI workflow that triggers on every push to the repository, checks out the code, and runs some shell commands.
