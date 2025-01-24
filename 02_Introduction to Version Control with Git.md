# Introduction to Version Control with Git

Version control is an essential tool for managing code, ensuring smooth collaboration, and maintaining a reliable history of your project’s development. In this lesson, you’ll learn what version control is, the benefits it provides, and how to use Git to track changes locally.

## What is Version Control?

Version control is a system that helps you:

- Track changes made to your files over time.
- Restore earlier versions of your project if something goes wrong.
- Collaborate with others by managing contributions from multiple people.

### Real-World Analogy:

Imagine writing a book. Without version control, you might save separate files like `book_final_draft_v1.docx`, `book_final_draft_v2.docx`, and so on. Version control eliminates this chaos by keeping a single file and recording every change, along with who made it and when.

## Benefits of Version Control

1. **Backup and Restore:** Easily recover your project from any point in time.
2. **Collaboration:** Work on the same project simultaneously with others without overwriting changes.
3. **Change History:** Keep a detailed record of what changed, why, and who made the changes.
4. **Experimentation:** Test new ideas in isolation (branches) without affecting the main project.

## What is Git?

Git is a powerful version control tool that helps you track changes in your projects. It is:

- **Distributed:** Every user has a full copy of the project’s history.
- **Fast and Lightweight:** Designed for speed and efficiency.
- **Widely Used:** It’s the most popular version control tool, supported by platforms like GitHub, GitLab, and Bitbucket.

**Illustration:**

_A diagram showing how Git tracks file changes in a local repository and synchronises with a remote repository._

## Setting Up Git on Your System

### Installing Git

1. **Download Git:**

   - Go to [git-scm.com](https://git-scm.com/).
   - Download the installer for your operating system (Windows, macOS, or Linux).

2. **Install Git:**

   - Follow the setup wizard. On Windows, you’ll get options to configure Git Bash, a terminal interface for running Git commands.

3. **Verify Installation:**
   - Open your terminal or Git Bash.
   - Type git --version and press Enter.
   - If installed, it will display the Git version (e.g., git version 2.x.x).

## Initialising a Git Repository

### Step 1: Navigate to Your Project Folder

Open your terminal and use the cd command to move into your project directory:

```bash
cd path/to/your/project
```

### Step 2: Initialise a Git Repository

Run the following command to create a new Git repository in your project folder:

```bash
git init
```

This creates a hidden `.git` folder that tracks all changes.

## Basic Git Workflow

1. **Staging Changes** (`git add`)

   Before committing, you need to stage the files you want to include.

   - Use `git add` to stage a specific file:
     ```bash
     git add filename
     ```
   - To stage all files:

     ```bash
     git add .
     ```

     **Illustration:**

     _A visual representation showing the movement of a file from the working directory to the staging area._

2. **Committing Changes** (`git commit`)

   Once your changes are staged, commit them to save a snapshot of your work:

   ```bash
   git commit -m "Your commit message"
   ```

   - **Commit Message Tips:** Write a clear, concise description of what you’ve done (e.g., "Added homepage layout").
   -

## Tracking Changes Locally

### Workflow Summary

1. Modify your files in the working directory.
2. Stage your changes with git add.
3. Commit your changes with git commit.

### Illustration of the Git Workflow:

1. Working Directory: Files you’re editing.
2. Staging Area: Files prepared for a snapshot.
3. Repository: The saved snapshot (commit).

## Activity: Your First Git Workflow

1. **Initialise a Repository:**

   - Create a folder named `my-first-project`.
   - Inside, add an `index.html` file with a basic HTML structure.

2. **Run Git Commands:**

   - Initialise Git:
     ```bash
     git init
     ```
   - Stage your file:
     ```bash
     git add index.html
     ```
   - Commit your changes:
     ```bash
     git commit -m "Initial commit with index.html"
     ```

3. **Check the Commit History:**
   - Use the command:
     ```bash
     git log
     ```
   - Observe the commit hash, author, date, and message.

## Updating Git Defaults for Inclusivity

### Why Change the Default Branch Name?

Traditionally, Git repositories use `master` as the default branch name. However, to promote inclusivity and remove language that might be perceived as insensitive, the Git community has adopted `main` as the new default branch name. Many platforms, like GitHub, now use `main` by default for new repositories.

### How to Set `main` as the Default Branch

1. **Configure Git Globally:**
   You can set `main` as the default branch for all new repositories by running:

   ```bash
   git config --global init.defaultBranch main
   ```

   This ensures that whenever you initialise a new repository, the default branch will be named `main`.

2. **Change an Existing Repository's Default Branch:**

   If you already have a repository where the default branch is `master`, you can rename it:

   ```bash
   git branch -m master main
   git push -u origin main
   ```

   This renames the branch locally and updates the remote repository.

### Best Practices for Working with Default Branches

- Always align your local repository's default branch with the remote repository.
- Inform collaborators about the branch name change to avoid confusion.
- When contributing to open-source projects, check the project's default branch before starting work.

## Key Takeaways

- Git helps you manage changes in your project.
- Use `git add` to stage changes and `git commit` to save them.
- Always write meaningful commit messages.

By the end of this lesson, students will have successfully tracked changes in their first project using Git!
