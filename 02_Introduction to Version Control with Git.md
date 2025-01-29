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

Open your project in VS Code and open the terminal integrated into VS Code.

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

2. **Committing Changes** (`git commit`)

   Once your changes are staged, commit them to save a snapshot of your work:

   ```bash
   git commit -m "Your commit message"
   ```

   - **Commit Message Tips:** Write a clear, concise description of what you’ve done (e.g., "Adds homepage layout").

## Tracking Changes Locally

### Workflow Summary

1. Modify your files in the working directory.
2. Stage your changes with git add.
3. Commit your changes with git commit.

### Illustration of the Git Workflow:

1. Working Directory: Files you’re editing.
2. Staging Area: Files prepared for a snapshot.
3. Repository: The saved snapshot (commit).

   <img src="./images/git local repo.png" alt="Git local and remote" width="400" height="250">

## Activity: Your First Git Workflow

1. **Initialise a Repository:**

   - Open the `my-project` folder (created in lesson 1) in VS Code.
   - Open the terminal in VS code and run the command below to initialise Git
     ```bash
     git init
     ```

2. **Adding Existing files:**

   - After initializing git, you will notice some existing files changing to green in colour, this means they have changes that are currently untracked in git, you need to stage and commit them to be saved to the repo.

     On **VS Code Activity Bar** (very left panel) there is a Source Control icon, clicking it will open the Source Control panel which can help you visualize and make git changes. On the image below it shows that there are 3 new `**Untracked (U)**` files.

      <img src="./images/VS git gui and unstanged changes.png" width="240" height="200">

     These files are not currently being tracked by Git. They has been created or added to your workspace but haven't been staged or committed yet.

   - Run git the following command to stage all files.

     ```
     git add .
     ```

     After running the above command, your files will move to the `Staged` area.

      <img src="./images/Changes after staging.png" width="240" height="200">

     The commit message can be written in the input bar just above the blue **Commit** button and then pressing the Commit button or it can be writen in the terminal as previously done

   - Commit your changes:
     ```bash
     git commit -m "Adds index, styles and readme files"
     ```

3. **Making changes:**

   - Make some changes to your index.html file like changing the text within h1 tag to "Welcome to My **First** Project"
     ```html
     <h1>Welcome to My First Project</h1>
     ```
   - Stage your file:
     ```bash
     git add index.html
     ```
   - Commit your changes:
     ```bash
     git commit -m "Modifies project heading"
     ```

4. **Check the Commit History:**
   - Use the command:
     ```bash
     git log
     ```
   - Observe the commit hash, author, date, and message.

## Updating Git Defaults for Inclusivity

### Why Change the Default Branch Name?

Traditionally, Git repositories use `master` as the default branch name. However, to promote inclusivity and remove language that might be perceived as insensitive, the Git community has adopted `main` as the new default branch name. Many platforms, like GitHub, now use `main` by default for new repositories.

The very bottom left of VS Code (left part if status bar) shows the branch name, which should be `master` by default

<img src="./images/Git branch in VS Status bar.png">

### How to Set `main` as the Default Branch

1. **Change an Existing Repository's Default Branch:**

   If you already have a repository where the default branch is `master`, you can rename it:

   ```bash
   git branch -m master main
   ```

   This renames the branch locally. The branch name on the status bar will update from `master`to `main`after a successful change.

   <img src="./images/Branch name changes to main.png">

2. **Configure Git Globally:**
   You can set `main` as the default branch for all new repositories by running:

   ```bash
   git config --global init.defaultBranch main
   ```

   This ensures that whenever you initialise a new repository, the default branch will be named `main`.

### Best Practices for Working with Default Branches

- Always align your local repository's default branch with the remote repository.
- Inform collaborators about the branch name change to avoid confusion.
- When contributing to open-source projects, check the project's default branch before starting work.

## Key Takeaways

- Git helps you manage changes in your project.
- Use `git add` to stage changes and `git commit` to save them.
- Always write meaningful commit messages.

By the end of this lesson, students will have successfully tracked changes in their first project using Git!
