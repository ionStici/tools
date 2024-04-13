# Set up your GitHub Project Board

This workflow is focused on frontend projects.

## Customizing the Board

_Set up columns that represent different stages of the development process. Column examples:_

### 1. To Do

Here you gather all incoming tasks such as new features, bug fixes, or improvements that need to be addressed (column for new tasks that have been identified but not yet started).

- **Purpose:** To capture all tasks that need attention.
- **Actions:** Tasks remain here until they are fully scoped and assigned.

### 2. Design

This column is dedicated to tasks involving design work, such as creating wireframes, prototypes, and final design specs that need approval before coding starts.

- **Purpose:** To focus on tasks that require visual assets and design approval.
- **Actions:** Tasks are moved here from "To Do" when they are ready to be worked on by designers.

### 3. Ready for Development

Once designs are approved and specs are ready, tasks are moved to this column. It signifies that the tasks are fully prepared for developers to start coding.

- **Purpose:** To queue up tasks that are ready for coding.
- **Actions:** Design-approved tasks are moved here to await development.

### 4. In Progress

This column represents tasks that are currently being worked on. It's important for tracking active development and ensuring that progress is being made on the right tasks.

- **Purpose:** To monitor ongoing development work.
- **Actions:** Developers move tasks here when they begin working on them, indicating active development.

### 5. Review

After development, tasks move to the review stage where code and functionality are reviewed. This can involve peer reviews, code quality checks, and initial testing by other team members.

- **Purpose:** To ensure the quality and functionality of the work before it goes into further testing.
- **Actions:** Completed tasks are moved here for peer review and initial feedback.

### 6. Testing

Testing across different browsers and devices to ensure compatibility and responsiveness. Testing may also include performance and security checks.

- **Purpose:** To thoroughly test the developed features for bugs and issues.
- **Actions:** Tasks are moved here after passing the initial review, awaiting QA testing and bug reporting.

### 7. Blocked

Sometimes, tasks cannot proceed due to external dependencies or issues that need resolution. This column helps in identifying and tracking such impediments.

- **Purpose:** To highlight tasks that are stalled due to dependencies or unresolved questions.
- **Actions:** Move tasks here when they cannot progress; regularly review and try to resolve blockers.

### 8. Done

Tasks that have been completed, tested, and are confirmed to meet the requirements are moved to this column. It signifies that no further action is required on these tasks.

- **Purpose:** To track completed and approved tasks.
- **Actions:** Move tasks here once they have passed all stages and are fully implemented.

## Managing Issues

- **Issues:** Ensure that each issue contains all the necessary information for understanding and completing the task.
- **Labels:** Create and use a standardized set of labels to categorize issues.
- **Milestones:** Group issues into milestones based on release cycles or major features.

## Managing Pull Requests

- **Linking:** Link Pull Requests to Issues.
- **Review:** Review all Pull Requests before merging to ensure quality and consistency.

## Automation

### 1. Automatically move tasks to "In Progress"

Set up automation to move tasks from "Ready for Development" to "In Progress" when a branch is created or a pull request is opened and linked to an issue.

- **Trigger:** Opening a pull request or creating a branch linked to an issue.
- **Action:** Move the linked issue to the "In Progress" column.

### 2. Shift tasks to "Review"

Once development is complete, and the changes are submitted through a pull request, the task should move to the "Review" column, where it can undergo peer review.

- **Trigger:** Marking a pull request as ready for review.
- **Action:** Move the associated issue to the "Review" column.

### 3. Push tasks to "Done"

After a pull request is reviewed and merged, it indicates that the task is completed. Setting up an automation to move tasks to "Done" when the pull request is merged helps in tracking completion.

- **Trigger:** Merging a pull request linked to an issue.
- **Action:** Move the linked issue to the "Done" column.

```yaml
# GitHub Actions
# If a pull request is merged into the main branch, it moves the linked issue to the "Done" column

name: Workflow Automation

on:
  pull_request:
    types: [opened, synchronize, closed]
    branches:
      - main

jobs:
  automate-project-movement:
    runs-on: ubuntu-latest
    if: github.event.pull_request.merged == true
    steps:
      - name: Move to Done
        uses: alex-page/github-project-automation-plus@v0.8.1
        with:
          project: "Project Name"
          column: "Done"
          repo-token: ${{ secrets.GITHUB_TOKEN }}
```
