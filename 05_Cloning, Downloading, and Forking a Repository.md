# Cloning, Downloading, and Forking a Repository

## Learning Objectives

By the end of this lesson, students will be able to:

1. Understand the differences between downloading, cloning, and forking repositories.
2. Download a repository as a ZIP file.
3. Clone a repository using Git commands.
4. Fork a repository and set up a local copy for collaboration.

## Downloading a Repository

### What is Downloading?

Downloading a repository is the process of retrieving all the files from a GitHub project as a compressed ZIP file. This is useful for quickly accessing the files without needing Git or version control.

### How to Download a ZIP File from GitHub

1. Go to the GitHub repository’s main page.
2. Locate the green Code button.
3. Click on it and select Download ZIP.
   <img src="./images/Downloading repo.png">
4. The repository will be downloaded as a ZIP file to your computer.
5. Extract the ZIP file to access the project files.

## Cloning a Repository

### What is Cloning?

Cloning creates a local copy of a remote repository on your computer. Unlike downloading, cloning includes the entire Git history and allows you to interact with the repository using Git commands.

### How to Clone a Repository with `git clone`

If you've already created or selected a parent folder for your repository and opened it in VS Code, follow these steps:

1. Open the Integrated Terminal:

   - In VS Code, open the Integrated Terminal by clicking on Terminal > New Terminal or using the shortcut Ctrl + `.
   - The terminal will start in the folder you’ve opened in VS Code (your parent folder).

2. Select or Create a Parent Folder:

   - Ensure the folder you’ve opened in VS Code is where you want to store the cloned repository.
     For example:
     ```
     Codespace Projects/
        SDF/  <- This is your parent folder
     ```
   - The cloned repository will create its own subfolder inside this parent folder.

3. Copy the Repository URL from GitHub:

   - Go to the repository on GitHub.
   - Click the green Code button and copy the repository URL (e.g., https://github.com/user/repository.git).

4. Clone the Repository:
   - In the Integrated Terminal, run the following command:
     ```bash
     git clone <repository-url>
     ```
   - For example:
     ```bash
     git clone https://github.com/user/repository.git
     ```
5. Navigate to the Cloned Repository:
   - Once the repository is cloned, Git will automatically create a subfolder with the same name as the repository (e.g., repository).
   - Move into the cloned repository folder by running:
     ```bash
     cd repository
     ```
6. Verify the Files in VS Code:
   - The cloned repository will appear as a subfolder in the Explorer Panel on the left.
   - If needed, you can switch to the cloned folder in VS Code by going to File > Open Folder and selecting the repository folder.

## Forking a Repository

### What is Forking?

Forking creates a personal copy of someone else’s repository in your GitHub account. This is commonly used when contributing to open-source projects.

### Why Fork a Repository?

- You can make changes without affecting the original project.
- It allows you to suggest changes through a pull request.
- Keeps your contributions organized.

### Steps to Fork a Repository

1. Open the GitHub repository you want to fork.
2. Click the Fork button at the top-right corner.
3. The repository will now appear in your GitHub account.

### Steps to Clone Your Fork

1. Navigate to your forked repository on GitHub.
2. Click the green Code button and copy the URL.
3. Clone it locally using `git clone`:
   ```bash
   git clone <your-forked-repository-url>
   ```

### Making Changes

- Edit the files locally.
- Stage and commit your changes:
  ```bash
  git add .
  git commit -m "Describe your changes"
  ```
- Push changes to your forked repository:
  `bash
git push  
`

## Activities

#### Download a Starter Project as a ZIP File

1. Share a GitHub repository link with students.
2. Ask them to download the repository as a ZIP file.
3. Extract the ZIP file and explore the contents.

### Clone a Repository Using Git

1. Provide students with the same repository URL.
2. Ask them to clone the repository using `git clone`.
3. Confirm they can navigate into the cloned folder and list files using the terminal.

### Fork, Clone, and Modify a Repository

1. Share a sample repository.
2. Ask students to fork the repository into their GitHub account.
3. Instruct them to clone their fork locally.
4. Have them make a simple change, such as updating a README file or adding a new file.
5. Guide them to commit and push changes to their forked repository.

## Key Takeaways

- Downloading is a quick way to get project files, but it doesn't include Git history.
- Cloning is ideal for creating a local Git-enabled copy of a repository.
- Forking allows you to create a personal copy of a repository for contributions or experimentation.
