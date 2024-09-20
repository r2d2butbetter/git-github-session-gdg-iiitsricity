
# 1. Introduction to Version Control Systems (VCS)
### Definition and Importance
A **Version Control System (VCS)** is a tool that helps track changes to files over time. It allows multiple people to collaborate on a project, maintain version history, and revert to previous states if needed. VCS is crucial for software development because:
- It enables collaboration among team members.
- Keeps a history of changes.
- Facilitates the rollback of mistakes.
- Tracks and manages code across branches.
- Other examples include Subversion(centralized VCS), Mercurial etc.

### Why Git?
Git is one of the most popular VCS, known for its **distributed** nature. Key advantages of Git include:
- **Speed**: Git is very fast compared to other VCS.
- **Distributed**: Every developer has a full copy of the repository, allowing for offline work.
- **Efficient Branching**: Git provides lightweight and flexible branching and merging strategies.

---

# 2. Brief on Git Installation
### Pre-installed on Ubuntu
On most Ubuntu systems, Git comes pre-installed, so no installation steps are required. You can verify this by running the following command:
```bash
git --version
```
### Installing Git on Windows and Linux
To install Git on Windows, you can follow these steps:
1. Visit the official Git website at [https://git-scm.com/downloads](https://git-scm.com/downloads).
2. Download the Git installer for Windows.
3. Run the installer and follow the on-screen instructions.
4. Once the installation is complete, you can open a command prompt and verify the installation by running the following command:
```bash
git --version
```
For Linux systems, you can use the package manager to install Git. For example, on Ubuntu, you can run the following command:
```bash
sudo apt-get install git
```

---

# A little bit of setup
### Git Config Basics

To set your username and email in Git, use the following commands:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

This is the name that shows up in commits so that git can identify who did what commit.
You can also set it locally for a repo, using the --local flag instead of the --global flag.

# 3. Basic Git Commands

### Creating a Repository
```bash
git init
```
Initializes a new Git repository in the current directory.

### Cloning a Repository
```bash
git clone <repository_url>
```
Clones an existing repository from a **remote location** (Like github, which we will look at later on).

### Checking Status
```bash
git status
```
Displays the state of the working directory and the staging area.

### Adding Changes
```bash
git add <file>
```
Stages file changes for the next commit.

### Committing Changes
```bash
git commit -m "message"
```
The below can be used too, but it will open a prompt and ask you to type the "message"

```bash
git commit
```
Commits staged changes with a descriptive message.

### Viewing History
```bash
git log
```
Shows the commit history of the repository.

---

# How to Write Good Commit Messages

- **Subject Line**: Use a concise summary (max 50 characters) in the **imperative mood** (e.g., "Add new feature").
- **Body (optional)**: Include detailed explanation if needed:
    - Explain the "why" behind the change.
    - Describe the impact or reasoning.
- **Issue References**: Link to related issues using `Fixes #<issue-number>` or `Closes #<issue-number>` to automatically close them.
- **Formatting**:
    - Keep subject line under 50 characters.
    - Use present tense, imperative mood.


# 4. Hands-On Activity

### Creating a Repository
Guide:
1. Create a new directory.
2. Navigate to the directory.
3. Initialize a new Git repository using `git init`.

### Making Changes
1. Create or modify a file in the repository.
2. Use `git add <file>` to stage the changes.
3. Use `git commit -m "your message"` to commit the changes.
4. View the commit history with `git log`.

---

# 5. Advanced Git Concepts

### Branches
**Branches** allow developers to work on separate features without affecting the main codebase. 

#### Creating a Branch
```bash
git branch <branch_name>
```

#### Switching Branches
```bash
git checkout <branch_name>
```

#### Merging Branches
```bash
git merge <branch_name>
```
Merges changes from the specified branch into the current branch.
**We will face issues with this merge part later, don't worry for now**

### Pulls and Fetches
- **git fetch**: Retrieves changes from the remote repository without applying them.
- **git pull**: Fetches and merges changes from the remote repository into the current branch.

### Rollbacks
- **git revert**: Reverts a specific commit by creating a new commit that undoes the changes.
- **git reset**: Moves the current branch pointer to a previous commit, potentially discarding commits.

---

# 6. Merge Conflicts and Resolution

### What are Merge Conflicts?
Merge conflicts occur when Git cannot automatically merge changes from different branches. This usually happens when the same lines of code are modified differently in each branch.

### Resolving Conflicts
1. Open the conflicting files and manually resolve the differences.
2. After resolving, use `git add` to mark the conflict as resolved.
3. Finally, commit the resolved changes using `git commit`.

---

# Conclusion

### Recap
- **Version Control** is essential for collaboration and code management.
- **Git** provides fast, distributed version control with efficient branching.
- You’ve learned basic and advanced Git commands, including handling merge conflicts.




# Part 2- Introduction to GitHub and Workflow

## 1. Introduction to GitHub

### What is GitHub?
**GitHub** is a web-based platform that provides hosting for Git repositories. It is used for version control and collaboration, allowing developers to work together on projects from anywhere. Key features of GitHub include:
- Hosting Git repositories.
- Enabling collaboration through pull requests and issues.
- Providing tools for continuous integration (CI) and project management.
- Alternatives to github include, gitlab, sourceforge, codeberg

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

- If you are working with someone else's repo and you are not a collaborator in it, you are required to fork it before cloning it.
- A Github fork creates a personal copy of a repository, allowing you to make changes and propose updates via pull requests.

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

## 4. Managing Projects on Git and GitHub

### Project Boards
GitHub **Project Boards** help organize and manage your project tasks. They allow you to create task cards and track their progress.

### Issues and Labels
**Issues** are used to track bugs, enhancements, and other project tasks. You can use **Labels** to categorize issues based on their priority or type (e.g., bug, enhancement).

### Milestones
Set **Milestones** to track the progress of your project and measure what’s been accomplished toward a release or a big goal.

### Collaborators and Permissions
You can invite **Collaborators** to your repository and manage their permissions by going to the repository settings and selecting "Manage Access."



### Q&A
Feel free to ask any questions or clarifications.
