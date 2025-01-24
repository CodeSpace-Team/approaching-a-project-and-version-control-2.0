# Collaborating with GitHub

## Introduction: How Collaboration Works on GitHub

- Collaboration in GitHub happens when multiple people work on the same project.
- There are two common ways to collaborate:
  1. **Forked Repository Workflow** (for open-source or external projects).
  2. **Collaborator Workflow** (for private or team-based projects).

## Collaboration in a Forked Repository

When working on someone else’s project that you don’t have write access to:

- **Fork the repository** to create your own copy.
- **Make changes in your forked repository** (e.g., create a new branch).
- **Submit a pull request** to suggest your changes to the original repository.

### What is a Pull Request?

- A pull request is a way to suggest changes to the original repository.
- It allows you to show your work to the project owner or collaborators and request that your changes be merged into their project.
- Think of it as saying:
  "Here’s what I’ve done—please review and merge it if it’s okay."

### How to Create a Pull Request on GitHub:

1. Go to your forked repository on GitHub.
2. Make some changes and push them to a branch in your fork.
3. Click the "**Pull Requests**" tab in your repository.
4. Click "**New Pull Request**" and compare your branch with the original repository’s branch.
5. Add a description explaining your changes and submit the pull request.

### Best Practices for Forked Repositories:

1. **Keep Your Fork Up-to-Date:**
   - Regularly fetch and pull updates from the original repository to avoid conflicts:
     ```bash
     git remote add upstream <original-repo-URL>
     git fetch upstream
     git pull upstream main
     ```
2. **Create a New Branch for Changes:**
   - Avoid working directly on the main branch; create a feature branch instead:
     ```bash
     git checkout -b feature/new-feature
     ```
3. Write Clear Pull Request Descriptions:
   - Explain what changes you’ve made and why.

## Collaboration as an Invited Collaborator

When invited to work directly on a repository:

- **Accept the Invitation:**
  - Check your email or GitHub notifications for an invitation and accept it.
- **Clone the Repository Locally:**
  - Use `git clone` to get the repository on your computer:
    ```bash
    git clone <repo-URL>
    ```
- **Push Changes Using Pull Requests:**
  - Even as a collaborator, it’s a good practice to create a branch, push your changes, and open a pull request instead of merging directly.
  - This allows your team to review and discuss the changes before they’re integrated into the main branch.

**Why Use Pull Requests as a Collaborator?**

- Ensures code quality and prevents mistakes.
- Encourages team communication and feedback.
- Helps keep the main branch stable by reviewing and testing changes first.

### Best Practices for Direct Collaboration:

1. Work on Feature Branches:
   - Always create separate branches for your changes to avoid conflicts.
2. Pull Before Making Changes:
   - Ensure your local copy is up-to-date by pulling the latest changes:
     ```bash
     git pull origin main
     ```
3. Communicate with Your Team:
   - Use GitHub Issues or comments to discuss ideas or potential changes before starting work.
   - When your work is ready, open a pull request to propose your changes.
   - Use the pull request to describe your changes clearly and engage in discussions with team members about the implementation.
   - Address feedback in the pull request before merging your changes.

## Fetching and Pulling Updates

Whether working on a forked repository or as a collaborator, keeping your local copy updated is essential:

- **Fetching Changes `(git fetch`):**

  - Use this to see if there are new updates in the remote repository without applying them.
  - Example:
    ```bash
    git fetch origin
    ```

- **Pulling Changes (`git pull`):**

  - Use this to fetch and apply updates:
    `bash
    git pull origin main  
    `
    **Why It’s Important:**

- Prevents merge conflicts by ensuring your local copy matches the remote repository before making changes.

## Activities

1. **Fork and Collaborate:**

   - Fork a sample repository, make changes on a branch, and submit a pull request to the original repository.

2. **Simulate Team Collaboration:**

   - Be invited as a collaborator to a repository.
   - Clone the repository, create a branch, make changes, and push them directly.

3. Practice Updating Your Repository:
   - Use `git fetch` and `git pull` to update your local repository from the remote one.
