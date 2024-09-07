
# Introduction to GitHub and Workflow
This is the repository for the upcoming git and github session, below is the content flow that we expect to be able to cover in the session.


## 1. Introduction to GitHub

### What is GitHub?
**GitHub** is a web-based platform that provides hosting for Git repositories. It is used for version control and collaboration, allowing developers to work together on projects from anywhere. Key features of GitHub include:
- Hosting Git repositories.
- Enabling collaboration through pull requests and issues.
- Providing tools for continuous integration (CI) and project management.

### GitHub Workflow
A typical workflow on GitHub includes:
1. **Repositories**: A central place where the project files are stored.
2. **Branches**: Used to work on different features or fixes without affecting the main codebase.
3. **Commits**: Snapshots of changes made to the code.
4. **Pull Requests**: A request to merge changes from one branch into another.

---

## 2. GitHub Workflow

### Creating a Repository
- On GitHub, click the "New" button in the repository section to create a new repository.
- Give the repository a name, optionally add a README, and click "Create Repository".

### Cloning a Repository
```bash
git clone <repository_url>
```
- Clone the repository to your local machine to start working on it.

### Making Changes
- Modify files in your local repository, then stage and commit the changes using Git.
```bash
git add <file>
git commit -m "Your message"
```

### Creating a Branch
```bash
git branch <branch_name>
git checkout <branch_name>
```
- Create and switch to a new branch where you will make changes.

### Pushing Changes
```bash
git push origin <branch_name>
```
- Push your changes to the new branch on GitHub.

### Creating a Pull Request
- On GitHub, open the repository and click the "New Pull Request" button.
- Select the branch you want to merge from and the branch you want to merge into (e.g., from `feature-branch` to `main`).
- Provide a title and description for the pull request and submit it for review.

---

## 3. Hands-On Activity

### Creating Pull Requests
1. Create a branch in a repository and push changes to it.
2. Submit a pull request to merge your changes into the `main` branch.

### Review and Merge
1. Review the submitted pull requests.
2. Test the changes and leave comments if necessary.
3. Merge the pull request into the `main` branch.

---

## 4. GitHub Alternatives

### Bitbucket
**Bitbucket** is another web-based platform for hosting Git repositories. It offers free private repositories and integration with Jira for project management.

### GitLab
**GitLab** provides Git repository hosting with built-in **CI/CD** tools, allowing you to automate testing and deployment.

### Other Alternatives
- **SourceForge**: One of the original platforms for open-source projects.
- **AWS CodeCommit**: A fully managed source control service that hosts Git repositories in AWS.

---

## 5. Managing Projects on Git and GitHub

### Project Boards
GitHub **Project Boards** help organize and manage your project tasks. They allow you to create task cards and track their progress.

### Issues and Labels
**Issues** are used to track bugs, enhancements, and other project tasks. You can use **Labels** to categorize issues based on their priority or type (e.g., bug, enhancement).

### Milestones
Set **Milestones** to track the progress of your project and measure what’s been accomplished toward a release or a big goal.

### Collaborators and Permissions
You can invite **Collaborators** to your repository and manage their permissions by going to the repository settings and selecting "Manage Access."
