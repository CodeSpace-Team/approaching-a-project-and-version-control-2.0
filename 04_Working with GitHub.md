# Working with GitHub

In this lesson, we'll introduce you to GitHub, a powerful platform that allows you to host your code remotely and collaborate with others. You'll learn how to create a GitHub repository, connect it to your local Git repository, and push changes to GitHub to keep your project updated.

## What is GitHub?

GitHub is a cloud-based platform for hosting and sharing code using Git, a version control system. It enables developers to:

- **Collaborate** on projects with others, even if they are in different locations.
- **Track and manage changes** made to code over time.
- **Host static websites** and projects directly from the repository.
- **Manage open-source projects** through features like forks, pull requests, and issue tracking.

GitHub provides a user-friendly interface for Git, making it easier to manage remote repositories. Think of it as a social network for developers, where you can share and collaborate on code, track issues, and even contribute to others' projects.

## Remote Repositories for Collaboration

A **remote repository** is a version of your project that is hosted on a platform like GitHub. It serves as a central source where you can:

- Share your project with collaborators.
- Backup your code so it’s not lost if something happens to your local machine.
- Contribute to other projects by forking repositories and submitting pull requests.

## Creating a GitHub Account

To use GitHub, you first need to create an account. Here’s how to do it:

1. **Go to GitHub**: Open [GitHub's website](https://github.com/).
2. **Sign Up**: Click the "Sign up" button and follow the prompts to create an account.
3. **Verify Email**: You w receive a confirmation email—click the link in the email to verify your account.
4. **Set up your profile**: Add your name, profile picture, and any other information you want to share.

Once you have your GitHub account set up, you can start creating repositories and managing your code remotely.

## Setting Up a Remote Repository on GitHub

After creating an account and logging in, you can create a new repository for your project. Here’s how:

1. **Click the "+" Icon:** In the upper-right corner of the GitHub dashboard, click the + icon and select New repository.
2. **Repository Name:** Give your repository a descriptive name (e.g., portfolio-website).
3. **Optional Description:** Write a short description of what your project does.
4. **Public or Private:** Choose whether the repository will be public or private. Public repositories can be viewed by anyone, while private repositories are only accessible to people you invite.
5. **Initialize with README:** Check the box to initialize the repository with a README file **if you have <u>not</u> created one locally**.
6. **Create Repository:** Click Create repository.

Now you have an empty repository on GitHub where you can push your local changes.

## Connecting a Local Repository to GitHub

Once your repository is created on GitHub, you need to connect it to your local Git repository so that changes can be pushed to the remote repository.

### Steps to connect your local repository:

1. **Navigate to your project folder:** Open the terminal in your project’s directory. If you’ve been following along with the previous lessons, this is the directory where your `README.md` and other files are located.

2. **Add the remote repository:** Use the following Git command to connect your local repository to the remote repository on GitHub:

   ```bash
   git remote add origin https://github.com/username/repository-name.git
   ```

   Replace `username` with your GitHub username and `repository-name` with the name of your repository.

3. **Check if the remote is added:** You can verify the connection by running:

   ```bash
   git remote -v
   ```

   This will show you the URL of the remote repository.

## Pushing Changes to GitHub

Once your local repository is connected to GitHub, you can push changes to the remote repository. This will update your GitHub repository with the changes you’ve made locally.

### Steps to push your local changes:

1. **Stage changes:** Before you can push your changes, you need to stage them. For example, if you've made updates to your `README.md` file, you would run:

   ```bash
   git add README.md
   ```

2. **Commit changes:** After staging, commit the changes to your local repository:

   ```bash
   git commit -m "Update README with project description"
   ```

3. **Push changes:** Now, you can push the changes to the remote repository on GitHub:

   ```bash
   git push -u origin main
   ```

   - The `-u` flag tells Git to remember the remote branch (you only need to use it the first time).
   - `origin` is the name of your remote repository.
   - `main` is the default branch name. (If your default branch is named master, use that instead.)

## Activities

- Create a new repository on Github, name it `my-project`.
- Select Public or Private visibility.
- Do not initialize the repository with a README file.
- Connect local repository to Github.
- Push local changes to Github.
- Verify changes on Github, reload the repo and verify that the README file appears with the content you created locally.
- Add a new section to the local README called Skills, list your skills (Github, markdown, etc) under the section.
- Commit and push your changes to the remote repo.
- Confirm that the updates appear on the remote repo.
